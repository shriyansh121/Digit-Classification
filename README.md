# Digit-Classification
This repository consist of image processing code of digit classification. Here two approach is used first is using simple Dense layer and second one is Lenet. 

# LeNet Architecture

LeNet is a convolutional neural network (CNN) architecture that was developed by Yann LeCun and his colleagues in 1989. This architecture played a crucial role in demonstrating the potential of neural networks for image recognition tasks, especially in reading handwritten digits and characters. LeNet is considered one of the earliest examples of CNNs, which are now foundational to many modern artificial intelligence (AI) applications in image and video analysis. 



The structure of LeNet consists of multiple layers designed to automatically and efficiently recognize patterns in images. The network typically includes two sets of convolutional and pooling (sub-sampling) layers followed by fully connected layers. Convolutional layers apply various filters to the input images to create feature maps that summarize key features such as edges and shapes. Pooling layers then reduce the dimensions of these feature maps to make the processing more manageable and to help the network focus on the most important features. Finally, the fully connected layers compute the final classifications, such as identifying which digit is present in an image.

### LeNet Layer Size Calculations
Below are the detailed calculations for each layer in the LeNet architecture, starting from the input layer to the output layer.

#### Formula:
`n+2p-1/s`,
where 
- n=Size from previous layer, 
- p is padding,
- s is stride.

1. **Input Layer:**
   - Size: `32x32` (Assuming the input images are 32x32 in size)

2. **First Convolutional Layer (C1):**
   - Filter size: `5x5`
   - Stride: `1`
   - Number of filters: `6`
   - Output size: `(32 - 5 + 1) x (32 - 5 + 1) x 6 = 28x28x6`

3. **First Pooling Layer (S2):**
   - Pooling size: `2x2`
   - Stride: `2`
   - Type: Average pooling
   - Output size: `28/2 x 28/2 x 6 = 14x14x6`

4. **Second Convolutional Layer (C3):**
   - Filter size: `5x5`
   - Stride: `1`
   - Number of filters: `16`
   - Output size: `(14 - 5 + 1) x (14 - 5 + 1) x 16 = 10x10x16`

5. **Second Pooling Layer (S4):**
   - Pooling size: `2x2`
   - Stride: `2`
   - Type: Average pooling
   - Output size: `10/2 x 10/2 x 16 = 5x5x16`

6. **Fully Connected Layer (C5):**
   - This layer flattens the output of the previous layer and connects every neuron to 120 output neurons.
   - Output size: `120`

7. **Fully Connected Layer (F6):**
   - This layer connects the 120 neurons from the previous layer to 84 neurons.
   - Output size: `84`

8. **Output Layer:**
   - Typically a fully connected layer with a softmax activation function to classify into classes (e.g., 10 classes for digit recognition).
   - Output size: `10`


### Impact and Legacy of LeNet in Deep Learning 

LeNet was specifically designed to recognize handwritten postal codes on mail for automated sorting systems, a task at which it excelled. Its success showcased the practical applicability of neural networks in real-world tasks and inspired sfurther research and development in the field of deep learning.

The usage of LeNet has historically been a stepping stone to more complex and capable neural network architectures. Although modern networks like AlexNet, VGG, and ResNet have largely surpassed LeNet in performance, yet LeNet’s basic principles and design continue to influence the development of new neural network architectures today. LeNet serves as an educational tool for deep learning, providing a manageable yet illustrative example of how deep learning can be structured and implemented.
