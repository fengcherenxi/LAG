# LAG-Pytorch
Official pytorch codes and models for paper:

A Benchmark Dataset of Endoscopic Images and Novel Deep Learning Method to Detect Intestinal Metaplasia and Gastritis Atrophy

# Pretrained Model & Datasets
Our models can be found in our Netdisk: [our-model](https://pan.baidu.com/s/1O2P7n38AJExaximzRy8vsA ) && Extraction code is: 1234

To view a sample of the data: [data-samples](https://github.com/fengcherenxi/LAG/tree/main/data)

To download data please contact: juanliao@scu.edu.cn && c.luo@uestc.edu.cn

To view the test results on video: [video-result](https://github.com/fengcherenxi/LAG/blob/main/resources/Video_results.mp4)

# Inspiration Model Architecture
This is an official implementation of Accurate Detection of Intestinal Metaplasia and Gastritis Atrophy using Local attention grouping network paper.

![](https://github.com/fengcherenxi/LAG/blob/main/resources/color.png#pic_center=300x400)

Differences between WLI and LCI images. LCI’s distinctive color space could highlight the gastric lesions.

We build a novel and relatively big endoscopy dataset of 21,420 images from the widely used White Light Imaging (WLI) endoscopy and more recent Linked Color Imaging (LCI) endoscopy, which were annotated and double checked by experienced radiologists, presenting a benchmark dataset.

![](https://github.com/fengcherenxi/LAG/blob/main/resources/datasets.png)

Samples of the developed Endoscopic dataset. The first row shows the WLI samples; the second row shows the LCI samples of the same positions. Each column indicates the position where the images were taken.

![](https://github.com/fengcherenxi/LAG/blob/main/resources/ourModel.png)

The working mechanism of the human visual system. Cone cells process multiple visual signals through bipolar cells and ganglion cells to obtain local stimulus. Rod cells process multiple visual signals through bipolar cells and ganglion cells to obtain fuzzy global stimulus.

Inspired by this cellular structure of the human eyes, we design an effective ensemble structure to supplement the local pixel information of the original input.

The local attention grouping (LAG) model. The LAG model structure is designed following the working principle of human vision cells. Ensemble modules are designed to imitate the cone cells and process locally critical information. The number of random crop depends on the results of the ablation experiment. The backbone pathway imitates the rod cells and processes the globally critical information.
# Experiments
## Qualitative
![](https://github.com/fengcherenxi/LAG/blob/main/resources/video_test.png)
## Quantitative
![](https://github.com/fengcherenxi/LAG/blob/main/resources/model_test_IM.png)

![](https://github.com/fengcherenxi/LAG/blob/main/resources/model_test_GA.png)
# Requirements
```
pytorch==1.7+cuda10.1
torchvision==0.6.0
numpy==1.19.5
```
# Citation
```
Jie Yang, Wenjian Sun, Yang Luo, Chunbo Luo. A Benchmark Dataset of Endoscopic Images and Novel Deep Learning Method to Detect Intestinal Metaplasia and Gastritis Atrophy [J].[Under review]
```