# VRDL HW4

## 1. Install dependencies
Install required libraries.

```
pip install -r requirements.txt
```

## 2. Training code
Train IMDN model by following command.
* root: the training data directory
* scale: scale factor
* nEpochs: total epochs
* step_size: learning rate descreased every step epoch

```
python train_IMDN.py --root train_decoded/ --scale 3 -nEpochs 200 --step_size 50
```
## 3. Pre-trained models
The pretrained model is in [checkpoint_x3](https://github.com/gyes00205/VRDL_HW4/tree/main/checkpoint_x3). You clone the whole github to inference.

## 4. Inference code
You can reproduce the results by the following command.
* test_lr_folder: testing data directory
* output_folder: output directory
* checkpoint: model weights
* upscale_factor: upscale faactor

```
python inference.py  \
--test_lr_folder testing_lr_images/ \
--output_folder results_16epoch \
--checkpoint checkpoint_x3/epoch_16.pth \
--upscale_factor 3
```



## Result
* **Low reaolution images**\
![](https://i.imgur.com/c59mclo.png)

* **High resolution images (IMDN)**\
![](https://i.imgur.com/62SsEJy.png)


## Reference
1. IMDN: https://github.com/Zheng222/IMDN
2. IMDN paper: https://arxiv.org/pdf/1909.11856v1.pdf
3. VDSR: https://github.com/twtygqyy/pytorch-vdsr
4. Seven ways to improve example-based single image super resolution,  https://arxiv.org/abs/1511.02228