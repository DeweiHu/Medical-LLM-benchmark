# Public benchmarks for medical LLMs

This is a updating summary for the public benchmarks for medical LLMs.

### Diagnosis based on text description
| | Benchmark | Question types | Data source | Input modality | Reasoning label | Paper |
| :--: | :-----: | :-----: | :-----: | :-----: | :-----: | :--------- |
| 1 | MedQA | choice | [link](https://ukgovernmentbeis.github.io/inspect_evals/evals/medqa/index.html) | text description | ✔️ | [What Disease Does This Patient Have? A Large-Scale Open Domain Question Answering Dataset from Medical Exams](https://arxiv.org/abs/2009.13081) 
| 2 | DiagnosisArena | choice | [link](https://github.com/SPIRAL-MED/DiagnosisArena) | text description | ✔️ | [DiagnosisArena: Benchmarking Diagnostic Reasoning for Large Language Models](https://aclanthology.org/2026.findings-acl.151.pdf) |
| 3 | PubMedQA | noul | [link](https://pubmedqa.github.io/) | text description | ✔️ | [PubMedQA: ADataset for Biomedical Research Question Answering](https://aclanthology.org/D19-1259.pdf) |
| 4 | NEJM | choice | [link](https://www.nejm.org/case-challenges) | text description + image | ✖️ | - |


### Clinical prediction (MIMIC-IV)
| Modality | MIMIC resource | Data format | Description |
| :-----: | :-----: | :-----: | :--------- |
| ECG | [MIMIC-IV-ECG](https://physionet.org/content/mimic-iv-ecg/1.0/) | 12-lead waveform | ~800k ECGs, ~160k patients; 10 s, 500 Hz |
| Echo | [MIMIC-IV-Echo](https://physionet.org/content/mimic-iv-echo/1.0.1/) | Echo DICOM sequences + structure measurements | 524,137 DICOM files, 7,228 studies, 4,572 patients for imaging; structured measurements from 206,488 studies / 91,372 patients |
| Chest X-ray | [MIMIC-CXR](https://physionet.org/content/mimic-cxr/2.1.0/) | Raw CXR DICOM images + radiology report | 377,110 images, 227,835 studies; patient/study IDs available |
| Clinical text | [MIMIC-IV-Note](https://www.physionet.org/content/mimic-iv-note/2.2/) | Discharge summaries and radiology reports | Linked by `subject_id`; radiology reports cover X-ray, CT, MRI, ultrasound, etc |
| Structured EHR | [MIMIC-IV Clinical Database](https://physionet.org/content/mimiciv/3.1/) | Demographics, diagnoses, labs, medications, procedures, admissions, ICU data | longitudinal clinical context |
| ED data | [MIMIC-IV-ED](https://physionet.org/content/mimic-iv-ed/2.2/) | Triage, vitals, chief complaint, diagnoses, medications, disposition | ~425k ED stays, linked to MIMIC-IV through `subject_id` / `hadm_id` |
| Continuous bedside signals | MIMIC-IV Waveform Database | ECG monitor waveform, PPG, arterial BP, respiration, etc. | Linked to clinical MIMIC-IV records; current published release is much smaller than diagnostic ECG |
