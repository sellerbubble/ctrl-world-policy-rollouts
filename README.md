# Ctrl-World Policy Rollout Experiments

Static GitHub Pages artifact for the Ctrl-World policy-in-loop rollout batches.

Contents:

- `index.html`: compact experiment record page.
- `media/matched_length/*/*.mp4`: 44 validation-length matched policy
  rollouts across 7 tasks. Each video already contains true video on the top
  row and policy rollout on the bottom row.
- `media/long_horizon/*/*.mp4`: 8 long-horizon pred-only pickplace policy
  rollouts.

Source batches in the local Ctrl-World workspace:

- `remote_results/policy_length_matched_pickplace_v1_20260615`
- `remote_results/policy_length_matched_remaining_v1_20260616`
- `remote_results/policy_long_horizon_pickplace_v1_20260615`

This page intentionally omits detailed per-video run ids, GPU logs, review
indexes, and quality metric plots. Those remain in the research workspace.

All videos default to `1.75x` playback in the page script.
