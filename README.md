# CS6140-Machine-Learning-Final-Project
This repository contains the Jupyter and Colab notebooks for the final project of the CS6140 Machine Learning course. The project involves super-resolution modeling using SRCNN, with a particular focus on incorporating land cover (LC) data to enhance the model's performance. Below is an overview of each notebook in the repository, detailing its purpose and contents.

## Project Notebooks Overview

- **baseline_srcnn.ipynb**: This notebook contains the training and evaluation of the final baseline SRCNN model. The results, including PSNR and SSIM metrics, are thoroughly evaluated and documented.

- **download_land_cover.ipynb**: Initially used to download RGB land cover images. These images were explored and evaluated for their potential to improve the SRCNN model.

- **download_lc_images.ipynb**: The final notebook used to download single-channel land cover images, where each pixel's value represents a specific land cover class label.

- **downscaled_hr_as_input_srcnn.ipynb**: This notebook explores the impact of using downscaled high-resolution images as input for the baseline SRCNN model, assessing the results in terms of image quality improvement.

- **extract_high_psnr_lc.ipynb**: A notebook focused on extracting corresponding land cover images for high-quality low-resolution and high-resolution image pairs.

- **filter_out_high_psnr.ipynb**: Calculates the average PSNR of the cleaned dataset and filters out low-resolution and high-resolution image pairs that exceed this average, aiming to enhance the training data's overall quality.

- **land_cover_data_process.ipynb**: Processes and cleans the RGB land cover images, preparing them for integration with the SRCNN model.

- **plot_hr_and_lr.ipynb**: Tests and visualizes the handling and plotting of high-resolution and low-resolution images, ensuring that the processing methods are correctly implemented.

- **srcnn_split_image_test.ipynb**: Conducts tests on the effect of splitting images into smaller patches before inputting them into the SRCNN model for training.

- **srcnn_with_attention_map.ipynb**: Attempts to integrate the RGB land cover images with an attention mechanism in the SRCNN model, exploring potential improvements in model performance.

- **srcnn_with_lc.ipynb**: Trains and evaluates the final SRCNN model that incorporates land cover data. The notebook contains a detailed analysis of the results, comparing them with the baseline model.

- **test_srcnn_training.ipynb**: The initial attempt to combine RGB land cover images with the SRCNN model, serving as a proof-of-concept for later experiments.

## Non-Standard Python Libraries Used

- **rasterio**: Used for handling and processing geospatial raster data, particularly for reading and processing the TIFF format images used in the project.

- **opencv-python**: Employed for image processing tasks such as resizing and normalizing images before they are input into the model.

- **matplotlib**: Used extensively for visualizing model performance, including training histories, and comparing PSNR and SSIM metrics.

- **earthengine-api** (`ee`): The Google Earth Engine Python API allows users to interact with the Google Earth Engine platform, which provides access to a vast public archive of satellite imagery and other geospatial datasets. This API is used in the project for downloading and processing land cover images.
