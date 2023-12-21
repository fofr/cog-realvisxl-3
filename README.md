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
