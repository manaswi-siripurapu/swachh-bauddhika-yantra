# Swachh Bauddhika Yantra — Trash Detection Dataset

This repository contains image data associated with **Swachh Bauddhika Yantra (SBY)**, an autonomous indoor cleaning robot designed to navigate indoor environments and identify trash and obstacles. The dataset supports the trash-detection component of the project.

## Repository Structure

```text
.
├── dataset/
│   ├── paper/
│   ├── aluminium_foil/
│   ├── cement_dust/
│   ├── bottle/
│   ├── wrapper/
│   └── wooden_dust/
└── sample_annotations/
    ├── paper/
    ├── aluminium_foil/
    ├── cement_dust/
    ├── bottle/
    ├── wrapper/
    └── wooden_dust/
```

Each class directory contains the files assigned to that category. `dataset/` contains the dataset images, while `sample_annotations/` contains sample annotation material organized by the same six categories. Refer to the files in each folder for the exact image and annotation formats.

## Classes

| Class name | Description |
|---|---|
| `paper` | Paper waste |
| `aluminium_foil` | Aluminium foil waste |
| `cement_dust` | Cement dust or fine debris |
| `bottle` | Bottle waste |
| `wrapper` | Wrapper or packaging waste |
| `wooden_dust` | Wooden dust or fine wood debris |

These categories reflect waste types relevant to the robot's cleaning and collection workflow.

## Project Context

SBY combines onboard computer vision, autonomous navigation, obstacle avoidance, and cleaning actions. The trash-detection component is intended to identify waste from camera images so that the system can select an appropriate response, such as collecting an object with the robotic arm or vacuuming smaller debris.

The project described in the accompanying research work uses an RGB camera mounted at a low height and angled downward to improve the visibility of floor-level objects. Images were collected in a laboratory setting with variation in object orientation, background, and lighting.

## Dataset Notes

- The folders are organized by the six waste categories listed above.
- The repository's folder structure alone does not specify the total number of images, image dimensions, train/validation/test split, or annotation format. Consult the actual files and dataset configuration before using the data for training.
- The research work also discusses `floor` and `obstacle` as annotation classes. Those classes are not represented as top-level folders in the six-class structure shown here.
- Do not assume that every image has a corresponding annotation file unless you have verified the folder contents.

## Usage

1. Clone or download this repository.
2. Inspect `dataset/` and `sample_annotations/` to confirm the image formats and annotation conventions.
3. If training an object-detection or instance-segmentation model, ensure the annotations match the model's expected format and that class IDs are mapped consistently.
4. Create separate training, validation, and test sets before applying augmentation. Apply augmentation to the training set only to avoid data leakage into evaluation sets.

No specific train/validation/test split or training configuration is prescribed by this README; configure these based on the files available in the repository.

## Citation and Attribution

If you use this dataset, please cite or acknowledge the associated work:

> **Design and Development of Navigation System and Trash Detection for Swachh Bauddhika Yantra.**

Please verify the final publication details and citation metadata before using this as a formal bibliographic reference.

## License

No license information was provided in the available project context. Unless a license file is added to this repository, reuse and redistribution permissions are not explicitly specified. Add an appropriate `LICENSE` file if you intend to grant permissions for others to reuse the dataset.
