# Image-dataset Generator
It uses [PIL](https://pillow.readthedocs.io/en/stable/), Python's imaging library to create a large dataset with great variations (contrast, brightnes, color balance, saturation etc) from few images.

### Installation
- Create a virtual environment and install the requirements
```
    pip install -r requirements.txt
```

### Usage
- Create a folder with different category folders inside it, and place the images in 'bright' / 'dim' / 'normal' folders depending upon the quality of image.
*NOTE: If you are unsure about the quality, just place them in the same folder - **normal**. You can also skip some folders but at least one of the type-folders is must!*
```
    Fruit_images
    ├───Apple
    │   ├───bright
    │   ├───dim
    │   └───normal
    ├───Banana
    │   ├───bright
    │   └───dim
    ├───Orange
    │   ├───bright
    │   └───normal
    └───Papaya
        └───normal
```
- **data** folder is created inside the same source_folder with following structure
```
    Fruit_images
    ├───Apple
    │   ├───bright
    │   ├───dim
    │   └───normal
    ├───Banana
    │   ├───bright
    │   └───dim
    ├───data
    │   ├───train
    │   │   ├───Apple
    │   │   ├───Banana
    │   │   ├───Orange
    │   │   └───Papaya
    │   └───validation
    │       ├───Apple
    │       ├───Banana
    │       ├───Orange
    │       └───Papaya
    ├───Orange
    │   ├───bright
    │   └───normal
    └───Papaya
        └───normal
```
- Use the following commands to generate the images
```
    # python image_gen.py <src_folder> --ratio <validtion_data>
    # Run 'python image_gen.py -h' for more information
    python image_gen.py Fruit_images --ratio 0.25
```