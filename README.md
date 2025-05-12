
# 🪝 DTCFT: Detection, Tracking, and Counting of Fishing Traps Dataset

This repository contains the **DTCFT dataset**, introduced in the paper:

**TrapCounter: Integrating Detection, Tracking and Optical Flow for the Automatic Counting of Active Fishing Traps**  
Ali Soltaninezhad, Melissa Cote, Alejandro Rico Espinosa, Tunai Porto Marques,  
Alexandra Branzan Albu, Justin Paetkau, Vanessa Diaz, Jacob Lower  
*University of Victoria & Archipelago Marine Research*
22nd Conference on Robots and Vision (oral presentation)

[[📄 Paper]](link-to-paper) | [[📽 Sample Videos]](link-to-videos-if-any)

---

## 📦 Dataset Description

**DTCFT** is the **first public dataset** designed for the detection, tracking, and counting of sablefish fishing traps in real-world fishing vessel footage. It includes annotated videos captured on commercial and survey vessels operating off the coast of British Columbia, Canada. Usage is for research purposes only.

### ✨ Key Features

- **10 videos** (330 seconds each, 1080p, 5 FPS)
- **16,500 frames** with tracking annotations (bounding boxes + IDs)
- **3,300 keyframes** for detection (1 every 5 frames)
- **Annotations** include:
  - Bounding boxes (COCO format)
  - Unique tracking IDs
- **Environmental diversity**: day/night, occlusion, fog, water droplets, and more
- **Two vessel types**: Commercial and Survey

---

## 🗂 Dataset Structure

```
DTCFT/
├── detection/
│   ├── O1/
│   │   ├── images/           # Detection frames
│   │   └── labels/           # YOLO-format label files
│   ├── O2/
│   │   ├── images/
│   │   └── labels/
│   └── ... (O3 to O10)
│
└── tracking/
    ├── videos/                # 10 anonymized video clips
    └── annotations/           # JSONs with bboxes + tracking IDs
```

---

## 🧠 Annotation Guidelines

- Annotated with [CVAT](https://github.com/cvat-ai/cvat)
- Traps with ≥25% visibility were annotated
- Bounding boxes include occluded areas
- Piles of traps annotated as single objects
- Text and faces anonymized using black masks
- Format: COCO-compatible JSON

---

## 📊 Dataset Challenges

| Acquisition Challenges     | Content Challenges         |
|---------------------------|----------------------------|
| Variable lighting          | Crew occlusion             |
| Water on lens              | Piles of traps             |
| Lens obstruction           | Rare trap activity events  |

Each video is categorized as Low / Medium / High difficulty based on challenge presence.

---

## 📥 Download

**Coming soon!** The dataset will be made publicly available upon publication of the paper.

---

## 📚 Citation

If you use this dataset in your research, please cite:

```bibtex
@inproceedings{soltaninezhad2025trapcounter,
  title={TrapCounter: Integrating Detection, Tracking and Optical Flow for the Automatic Counting of Active Fishing Traps},
  author={Soltaninezhad, Ali and Cote, Melissa and Rico Espinosa, Alejandro and Porto Marques, Tunai and Branzan Albu, Alexandra and Paetkau, Justin and Diaz, Vanessa and Lower, Jacob},
  booktitle={Conference on Robots and Vision},
  year={2025}
}
```

---

## 📬 Contact

For questions or collaboration, contact:  
**Ali Soltaninezhad** – [alisoltaninezhad@uvic.ca](mailto:alisoltaninezhad@uvic.ca)
