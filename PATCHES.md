# List of patches in Godot for Sidescrollers

- `renderer_low_latency` - Reduced display latency through optional CPU/GPU synchronization.
    - Adds a new option via ProjectSetting `rendering/driver/synchronization/cpu_gpu_sync` and script function `RenderingServer::set_cpu_gpu_sync_mode()`.
    - When set to `Parallel`, behaves the same as vanilla.
    - When set to `Sequential`, can save 1-2 frames of display lag at the cost of reduced performance (though for pixel art games, chances are your FPS is so high you won't even notice, even on a more modest system).
    - The inclusion of `Sequential` is controversial, so the patch lives here for the time being.
