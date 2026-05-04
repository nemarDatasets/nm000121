[![DOI](https://img.shields.io/badge/DOI-10.82901%2Fnemar.nm000121-blue)](https://doi.org/10.82901/nemar.nm000121)

# SSVEP MAMEM 3 dataset

SSVEP MAMEM 3 dataset.

## Dataset Overview

- **Code**: MAMEM3
- **Paradigm**: ssvep
- **DOI**: 10.48550/arXiv.1602.00904
- **Subjects**: 11
- **Sessions per subject**: 1
- **Events**: 6.66=33029, 7.50=33028, 8.57=33027, 10.00=33026, 12.00=33025
- **Trial interval**: [1, 4] s
- **Runs per session**: 10
- **File format**: csv
- **Data preprocessed**: True

## Acquisition

- **Sampling rate**: 128.0 Hz
- **Number of channels**: 14
- **Channel types**: eeg=14
- **Channel names**: AF3, AF4, F3, F4, F7, F8, FC5, FC6, O1, O2, P7, P8, T7, T8
- **Montage**: 10-20
- **Hardware**: EGI 300 Geodesic EEG System (GES 300)
- **Software**: Microsoft Visual Studio 2010 with OpenGL
- **Reference**: CAR
- **Sensor type**: scalp electrodes
- **Line frequency**: 50.0 Hz
- **Online filters**: 5-48 Hz bandpass, 50 Hz notch
- **Impedance threshold**: 80.0 kOhm
- **Cap manufacturer**: EGI
- **Cap model**: HydroCel Geodesic Sensor Net (HCGSN)
- **Electrode type**: wet
- **Auxiliary channels**: ecg, gsr, ppg

## Participants

- **Number of subjects**: 11
- **Health status**: healthy
- **Age**: min=24.0, max=39.0
- **Gender distribution**: male=8, female=3
- **Handedness**: {'right': 10, 'left': 1}
- **BCI experience**: naive
- **Species**: human

## Experimental Protocol

- **Paradigm**: ssvep
- **Number of classes**: 5
- **Class labels**: 6.66, 7.50, 8.57, 10.00, 12.00
- **Trial duration**: 5.0 s
- **Study design**: Subjects focus attention on a violet box flickering at different frequencies (6.66, 7.50, 8.57, 10.00, 12.00 Hz) presented at the center of the monitor. Each trial lasts 5 seconds followed by 5 seconds rest.
- **Feedback type**: none
- **Stimulus type**: visual
- **Stimulus modalities**: visual
- **Primary modality**: visual
- **Synchronicity**: synchronous
- **Mode**: offline
- **Training/test split**: False
- **Instructions**: Subjects were instructed to focus attention on the flickering stimulus and minimize artifacts by reducing eye blinks and movements.
- **Stimulus presentation**: display=22 inch LCD monitor, 60 Hz refresh rate, 1680x1080 resolution, background=black, stimulus=violet box flickering at center of screen, graphics=Nvidia GeForce GTX 860M with vertical synchronization enabled

## HED Event Annotations

Schema: HED 8.4.0 | Browse: https://www.hedtags.org/hed-schema-browser

```
  6.66
    ├─ Sensory-event
    ├─ Experimental-stimulus
    ├─ Visual-presentation
    └─ Label/6_66

  7.50
    ├─ Sensory-event
    ├─ Experimental-stimulus
    ├─ Visual-presentation
    └─ Label/7_50

  8.57
    ├─ Sensory-event
    ├─ Experimental-stimulus
    ├─ Visual-presentation
    └─ Label/8_57

  10.00
    ├─ Sensory-event
    ├─ Experimental-stimulus
    ├─ Visual-presentation
    └─ Label/10_00

  12.00
    ├─ Sensory-event
    ├─ Experimental-stimulus
    ├─ Visual-presentation
    └─ Label/12_00

```
## Paradigm-Specific Parameters

- **Detected paradigm**: ssvep
- **Stimulus frequencies**: [6.66, 7.5, 8.57, 10.0, 12.0] Hz
- **Number of targets**: 5

## Data Structure

- **Trials**: 1104
- **Trials context**: Total of 1104 trials (5 seconds each) across all subjects and sessions. Subject S001: 3 sessions, S003 and S004: 4 sessions each, all others: 5 sessions. Each session includes 23 trials (8 adaptation + 15 experimental).

## Preprocessing

- **Preprocessing applied**: True
- **Steps**: bandpass filtering (5-48 Hz), notch filtering (50 Hz), artifact removal (AMUSE, ICA), Common Average Reference (CAR)
- **Highpass filter**: 5.0 Hz
- **Lowpass filter**: 48.0 Hz
- **Bandpass filter**: {'low_cutoff_hz': 5.0, 'high_cutoff_hz': 48.0}
- **Notch filter**: 50.0 Hz
- **Filter type**: IIR (Chebyshev, Elliptic)
- **Artifact methods**: AMUSE, ICA, FastICA
- **Re-reference**: CAR

## Signal Processing

- **Classifiers**: LDA, SVM, Random Forest, kNN, Naive Bayes, CCA, ELM, Decision Trees
- **Feature extraction**: Periodogram, Welch, Goertzel, Yule-AR, STFT, Discrete Wavelet Transform, PSD, CSP, ICA
- **Frequency bands**: analyzed=[5.0, 48.0] Hz
- **Spatial filters**: CAR, CSP, Minimum Energy

## Cross-Validation

- **Method**: leave-one-subject-out
- **Evaluation type**: cross_subject

## Performance (Original Study)

- **Accuracy**: 72.47%
- **Default Config Accuracy**: 72.47
- **Optimal Config Accuracy**: 79.47
- **Best Electrode Accuracy**: 74.42
- **Execution Time Ms**: 5.0

## BCI Application

- **Applications**: research, comparative_study
- **Environment**: laboratory
- **Online feedback**: False

## Tags

- **Pathology**: Healthy
- **Modality**: Visual
- **Type**: Perception

## Documentation

- **Description**: Comparative evaluation of state-of-the-art algorithms for SSVEP-based BCIs. Dataset includes 256-channel EEG signals from 11 subjects performing SSVEP tasks with 5 different flickering frequencies.
- **DOI**: 10.6084/m9.figshare.2068677.v1
- **Associated paper DOI**: arXiv:1602.00904v2
- **License**: ODC-By-1.0
- **Investigators**: Vangelis P. Oikonomou, Georgios Liaros, Kostantinos Georgiadis, Elisavet Chatzilari, Katerina Adam, Spiros Nikolopoulos, Ioannis Kompatsiaris
- **Senior author**: Ioannis Kompatsiaris
- **Institution**: Centre for Research and Technology Hellas (CERTH)
- **Country**: Greece
- **Repository**: Figshare
- **Data URL**: https://dx.doi.org/10.6084/m9.figshare.2068677.v1
- **Publication year**: 2016
- **Ethics approval**: Ethics committee of the Centre for Research and Technology Hellas, approved 3/7/2015
- **Keywords**: SSVEP, BCI, brain-computer interface, EEG, visual evoked potentials, comparative evaluation, signal processing

## Abstract

Brain-computer interfaces (BCIs) have been gaining momentum in making human-computer interaction more natural, especially for people with neuro-muscular disabilities. This report focuses on EEG-based BCIs that rely on Steady-State-Visual-Evoked Potentials (SSVEPs) and performs a comparative evaluation of state-of-the-art algorithms for filtering, artifact removal, feature extraction, feature selection and classification. The dataset consists of 256-channel EEG signals from 11 subjects, along with a processing toolbox for reproducing results.

## Methodology

Comparative evaluation of SSVEP-based BCI algorithms using leave-one-subject-out cross-validation. The study examines filtering methods (IIR, FIR), artifact removal (AMUSE, ICA), feature extraction (Periodogram, Welch, Goertzel, Yule-AR, STFT, DWT), feature selection (Shannon entropy, PCA, ICA), and classification (LDA, SVM, kNN, Naive Bayes, Random Forest, CCA, ELM, Decision Trees). Each parameter is studied independently while keeping others fixed to identify optimal configurations.

## References

Oikonomou, V. P., Liaros, G., Georgiadis, K., Chatzilari, E., Adam, K., Nikolopoulos, S., & Kompatsiaris, I. (2016). Comparative evaluation of state-of-the-art algorithms for SSVEP-based BCIs. arXiv preprint arXiv:1602.00904.

MAMEM Steady State Visually Evoked Potential EEG Database `<https://archive.physionet.org/physiobank/database/mssvepdb/>`_

S. Nikolopoulos, 2016, DataAcquisitionDetails.pdf `<https://figshare.com/articles/dataset/MAMEM_EEG_SSVEP_Dataset_III_14_channels_11_subjects_5_frequencies_presented_simultaneously_/3413851>`_
Appelhoff, S., Sanderson, M., Brooks, T., Vliet, M., Quentin, R., Holdgraf, C., Chaumon, M., Mikulan, E., Tavabi, K., Hochenberger, R., Welke, D., Brunner, C., Rockhill, A., Larson, E., Gramfort, A. and Jas, M. (2019). MNE-BIDS: Organizing electrophysiological data into the BIDS format and facilitating their analysis. Journal of Open Source Software 4: (1896). https://doi.org/10.21105/joss.01896

Pernet, C. R., Appelhoff, S., Gorgolewski, K. J., Flandin, G., Phillips, C., Delorme, A., Oostenveld, R. (2019). EEG-BIDS, an extension to the brain imaging data structure for electroencephalography. Scientific Data, 6, 103. https://doi.org/10.1038/s41597-019-0104-8

---
Generated by MOABB 1.4.3 (Mother of All BCI Benchmarks)
https://github.com/NeuroTechX/moabb
