# Ctrl-World Rollout Visualizations

Static GitHub Pages artifact for visual review of Ctrl-World rollout results.

Published URL:

- https://sellerbubble.github.io/ctrl-world-policy-rollouts/

The root page is organized into two top-level parts:

1. Official Ctrl-World checkpoint rollouts
   - matched-length policy-in-loop rollout videos across 7 tasks
   - long-horizon pred-only pickplace rollout videos
   - world model: provided Ctrl-World checkpoint-10000 setup

2. Our trained checkpoint rollouts
   - validate video-generation results for 100k, 200k, and 300k checkpoints
   - standard autoregressive replay results, 25 frames per video
   - longer autoregressive replay results, 49 frames per video
   - media under `media/ckpt_eval/{validate,replay,long_replay}`

Videos are folded by task, instruction condition, result group, or sample row.
Click a section to expand the videos. All videos default to `1.75x` playback
speed in the page script.
