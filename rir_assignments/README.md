# RIR channel assignments

For each dataset, the RIR (room impulse response) channel used to generate the reverberant observation is specified by `h1_index`. Under the same-room mismatch (SR) condition, the training-specific RIR is randomly selected from the remaining four channels, with the exact assignment used in the reported experiments provided as `h2_SR_index`. Under the matched (oracle) condition, the training-specific RIR is identical to the observation RIR.

All indices are zero-based and refer to the five channels of the corresponding ACE Cruciform RIR. Within each dataset, the same fixed assignment sequences are used across the three acoustic environments (ACE 803 / 508 / 403a).

- `<dataset>_rir_assignments.csv` — columns `utterance_id, h1_index, h2_SR_index`
- `<dataset>_h1_indices.npy`, `<dataset>_h2_SR_indices.npy` (EARS: `ears100_<room>_h1_indices.npy`, `ears100_<room>_h2_indices.npy`, identical across rooms) — one entry per utterance, in the row order of the CSV
- `ears100/ears100_revision_filelist.txt` — the 100 EARS-100 utterance file names, in CSV order

The IEEE and LibriSpeech assignments were recovered from the original experiment manifests.
