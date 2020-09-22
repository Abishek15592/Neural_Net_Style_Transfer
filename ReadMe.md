# Neural Style Transfer

This is a project that involved implementation of a simple neural style transfer.

<b>Input</b> : A content image and a style image

<b>Output</b> : A stylized content image 

<b><i>Neural Style Transfer</i></b> is a process of generating a new image by retaining some features from content image by applying style from the style image.

For this project I'm using a VGG-19 model that is pre-trained on a large image dataset (Imagenet Dataset). The intermediate layers of the model work as feature detectors. And we use the output of the intermediate feature detectors of the content image and style image and compare it to those of stylized image to give us the content and style cost respectively. We then add the style and content cost to get the total cost. 

If we then run an optimization algorithm to minimize the total cost, the resulting solution would be an image that has style of the style image applied to the content image.

The VGG-19 model has 5 blocks with each block having some convolutional layer followed by a pooling layer.

<br>

# Steps for the project
<ol>
<li>Import the VGG Model</li><br>

    - Set include_top to false as we dont want the top layer. We dont want the output of the entire model but want the ouput of the intermediate layers.

    - And we also set the model.trainable to false as we don't want the model to update its parameters but just want to use it as such in our project.

    - Also run model.summary() to see the summary of the VGG-19 model.
<li> Importing other modules</li><br>

    - 