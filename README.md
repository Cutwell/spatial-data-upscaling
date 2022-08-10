# Spatial data upscaling
 Pipeline for augmenting sparse data for genetic optimisation

## Augmenting data in specific search space using large broad dataset
During data collection for genetic optimisation, available data may be broad instead of specific. Training a neural network on broad data can enable data collection for a specific search space at increased resolution. This pipeline suggests a method for training a model on a broad dataset, and applying it to generate data at a desired resolution for a specific search space.

| | | | | |
|:---:|:---:|:---:|:---:|:---:|
| ![](/.github/README/wind_world.png) | ![](/.github/README/wind_uk.png) | ![](/.github/README/wind_plot.png) | ![](/.github/README/wind_pred_plot.png) | ![](/.github/README/wind_zoomed.png) |
| Broad dataset has large amount of data.. | ..but is insufficient at specific search space. | The model wants to learn spatial features of the datset.. | ..and is able to predict similar data, suggesting it has learnt the dataset. | Using this model, we can generate high resolution data for our search space. |

## Blog post
Read about this project in further detail at [https://cutwell.github.io/neural-network-augmentation/](https://cutwell.github.io/neural-network-augmentation/).

## Pipeline
1. Follow `train_model.ipynb` to train a regression model.
2. View `run_model.ipynb` for ways to apply the regression model to predict wind data for the search space.
