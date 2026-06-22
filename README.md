# Ctrl-World Checkpoint Visualizations

Static GitHub Pages artifact for Ctrl-World validate/replay visual review.

Published URL:

- https://sellerbubble.github.io/ctrl-world-policy-rollouts/

Current contents:

- `index.html`: unified visual review page.
- `media/ckpt_eval/validate/`: validate video-generation results for 100k, 200k, and 300k checkpoints.
- `media/ckpt_eval/replay/`: standard autoregressive replay results, 25 frames per video.
- `media/ckpt_eval/long_replay/`: longer autoregressive replay results, 49 frames per video.

Each section includes checkpoint summary metrics, a trend figure, per-sample CSVs,
and a video matrix. Videos show the true/recorded future on the top row and the
model prediction on the bottom row, with three camera views tiled horizontally.
All videos default to `1.75x` playback speed in the page script.

Source artifacts in the local Ctrl-World workspace:

- `remote_results/validate_ckpt_compare_100k_200k_300k_20260622`
- `remote_results/replay_ckpt_compare_100k_200k_300k_20260622`
- `remote_results/replay_ckpt_compare_100k_200k_300k_chunks12_20260622`
