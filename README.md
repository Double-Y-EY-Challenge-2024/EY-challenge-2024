# 2024 EY Open Science Data Challenge: Tropical Storm Damage Detection Model

### Team: Double Y (Yi Jie Wong, Yin Loon Khor, Liu Ziwei)

The goal of the [challenge](https://challenge.ey.com/challenges/tropical-cyclone-damage-assessment-lrrno2xm) is to develop a machine learning model to identify and detect “damaged” and “un-damaged” coastal infrastructure (residential and commercial buildings), which have been impacted by natural calamities such as hurricanes, cyclones, etc. Participants will be given pre- and post-cyclone satellite images of a site impacted by Hurricane Maria in 2017 and build a machine learning model, designed to detect four different objects in a satellite image of a cyclone impacted area:
1. Undamaged residential building
2. Damaged residential building
3. Undamaged commercial building
4. Damaged commercial building

## Our Solution

- We are among the Top 10 Global Semi-Finalist of **EY Open Science Data Challenge 2024** 🎉🥳 </br>
- We ranked 8th in Phase 1 out of 11,000 registrants! 🌍🏆 </br>
- In terms of evaluation score, we rank 4th, tying with other impressive competing teams! 🤩
- Meanwhile, we ranked 1st out of 22 teams in Malaysia! 🏅

![methodology](https://github.com/yjwong1999/EY-challenge-2024/blob/main/Team%20Double%20Y%20-%20Methodology.jpg?raw=true)

<!-- 
## Business Idea: Data Fleet is What You Need
- Data is often compared to oil, but like oil, data needs to be refined and transformed to unleash its true potential.
- Our proposed method achived promising results with minimal training data!
-->

## Repo Structure
```
EY-challenge-2024
├── our-best-runs                       (proof of our experiment that yields the highest mAP)
│   ├── detect
│   │   ├── predict                     
│   │   ├── train                       
├── additional-dataset.zip              (additional dataset)
├── best-trained-model.pt               (best trained model which we used for submission, mAP 0.51)
├── challenge_1_submission_images.zip   (just the zip file of EY Challenge Phase 1 test images)
├── labelled-dataset.zip                (labelled dataset)
├── Model-development-notebook.ipynb    (to train the model)
├── pretrained-on-msft-puerto-rico      (models pretrained on Microsoft Building Footprint -> Puerto Rico dataset)
├── requirements.txt                    (dependencies requirement)
├── Validation-notebook.ipynb           (for Phase 1 submission)
```

## Setup environment
```bash
# Clone the repo
git clone https://github.com/yjwong1999/EY-challenge-2024.git
cd EY-challenge-2024

# Create conda environment
conda create --name ey-challenge python=3.8.10 -y
conda activate ey-challenge
```

## Training
<!-- 
1. Start with `1 BuildingDetection.ipynb` to pretrain a YOLOv8n model using [Msft Building Footprint](https://planetarycomputer.microsoft.com/dataset/ms-buildings) dataset. A pretrained experiments outputs (including the weights) of Module 1 are provided in `pretrained` directory. So unless you want to modify the training pipeline for Module 1, you can skip this and directly go to Module 2.
2. With the pretrained model, you can proceed to `2 Finetuner.ipynb`. In this module, you will fine-tune the pretrained model from Module 1 on the EY Training Dataset
-->
1. Use `Model-development-notebook.ipynb` to train the model following our pipeline. If you cant download the `additional-dataset.zip` due to filesize error, than you can use `Model-development-notebook (backup).ipynb` as an alternative
2. Use `Validation-notebook.ipynb` to generate `submission.zip`

## Download dataset
1. Our submitted `content-package` can be found in this [link](https://drive.google.com/drive/folders/1KI9Fh0qCpzWMw-Cf9eWf0-LAyC9nIq1n?usp=sharing). You can find all of our datasets here as well

## Cite this repository

```
@INPROCEEDINGS{10174362,
  author={Wong, Yi Jie and Khor, Yin-Loon and Liu, Ziwei},
  booktitle={}, 
  title={Automating Coastal Vulnerability Assessment: AI-Driven Geospatial Analysis via Building Damage Detection}, 
  year={2024},
  volume={},
  number={},
  pages={},
  doi={https://doi.org/10.36227/techrxiv.172963135.56918790/v1}}
```
