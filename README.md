# Ctrl-World Policy Rollout Experiments

Static GitHub Pages artifact for the Ctrl-World policy-in-loop rollout batches.

Published URLs:

- Main policy rollout page: https://sellerbubble.github.io/ctrl-world-policy-rollouts/
- Checkpoint visualizations: https://sellerbubble.github.io/ctrl-world-policy-rollouts/checkpoint-visualizations/

Main page contents:

- `index.html`: compact experiment record page for policy rollouts.
- `media/matched_length/*/*.mp4`: 44 validation-length matched policy rollouts across 7 tasks. Each video already contains true video on the top row and policy rollout on the bottom row.
- `media/long_horizon/*/*.mp4`: 20 long-horizon pred-only pickplace policy rollouts, covering all 10 validation trajectories under two instruction conditions.

Checkpoint visualization page contents:

- `checkpoint-visualizations/index.html`: unified visual review page for validate/replay/long-replay checkpoint results.
- `media/ckpt_eval/validate/`: validate video-generation results for 100k, 200k, and 300k checkpoints.
- `media/ckpt_eval/replay/`: standard autoregressive replay results, 25 frames per video.
- `media/ckpt_eval/long_replay/`: longer autoregressive replay results, 49 frames per video.

All videos on both pages default to `1.75x` playback speed in the page script.
