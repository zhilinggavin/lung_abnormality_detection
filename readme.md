# Automatic Lung Abnormalities Deetction
## Introduction
Automatically detects the counterfactual regions indicating lung abnormalities and highlights them using bounding boxes.

## Segmentation

You can load pretrained anatomical segmentation models. 
<!-- [Demo Notebook](scripts/segmentation.ipynb) -->

```python3
seg_model = xrv.baseline_models.chestx_det.PSPNet()
output = seg_model(image)
output.shape # [1, 14, 512, 512]
seg_model.targets # ['Left Clavicle', 'Right Clavicle', 'Left Scapula', 'Right Scapula',
                  #  'Left Lung', 'Right Lung', 'Left Hilus Pulmonis', 'Right Hilus Pulmonis',
                  #  'Heart', 'Aorta', 'Facies Diaphragmatica', 'Mediastinum',  'Weasand', 'Spine']
```

![](torchxrayvision_folder/docs/segmentation-pspnet.png)

## More details To Be Added Soon