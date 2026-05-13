# EEG Signal Noise Reduction Using SVD

A biomedical signal-processing project that uses Singular Value Decomposition, or SVD, to reduce EOG eye-movement artifacts from EEG recordings.

The project recreates and validates ideas from a classical EEG denoising paper using a linear-algebra-based subspace separation approach.

---

## Project links and evidence

| Item | Link / Note |
|---|---|
| Repository | https://github.com/Mrudula-itsjuzme/EEG-signal-reconstruction-using-SVD |
| Paper / reference | https://doi.org/10.1016/S0165-1684(96)00129-6 |
| Demo video | Not uploaded yet |
| Deployment | Not applicable; MATLAB signal-processing implementation |
| Dataset note | Uses simulated EEG/EOG mixtures; future validation planned on public EEG eye-artifact datasets |
| Result screenshots / plots | Add before/after reconstruction plots to the repo once finalized; current SNR results are documented below |

---

## Project context

**Team 9**

- Manohar P
- Mrudula
- Sainath
- Pushpak

---

## Reference paper

**Title:** SVD based technique for noise reduction in electroencephalographic signals  
**Authors:** P. K. Sadasivan and D. Narayana Dutt  
**Journal:** Signal Processing, Elsevier, 1996  
**DOI:** https://doi.org/10.1016/S0165-1684(96)00129-6

---

## Problem statement

EEG signals are weak and easily contaminated by eye-movement artifacts. These EOG artifacts can dominate the recorded signal and make brain-signal interpretation unreliable.

This project uses SVD to separate high-energy artifact components from the weaker EEG signal subspace.

---

## Method overview

```text
Simulated / Recorded EEG + EOG Mixture
              ↓
Data Matrix Construction
              ↓
SVD Decomposition
              ↓
Artifact Subspace Identification
              ↓
Noise / EEG Subspace Reconstruction
              ↓
Cleaned EEG + SNR Evaluation
```

---

## Key methodology

- model observed EEG as a mixture of true EEG, EOG artifacts, and noise
- apply SVD to decompose the observation matrix
- identify dominant singular components linked to high-energy artifacts
- reconstruct the desired EEG from the remaining subspace
- evaluate improvement using input and output SNR

---

## Implementation highlights

- MATLAB-based implementation
- simulated alpha rhythm at 10 Hz
- simulated beta rhythm at 20 Hz
- low-frequency EOG artifact modeling between 0–4 Hz
- recreated contaminated EEG with input SNR around -9.5 dB
- reported output SNR improvement around 13.83 dB to 19.16 dB

---

## Challenges handled

| Challenge | Solution |
|---|---|
| Sign indeterminacy | correlation check for inverted singular vectors |
| Rank estimation | artifact-subspace rank selected using energy dominance |
| Noise scaling | tuned sensor-to-signal power ratios to match expected SNR |

---

## Tech stack

- MATLAB
- Linear algebra
- Singular Value Decomposition
- Biomedical signal processing
- EEG/EOG artifact reduction

---

## Future improvements

- validate on public EEG eye-artifact datasets
- test with directly acquired EEG/EOG recordings
- compare SVD with ICA, wavelet denoising, and deep-learning denoisers
- add plots showing before/after reconstruction quality
- port the implementation to Python for wider reproducibility

---

## Author

Maintained by [Pedamallu Sai Mrudula](https://github.com/Mrudula-itsjuzme) as part of an applied AI, linear algebra, and biomedical signal-processing portfolio.
