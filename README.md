
# Invertible Scattering Transform Project

## Overview

This project extends the functionality of the scattering transform by introducing the concept of an **invertible scattering transform**, the extension is done on the existing Kymatio libary (https://github.com/kymatio/kymatio). The project also  offers examples for various applications such as classification and texture reconstruction.

## Folder Structure

- **`coefficients_plot/`**: Contains user-generated plots from the `plot_scattering_frequencies.py` script in the `kymatio-main/examples/2d` folder, visualizing the frequencies of the coefficients obtained from the scattering transform.
- **`kymatio-main/`**: Includes the main Kymatio library where modifications were made:
  - **`kymatio/`**: This folder contains the core changes to support the invertible scattering transform.
  - **`examples/`**: This folder contains example scripts demonstrating the use of the invertible scattering transform, including MNIST classification and visualization.
- **`texture_reconstruction/`**: This folder contains modified code for texture reconstruction, using coefficients generated by the `invertibleScattering2d` function.

## Usage Instructions

### `coefficients_plot` Folder
This folder contains user-generated plots, visualizing the frequencies of the coefficients from the scattering transform.

- The plots are created by running the `plot_scattering_frequencies.py` script in the `kymatio-main/examples/2d` folder.
- The resulting plots are stored as output in this folder.

### `kymatio-main` Folder

This folder includes the modifications to the Kymatio library:
1. **`kymatio/`**: The core changes are in the `scattering2d.py` file where the `invertibleScattering2d` function is added, allowing users to select between the original and invertible scattering transforms.
2. **`examples/2d`**: This folder contains examples demonstrating the use of the invertible scattering transform here we describe the scripts we changed or modified from the Kymatio libary:
   - **`check_non_expensiveness.py`**: Assesses the non expensivness property of the invertible scattering transform.
   - **`plot_scattering_frequencies.py`**: Visualizes the frequencies of the coefficients obtained from the invertible scattering transform.
   - **`long_mnist_classify_torch.py`**: Uses the invertible scattering transform for classifying the MNIST dataset with PyTorch.
   - - **`cifar_torch.py`**: Uses the invertible scattering transform for classifying the CIFAR-10 dataset with PyTorch.

### `texture_reconstruction` Folder

This folder contains modified code based on https://github.com/mariaprat/scattering for texture reconstruction, using the coefficients generated by the `invertibleScattering2d` function.

#### Usage:
 **Run Texture Reconstruction**:  The output will be stored as synthesized texture images in the `texture_reconstruction/synthesized_textures` directory.

### More information
For more information about the invertible scattering transform , and the code in this project can be found the following document: Invertible Scattering Transform.pdf

### Credits:
* Andreux M., Angles T., Exarchakis G., Leonarduzzi R., Rochette G., Thiry L., Zarka J., Mallat S., Andén J., Belilovsky E., Bruna J., Lostanlen V., Chaudhary M., Hirn M. J., Oyallon E., Zhang S., Cella C., Eickenberg M. (2020). Kymatio: Scattering Transforms in Python. Journal of Machine Learning Research 21(60):1−6, 2020

* https://github.com/kymatio/kymatio

* https://github.com/mariaprat/scattering

