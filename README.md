# lora-vast-ai
This repo is for documentation purposes.

## Getting Started
Prerequisistes:
- vast.ai account
- 10-15 images
- labels with descriptions as txt files (in txt labels I always used "[trigger]")


### Training
Start a vast.ai container with enough GPU ram. At least for vast.ai it was helpful to use directly a pytorch template with cuda installed. For the installation follow the [instructions](https://github.com/ostris/ai-toolkit) for FLUX.1 Training. 

I needed to install another package:

```
sudo apt-get update
sudo apt-get install libgl1-mesa-glx -y
```

My repo uses the flux schnell weights.

#### data structure

```root/
└── ai-toolkit/
    └── dataset/
        ├── image-1.jpg
        ├── image-1.txt
        ├── image-2.jpg
        ├── image-2.txt
        ├── ...
      └── .../
```
At least for me with around 10-15 images it took me around 3 hours to train the lora models (with around 4 epochs).

### Inference
For the inference I used another [ComfyUI FLUX.1 on Vast.ai](https://cloud.vast.ai/?ref_id=31110&creator_id=31110&name=ComfyUI%20FLUX.1).

It takes a while until you can access the workflow UI (~ around 5-10 minutes). After that, you can just upload the workflow.json file from this repo and start creating new images with your own prompts.


## Acknowledgments  

Big thanks to [ostris](https://github.com/ostris) for creating [ai-toolkit](https://github.com/ostris/ai-toolkit).
