# **FaceSeg**
> [!Note]
> The [next version](https://github.com/Mikzarjr/Ultimate-Segmentation) of `CLIP-DINO-SAM` combination will come out soon!📆

> [!Tip]
> 📄 Paper with detailed explanation of the structure of the combination of `CLIP-DINO-SAM` models: [PDF](https://pdf.com)
>
> :octocat: Github with detailed workflow of labelling data with `CLIP-DINO-SAM` for `YOLO`: [Github]([(https://pdf.com)](https://github.com/Mikzarjr/Ultimate-Segmentation))

# 👀 Example Output
Here are example predictions of YOLO model segmenting parts of face after being trained on an auto-labeled dataset using `CLIP-DINO-SAM`

<div align="center">
  <p>
    <a align="center" href="">
      <img
        width="400"
        src="https://github.com/Mikzarjr/FaceSegmentation/blob/main/docks/demo_media/CDS_Output_1.jpeg"
        alt="CDS Output 1"
      >
    </a>
    <a align="center" href="https://github.com/Mikzarjr/FaceSegmentation/blob/main/docks/demo_media/CDS_Output_2.jpeg" target="_blank">
      <img
        width="400"
        src="https://github.com/Mikzarjr/FaceSegmentation/blob/main/docks/demo_media/CDS_Output_2.jpeg"
        alt="CDS Output 2"
      >
    </a>
  </p>
</div>

# 📚 Basic Concepts



#
# 💿 Installation
### Clone repo
```bash
git clone https://github.com/Mikzarjr/Face-Segmentation
```

### Install requirements
```bash
pip install -r FaceSeg/requirements.txt
```
or
```bash
pip install -e setup.py
```

# 🚀 Quickstart
### Import dependencies
```python
from FaceSegmentation.Pipeline.Config import *
from FaceSegmentation.Pipeline.Segmentation import FaceSeg
```

### Choose image to test the framework 
sample images are located in FaceSeg/TestImages
```python
image_path = f"{IMGS_DIR}/img1.jpeg"
```

### Run the following cell to get segmentation masks
Main segmentation mask is located in /segmentation/combined_masks

All separate masks are located in /segmentation/split_masks
```python
S = FaceSeg(image_path)
S.Segment()
```
### Create COCO.json annotations
```python
from FaceSegmentation.Pipeline.CreateJson import CreateJson
```
```python
A = CreateJson(image_path)
A.CreateJsonAnnotation()
```







