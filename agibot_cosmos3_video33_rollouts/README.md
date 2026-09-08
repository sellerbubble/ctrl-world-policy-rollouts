# Cosmos3 AgiBot 33-frame ID/OOD rollouts

This directory publishes the visual evaluation artifact for a Video2World-only
Cosmos3 adaptation on AgiBot World data. It contains 80 complete rollouts, 80
contact sheets, per-task galleries, and aggregate metrics for the head-camera
and native-canvas input modes.

[Open the interactive report](index.html)

## Evaluation protocol

- Checkpoint: step 100, selected as the earliest checkpoint used for the formal
  rollout evaluation.
- Prompt: `task_name + current subgoal`.
- Temporal format: three autoregressive 33-frame segments per task at 10 Hz.
- Assembly: duplicate boundary frames are removed, producing one 97-frame
  video (about 9.7 seconds) per task.
- Randomness: seed `20260829` is held fixed across views and task splits.
- Coverage: 20 training-distribution (ID) tasks and 20 held-out (OOD) tasks for
  each of the head and native-canvas modes.

## Results

| Split / view | Tasks | 97-frame videos | Boundary / within-frame MAE | Visible motion adherence |
| --- | ---: | ---: | ---: | --- |
| ID / Head | 20 | 20 | 1.531 | 14 clear, 6 partial, 0 fail |
| ID / Canvas | 20 | 20 | 1.351 | 17 clear, 3 partial, 0 fail |
| OOD / Head | 20 | 20 | 1.357 | 14 clear, 6 partial, 0 fail |
| OOD / Canvas | 20 | 20 | 1.307 | 14 clear, 6 partial, 0 fail |

The canvas variant has the lower segment-boundary penalty on both ID and OOD.
Its largest visible advantage is on ID motion adherence (17/20 clear versus
14/20 for head). On the held-out task set, both modes have the same manual
adherence counts, so these results do not establish an OOD task-success
advantage for either view.

## Interpretation limits

The adherence labels measure visible target-directed arm motion and interaction
progress. They are not simulator or real-robot task-success measurements. A
`partial` label often means that the 9.7-second rollout ends while the robot is
still approaching or interacting with the target. Boundary/within MAE is a
continuity diagnostic, not a perceptual-quality or semantic-success score.

The published artifact intentionally excludes training caches, intermediate
segments, machine-specific paths, and private infrastructure provenance. The
machine-readable aggregate is in [`summary.json`](summary.json), and the ID
manual labels are in
[`id/manual_id_rollout_adherence_v1.csv`](id/manual_id_rollout_adherence_v1.csv).
