
# Towards Robust Hair Weave Detection and Repair with WeaveFormer

## Introducing WeaveFormer: AI-Powered Hair Weave Detection and Restoration

WeaveFormer is an advanced AI model designed to revolutionize the hair care industry. With its cutting-edge technology, WeaveFormer can accurately identify various weave types, detect the installation style (e.g., frontal, sew-in), determine the average length of the hair, and pinpoint installation faults or hair degradation. By leveraging its powerful algorithms, WeaveFormer can seamlessly restore poorly installed or degraded hair weaves to a high-quality state, providing a comprehensive solution for both professionals and individuals.

With WeaveFormer, you can trust that the model's generative capabilities will ensure exceptional results when repairing hair weave installations. Whether it's addressing flaws in the installation technique or rejuvenating degraded hair, WeaveFormer's AI-powered restoration process guarantees a visually appealing and natural-looking outcome. Say goodbye to poorly installed weaves and hello to flawlessly restored hairstyles with WeaveFormer.

## Model Description

This AI model, WeaveFormer, is implemented in PyTorch. It leverages a transformer-based prediction network that has been trained on an expansive collection of synthetic and real-world hair weave datasets. The model excels in detecting and digitally repairing poor weave installations and also features a controllable feature transformation module. This module ensures adaptability to a range of weave degradation levels and various hair textures, achieving an excellent balance between fidelity and restoration quality. The model is a collaborative product of a team of AI researchers and hair care experts.

## Intended Use

WeaveFormer is designed to be a valuable resource for individuals and professionals in the hair care industry. Its primary application is to assist in detecting and repairing poorly installed weaves. Additionally, it can serve as a valuable learning tool for stylists by providing visual feedback and suggestions for improving their weave installations. Hair weave manufacturers can also use WeaveFormer to assess and enhance the quality of their products.

## Ethical Considerations

While WeaveFormer provides an innovative solution for detecting and repairing hair weaves, it's important to note that it may not always provide accurate results for all types of weaves or predict the optimal solution for all weave repairs. The model's results should be used as guidance and be interpreted alongside professional advice. Moreover, user privacy and consent are vital. Users must be adequately informed about and provide their consent for their hair images to be used for the model's operation.

## Caveats and Recommendations

For best results, we recommend using high-resolution images that clearly display the hair weave. Factors such as image blur, extreme lighting conditions, or obscured views of the weave may affect the model's performance. The model's results on complex weave installations should be interpreted with caution, and professional advice should always be sought in such cases.

**Paper | Project Page | Video**
  
**Micah Berkley**

⭐ If WeaveFormer is helpful to your projects, please star this repo. Thanks! 🤗

## Updates

* 2023.06.06: Add features of detection and repair for various weave types.
* 2023.06.01: Include additional weave detectors, producing more accurate detection and restoration.
* 2023.05.28: Support image input for various weave types. Try it to enhance your weave detection and restoration! 🖼️
* 2023.05.14: Integrated to 🚀 Replicate. Try out online demo! [Replicate](https://replicate.ai/)

## TODO
* Add training code and config files
* Add checkpoint and script for hair weave detection and repair
* Add checkpoint and script for deep wave detection and restoration
* Add background image enhancement
* 🐼 Try Enhancing Old Photos / Fixing AI-arts

## Hair Weave Detection and Repair

## Deep Wave Detection and Restoration

## Dependencies and Installation

* PyTorch >= 1.7.1
* CUDA >= 10.1
* Other required packages in requirements.txt

```shell
# Clone this repository
git clone https://github.com/micahberkley/WeaveFormer
cd WeaveFormer

# Create a new Anaconda environment
conda create -n weaveformer python=3.8 -y
conda activate weaveformer

# Install Python dependencies
pip3 install -r requirements.txt
python basicsr/setup.py develop


## Quick Inference

### Download Pre-trained Models:

Download the pretrained models from [Releases | Google Drive | OneDrive](https://github.com/micahberkley/WeaveFormer/releases) to the `weights/WeaveFormer` folder. You can manually download the pretrained models OR download by running the following command:

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

## Citation

If our work is useful for your research, please consider citing:

```shell
@inproceedings{berkley2023weaveformer,
    author = {Berkley, Micah},
    title = {Towards Robust Hair Weave Detection and Repair with WeaveFormer},
    year = {2023}
}
```

## License
``` coming soon ```

## Acknowledgement

This project is based on BasicSR. Some codes are brought from Unleashing Transformers, YOLOv5-face, and FaceX
```

You can copy and paste the above markdown into your readme.md file on GitHub.
