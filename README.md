# Segmentation - Pretrained and Custom Procedure

In this section I have described , how to do Segmentation  in Computer vision .


## References

https://drive.google.com/drive/u/0/folders/1P7RffRtB7nhyVMtCWoxG9hLTgr_wrMWe
https://github.com/facebookresearch/detectron2

## Authors

- [@Jateendra](https://github.com/Jateendra)

## A ) Pretrained Images :


```bash

1 . URL : https://github.com/facebookresearch/detectron2 and open Colab notebook link from here .
2 . Change as below :

	# !pip install detectron2 -f https://dl.fbaipublicfiles.com/detectron2/wheels/$CUDA_VERSION/torch$TORCH_VERSION/index.html
	!python -m pip install 'git+https://github.com/facebookresearch/detectron2.git'

3 . **
	- tensor([17,  0,  0,  0,  0,  0,  0,  0, 25,  0, 25, 25,  0,  0, 24],device='cuda:0') - This many no. of classes , 0,0,0 are same classes .
	- [126.6035, 244.8977, 459.8291, 480.0000] - Polygon boxes in Semantic Segmentation , Bounding Boxes in Object Detection .

```

## B ) Custom Images :


```bash

1 . In Anaconda , go to location : C:\Users\jatpradh\Documents\CV\100_Image_Segmentation\Detectron2
	- python labelme2coco.py label_mask --output cons_file.json 
	- ** "label_mask" folder has all the images and their corressponding .json files .
	- ** you will have a "cons_file.json" file generated .
	- ** go to "categories": [ section and you will find 14 categories in total .
	- ** while training "images" folder and "trainval.json" file should be there .
	
2 . ** Make sure you have "images" folder ( only raw images ) and .json file for training .
3 . Open "ImageSegmentation_Detectron2_CustomTraining.ipynb" in google colab .

```
