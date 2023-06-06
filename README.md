Sure, here's a version of the README tailored for your WeaveFormer model:

```markdown
## Towards Robust Hair Weave Detection and Repair with WeaveFormer

**Paper | Project Page | Video**

S-Lab, Nanyang Technological University
**Micah Berkley**

⭐ If WeaveFormer is helpful to your projects, please star this repo. Thanks! 🤗

## Updates

* 2023.04.19: 🐳 Training codes and config files are public available now.
* 2023.04.09: Add features of detection and repair for various weave types.
* 2023.02.10: Include additional weave detectors, producing more accurate detection and restoration.
* 2022.10.05: Support image input for various weave types. Try it to enhance your weave detection and restoration! 🖼️
* 2022.09.14: Integrated to 🤗 Hugging Face. Try out online demo! Hugging Face
* 2022.09.09: Integrated to 🚀 Replicate. Try out online demo! Replicate

## TODO
 * Add training code and config files
 * Add checkpoint and script for hair weave detection and repair
 * Add checkpoint and script for deep wave detection and restoration
 * Add background image enhancement
 * 🐼 Try Enhancing Old Photos / Fixing AI-arts
  

## Hair Weave Detection and Repair
   

## Deep Wave Detection and Restoration
 

## Dependencies and Installation
* Pytorch >= 1.7.1
* CUDA >= 10.1
* Other required packages in requirements.txt

```shell
# git clone this repository
git clone https://github.com/micahberkley/WeaveFormer
cd WeaveFormer

# create new anaconda env
conda create -n weaveformer python=3.8 -y
conda activate weaveformer

# install python dependencies
pip3 install -r requirements.txt
python basicsr/setup.py develop
```

## Quick Inference
### Download Pre-trained Models:
Download the pretrained models from [Releases | Google Drive | OneDrive] to the `weights/WeaveFormer` folder. You can manually download the pretrained models OR download by running the following command:

```shell
python scripts/download_pretrained_models.py WeaveFormer
```

### Prepare Testing Data:
You can put the testing images in the `inputs/TestWhole` folder. If you would like to test on specific weave types, you can put them in the `inputs/specific_weave` folder.

### Testing:
Fidelity weight w lays in [0, 1]. Generally, smaller w tends to produce a higher-quality result, while larger w yields a higher-fidelity result. The results will be saved in the `results` folder.

```shell
python inference_weaveformer.py --input_path [image folder]|[image path]
```

## Training:
The training commands can be found in the documents: English | 简体中文.

## Citation
If our work is useful for your research, please consider citing:

```shell
@inproceedings{berkley2023weaveformer,
    author = {Berkley, Micah},
    title = {Towards Robust Hair Weave Detection and Repair with WeaveFormer},
    booktitle = {To be published},
    year = {2023}
}
```

## License
This project is licensed under NTU S-Lab License 1.0. Redistribution and use should follow this license.

## Acknowledgement
This project is based on BasicSR. Some codes are brought from Unleashing Transformers, YOLOv5-face, and FaceX