# Ctrl-World Rollout Visualizations

Static GitHub Pages artifact for visual review of Ctrl-World rollout results.

Published URL:

- https://sellerbubble.github.io/ctrl-world-policy-rollouts/

The root page is organized into five top-level parts:

1. Official Ctrl-World checkpoint rollouts
   - matched-length policy-in-loop rollout videos across 7 tasks
   - long-horizon pred-only pickplace rollout videos
   - world model: provided Ctrl-World checkpoint-10000 setup

2. Our trained checkpoint rollouts
   - validate video-generation results for 100k, 200k, and 300k checkpoints
   - standard autoregressive replay results, 25 frames per video
   - longer autoregressive replay results, 49 frames per video
   - official DROID replay metric sweep for 20 checkpoints from 20k to 400k
   - media under `media/ckpt_eval/{validate,replay,long_replay}`
   - official replay metrics under `media/ckpt_eval/official_droid_replay_20ckpts`

3. AgiBot camera pose and ray visualization
   - interactive 3D camera-center, image-plane, and ray animation
   - synchronized left-wrist, right-wrist, and head videos
   - page under `camera_ray_visualization/task327_ep0_stacked_views/`

4. AgiBot semantic mask review
   - task-diverse 20-episode full-video overlay with small/medium/large semantic masks
   - earlier semantic-mask pipeline stage review
   - page under `semantic_mask_review/`

5. Camera ray conditioning design
   - forward-pass diagram for Ctrl-World training with dense camera-ray conditioning
   - figure under `camera_ray_conditioning/`

Videos are folded by task, instruction condition, result group, or sample row.
Click a section to expand the videos. All videos default to `1.75x` playback
speed in the page script.
