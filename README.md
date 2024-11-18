# PII-Data-Detection
[competition](https://www.kaggle.com/competitions/pii-detection-removal-from-educational-data)
## team & result
![image](https://github.com/tsebaka/PII-Data-Detection/assets/78146236/985ead9c-2277-44af-8d4c-88d6122783d4)

## solution details
* Achievable speedup ranges from 30% for smaller models to up to 200% for larger models.
* All PyTorch-based models are supported, including Custom PyTorch, PyTorch Lightning, Transformers, etc.
* Models are converted and quantized to BFLOAT16 ONNX format.
* The converted models boast a 2x smaller memory footprint compared to FP32.
* There's only a minor performance degradation, typically fixable with a proper threshold adjustment.
* Conversion is done on-the-fly for all models. Models can be saved from the output and reused by passing conversion steps.
* Speed-up functionality is optimized for T4 Kaggle cards.
* Issues like timeouts and memory errors for larger models are resolved. An undocumented ONNX conversion method is utilized for files >2GB, splitting models into two parts (.onnx, .data).
* It's recommended to pin this notebook environment and transfer other models here due to fixed libraries set for GPU-ONNXRuntime and the converter. Changes in Kaggle's environment may disrupt functionality.
* Warnings can be disregarded as the system operates smoothly.
* Only one model type is available due to the tokenizer used.
* Testing can be conducted on train folds.

## how to run (data_get.sh and scripts soon)
* run notebook solution.ipynb
