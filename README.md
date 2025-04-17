# Audio_Detection_Project
# 🧠 MemoTag Speech Intelligence - Cognitive Impairment Detection

This project analyzes anonymized audio clips to detect early signs of cognitive impairment using unsupervised machine learning and NLP-based speech feature extraction.

---

## 📌 Objective

To extract meaningful linguistic and acoustic features from speech and identify participants showing early symptoms of cognitive decline, using unsupervised clustering.

---

## 🔍 Extracted Features

We extracted a mix of linguistic and prosodic (acoustic) features from the audio samples:

| Feature | Description |
|--------|-------------|
| **Pauses per sentence** | Measures average pause duration and frequency. Increased pauses can suggest retrieval or fluency issues. |
| **Hesitation markers** | Counts "uh", "um", etc. High counts indicate potential processing or memory delays. |
| **Word recall issues** | Detected word substitutions or semantic anomalies using basic NLP patterns. |
| **Speech rate** | Calculated in words per minute. Lower speech rate may signal cognitive strain. |
| **Pitch variability** | Measures changes in vocal pitch over time. Flattened prosody can indicate neurological issues. |
| **Naming/Word-Association Gaps** | Manual or pattern-based checks for missing key terms in expected tasks. |
| **Sentence Completion Failures** | Incomplete or abruptly stopped sentences were flagged. Often found in MCI patients. |

---

## 🤖 Machine Learning Method

### K-Means Clustering (Unsupervised)

- **Why K-Means?**  
  No labels were available (diagnosis info), so clustering helped uncover natural groupings.

- **Steps**:
  - Extract features per audio file.
  - Standardize with `StandardScaler`.
  - Cluster into 2 groups using `KMeans(n_clusters=2)`.
  - Visualized using `PCA` for 2D representation.

- **Outcome**:
  - Two distinct clusters emerged.
  - One cluster showed higher pauses, slower speech, and more hesitations — suggesting possible cognitive impairment patterns.

---

## 🔮 Next Steps (Toward Clinical Robustness)

| Area | Description |
|------|-------------|
| **Labeled Dataset** | Collaborate with clinicians to get ground truth diagnostic labels. |
| **Advanced NLP** | Use models like BERT to detect subtle semantic impairments. |
| **Acoustic Modeling** | Apply `openSMILE`, `Praat`, or deep learning for prosody and articulation features. |
| **Multimodal Fusion** | Combine text, audio, and (optionally) video cues. |
| **Clinical Validation** | Incorporate MMSE/MoCA scores and expert feedback to evaluate effectiveness. |

---

## ✅ Conclusion

This pipeline demonstrates how everyday voice recordings can be analyzed for cognitive health. With further data and refinement, this system can evolve into a valuable **non-invasive, scalable screening tool** for early-stage cognitive disorders.

---

