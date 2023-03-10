PKGAN

This is a code for training a Progressive Generative Adversarial Network (PKGAN) to generate images of size 64x64 using the ImageFolder dataset and PyTorch.
Requirements

    PyTorch
    torchvision
    tqdm
    matplotlib
    cv2
    numpy

Usage

    Set the DATA_DIR variable to the path of your dataset.
    Run the code.
    The generated images will be displayed using matplotlib.

Model architecture

The model consists of a discriminator and a generator. The discriminator is a convolutional neural network that classifies images as real or fake. The generator is responsible for generating new images that can fool the discriminator.

Training

The code uses the LeakyReLU activation function and the Adam optimizer. The training is done by alternating the training of the generator and the discriminator. The images generated by the generator during training will be displayed using matplotlib.

Note

    The code uses the GPU if available, otherwise it falls back to the CPU.
    The show_batch function can be used to display a random batch of images from the dataset.

Dataset

The code uses the ImageFolder dataset and applies some image preprocessing such as resizing, cropping and normalization on the images.

Dataset here:

https://drive.google.com/file/d/1ytNT1GTykzQy50_zvS4T2OwBsx2Y_Q0c/view?usp=share_link


Full Training Loop



![6NMdO9u](https://user-images.githubusercontent.com/94846393/213864088-aa9bfb78-5823-40cc-bfc6-d41da3fd936e.png)



Additional Information

    The code uses the torch.utils.data.DataLoader for loading the data and dividing it into batches.
    The code uses torchvision.transforms to apply data preprocessing techniques such as resizing, cropping and normalization on the images.
    The show_images function is used to display the generated images using matplotlib.
    The get_default_device function is used to select the GPU if available, otherwise it falls back to the CPU.
    The to_device function is used to move the data to the selected device (GPU or CPU).
    The DeviceDataLoader class is used to wrap the dataloader and move the data to the selected device.

Conclusion

This is a basic implementation of a Progressive Generative Adversarial Network (PKGAN) for generating images of size 64x64. The code can be further modified and improved to achieve better results, such as by changing the architecture of the generator and discriminator, training for more epochs, or fine-tuning the hyperparameters.

