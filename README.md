# pokemon-GAN
Realization of GAN using Pokemon Dataset

TensorFlowGAN.ipynb - is a file which is realized first version of my GAN. This version uses full sized images. Realization is inspired by DCGAN. Many of DCGAN features are included.

TensorFlowGAN-2.ipynb - is file which is realized second version of my GAN. This version uses 128-by-128 resolution of images. Realization also inspired by DCGAN but a lot of new features were added. There features are several Dropout layers in Genereation Network, GaussianNoise layers at each layer. Also some noise is added to images when Discriminator gets images. Also in this version data augmentation was added (fliping and rotation of images). Ungortunately this version haven't its training yet.

Each file has its own parts. They all pointed using Headers.

First part of every version is sterted with module imports. Then data augmentation is going in version 2. After this data is loaded and hyperparameters are initialized. At the part "Create the model" generator('make_generator_model') and discriminator('make_discriminator_model) functions are defined. Next part is defining the loss and optimizers for discriminator('discriminator_loss') and generator('generator_loss'). In this part the final chapter is checkpoints to get last weights if model has stopped by some reason. Final part is defining the training loop. First of all its hyperparameters are initialized. Then random seed is generated to future visualization of images evolution. This part has not been realized. Then train step('train_step') is defined and main function('train) which train the model. The function 'generate_and_save_images' shows generated imaged and save them to future visualization of progress.

To generate image first of all you should get trained model of the generated. After this you can simply call this object with random noise as argument

Many of features have not been added and a lot of hyperparameters have not been added due to lack of time. The main problem is time of training the model. GPU version of tensorflow and trying of optimize training process helped but not really mucb. There a lot improvements to involve so it is just matter of time. 

Second version changes were taken according to this article: https://github.com/soumith/ganhacks.

Also I know one person's realization of this GAN which was trained during mode time. But I decided to create my own model that could in future beat this model.

Example of pokemon generation:

![alt text](https://github.com/GeorgeFucker/pokemon-GAN/blob/master/image_at_epoch_1214.png)
