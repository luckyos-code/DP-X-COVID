# Privacy-Preserving Detection of COVID-19 in X-Ray Images

## Contents
* [Report](reports/Masters_Thesis_Lucas_Lange.pdf) - Master's Thesis, English
* [Results](results/) - Figures and Tables
* [Experiments](experiments/) - Jupyter Notebooks

## Abstract
Chest X-rays enable a fast and safe diagnosis of COVID-19 in patients. Applying Machine Learning (ML) methods can support medical professionals by classifying large numbers of images. However, the amount of data needed for training such classifiers poses problems due to clinical data privacy regulations, which present strict limitations on data sharing between hospitals. Specifically, the models resulting from ML are vulnerable to attacks and can compromise data integrity by leaking details about their training data. Privacy-Preserving ML (PPML) offers methods to create private models that satisfy Differential Privacy (DP), enabling the development of medical applications while maintaining patient privacy.

This work aims at investigating the privacy-preserving detection of COVID-19 in X-ray images. The PPML training methods DP-SGD and PATE are matched against non-private training. The private models should mitigate the data leakage threats posed by Membership Inference Attacks (MIAs). However, the inclusion of DP showed no improvements in MIA defense on the COVID-19 detection task. Instead, the non-private models presented the same repelling properties as the private models. Thus, if only the defense against MIAs is of concern, the non-private approach achieving 97.6\% classification accuracy is the best choice. Private DP-SGD training for $\varepsilon = 1$ is a more sensible alternative when a theoretical privacy guarantee is needed. The best DP-SGD model reaches 74.1\% accuracy. Even though the accuracy-privacy trade-off of 23.5\% is significant, the private model performs 0.3\% better than related work and keeps much tighter privacy guarantees. Ultimately, the conflicting findings from the additional experiments on the MNIST database, where DP significantly increased MIA defense, indicate that PPML (or DP-SGD) is heavily task-dependent. Thus, research on one dataset might not carry over to others.
