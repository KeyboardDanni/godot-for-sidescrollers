# List of patches in Godot for Sidescrollers

- `patches/renderer_low_latency` - Reduced display latency through optional CPU/GPU synchronization.
    - Adds a new option via ProjectSetting `rendering/driver/synchronization/cpu_gpu_sync` and script function `RenderingServer::set_cpu_gpu_sync_mode()`.
    - When set to `Parallel`, behaves the same as vanilla.
    - When set to `Sequential`, can save 1-2 frames of display lag at the cost of reduced performance (though for pixel art games, chances are your FPS is so high you won't even notice, even on a more modest system).
    - The inclusion of `Sequential` is controversial, so the patch lives here for the time being.
- `patches/physics_lerp_settings_fix` - Fix changing physics interpolation in SceneTree at runtime.
    - There are multiple bugs that occur when toggling this setting while the game is running.
        - Any static nodes that start out invisible will shake violently once they are unhidden.
        - Camera stops updating completely.
    - These issues may be fixed in the pending physics interpolation rework. Until then, this patch acts as a stopgap.
- `patches/fork_readme` - Godot for Sidescrollers readme.
