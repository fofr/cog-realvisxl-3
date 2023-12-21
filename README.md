# cog-realvisxl-3

[![Replicate demo and cloud API](https://replicate.com/fofr/realvisxl-v3/badge)](https://replicate.com/fofr/realvisxl-v3)

Run on Replicate:
https://replicate.com/fofr/realvisxl-v3

An SDXL full model tune aimed at photorealism:
https://huggingface.co/SG161222/RealVisXL_V3.0

## Development

Follow the [model pushing guide](https://replicate.com/docs/guides/push-a-model) to push your own fork of SDXL to [Replicate](https://replicate.com).

## Basic Usage

for prediction,

```bash
cog predict -i prompt="a photo of TOK"
```

```bash
cog train -i input_images=@example_datasets/__data.zip -i use_face_detection_instead=True
```

```bash
cog run -p 5000 python -m cog.server.http
```

## Update notes

**2023-08-17**
* ROI problem is fixed.
* Now BLIP caption_prefix does not interfere with BLIP captioner.


**2023-08-12**
* Input types are inferred from input name extensions, or from the `input_images_filetype` argument
* Preprocssing are now done with fp16, and if no mask is found, the model will use the whole image

**2023-08-11**
* Default to 768x768 resolution training
* Rank as argument now, default to 32
* Now uses Swin2SR `caidas/swin2SR-realworld-sr-x4-64-bsrgan-psnr` as default, and will upscale + downscale to 768x768
