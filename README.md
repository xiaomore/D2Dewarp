## D2Dewarp

The code for "D2Dewarp: Dual Dimensions Geometric Representation Learning Based Document Image Dewarping", CVPR 2026.

<div align=center>
<img width="350" height="200" src="https://github.com/xiaomore/D2Dewarp/blob/main/images/model1.png"/>
<img width="200" height="200" src="https://github.com/xiaomore/D2Dewarp/blob/main/images/model2.png"/>
</div>

#### Training Dataset
We propose a training set of distorted images with horizontal and vertical line annotations. 
You can find more details and download this dataset on [DocDewarpHV](https://github.com/xiaomore/DocDewarpHV).

#### Evaluation Dataset
We evaluate on three datasets [DocUNet](https://www3.cs.stonybrook.edu/~cvl/docunet.html) (130 images), 
[DIR300](https://github.com/fh2019ustc/DocGeoNet) (300 images)
and [DocReal](https://github.com/irisXcoding/DocReal) (200 images).

#### Training

Modify the data_path and related hyperparameters, and then execute the Python file:

 `python train.py --data_path /DATA/PATH --save_path /OUTPUT/DIR` 
 
 or execute the script:
 `bash train.sh /OUTPUT/DIR`

#### Inference
Please download the pre-trained model from 
[Google Drive](https://drive.google.com/drive/folders/1gv0lLaZWlUt1tX7EJDaVhtFhmV-ewQox?usp=sharing) 
or [Baidu Cloud](https://pan.baidu.com/s/1qnHjy3-ANlrrgjc7hac3Bg?pwd=2cut). Then execute:
 
 `python predict.py --model_path /MODEL/PATH --img_path /BENCHMARK/DIR --save_path /SAVE/PATH`

#### Evaluation

We follow the evaluation environment and code in [DocUNet](https://www3.cs.stonybrook.edu/~cvl/docunet.html) 
and [DocGeoNet](https://github.com/fh2019ustc/DocGeoNet).

For CER and ED metrics evaluation:

```text
Tesseract==5.0.1.20220118 (Windows)
pytesseract==0.3.8
```
For DocReal (Chinese Benchmark), we used PaddleOCR's ([Link](https://github.com/PaddlePaddle/PaddleOCR)) text detection model *DBNet* with “detv4_teacher_inference” and 
text recognition model *SVTR_LCNet* with “OCRv4_rec_server_infer”.

The dewarped images from our method can be downloaded from [Google Drive](https://drive.google.com/drive/folders/1gv0lLaZWlUt1tX7EJDaVhtFhmV-ewQox?usp=sharing) 
or [Baidu Cloud](https://pan.baidu.com/s/1qnHjy3-ANlrrgjc7hac3Bg?pwd=2cut).

#### License
This work need to be referenced under [CC BY-NC-ND 4.0 License](https://creativecommons.org/licenses/by-nc-nd/4.0/) for non-commercial research purposes.

#### Contact

If you have any questions about this work, you can always contact [hengli.lh@outlook.com](mailto:hengli.lh@outlook.com).

#### Acknowledgement
Thanks to [Doc3D](https://github.com/cvlab-stonybrook/doc3D-dataset) for open-sourcing the code.
We also thanks to [cddod](https://github.com/kailigo/cddod), [CDLA](https://github.com/buptlihang/CDLA), [M6Doc](https://github.com/HCIILAB/M6Doc) and [PubLayNet](https://github.com/ibm-aur-nlp/PubLayNet)
for their outstanding work in open-sourcing the original document images. 
Thanks to [DocTr](https://github.com/fh2019ustc/DocTr), [DocScanner](https://github.com/fh2019ustc/DocScanner), [RDGR](https://github.com/XiangWeiJiang/Document_Geometry_Dewarping), [DocRes](https://github.com/ZZZHANG-jx/DocRes), and others for their excellent work and open-source code.

#### Citation
If our methods and code are helpful to you, please refer to the following BibTeX format for citation:

```text
@article{li2025dual,
  title={Dual Dimensions Geometric Representation Learning Based Document Dewarping},
  author={Li, Heng and Chen, Qingcai and Wu, Xiangping},
  journal={arXiv preprint arXiv:2507.08492},
  year={2025}
}
```