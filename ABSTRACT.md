The **Windmill Detection on French Aerial Images Dataset** was curated from 11 raster samples extracted from the latest French aerial images of 2021, each containing a minimum of 20 windmills per sample. These samples were cropped to a size of 2048*2048 pixels for training and validation purposes. During the selection of these areas, the authors delineated the regions of interest (ROI), defined as the union of the bounding boxes of the raster images. Initially, the raster images were in JPEG2000 format but were converted to JPEG to facilitate labeling using the [YBAT tool](https://github.com/drainingsun/ybat). YBAT, an open-source labeling tool, was chosen due to its lack of size constraints and ease of installation, as it is built with pure HTML and JavaScript. Raster sampling was conducted using the sampling and generation functions of [Odeon landcover](https://dai-projets.gitlab.io/odeon-landcover/), resulting in a training folder comprising the 11 raster samples divided into smaller patches. These patches were labeled and subsequently split into training and validation datasets.

<img src="https://github.com/dataset-ninja/windmill-detection-french/assets/120389559/7be913c7-e86c-4674-b3a2-cce8508b8fbb" alt="image" width="800">

The labelling is manually done with the YBAT tool. It helps producing the label files in YOLO V5 accepted format. The labelling was done following those principles :

* Select the whole windmill in a box
* If only a part of a windmill is visible, we also select it
* The authors don't select the shadow of the windmill