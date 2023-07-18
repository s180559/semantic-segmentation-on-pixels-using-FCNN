![fcnnn2](https://github.com/s180559/semantic-segmentation-on-pixels-using-FCNN/assets/111356869/e9130389-4b36-4d13-8eea-253df64163bb)
![Uploading fcnn1.png…]()
![Uploading fcnn.png…]()
# semantic-segmentation-on-pixels-using-FCNN
The problem at hand is the lack of accurate and precise semantic segmentation for road and lane images. Existing methods struggle to classify individual pixels effectively, resulting in inaccurate segmentation and limited understanding of road scenes. This poses challenges in domains like autonomous driving, where reliable segmentation is essential for object detection and obstacle avoidance. The objective of this project is to develop a semantic segmentation model that accurately classifies pixels in road and lane images while effectively addressing these challenges. The aim is to enhance understanding and enable improved autonomous driving systems and other applications relying on precise image segmentation.
![image](https://github.com/s180559/semantic-segmentation-on-pixels-using-FCNN/assets/111356869/dbea50ce-f72e-4612-ba4e-2a59b8ba11c5)
# Proposed system
The proposed system introduces fully convolutional networks (FCNs) as an improvement over the existing system. FCNs convert classification networks into dense prediction models by transforming fully connected layers into convolutional layers. This allows the network to accept inputs of any size and produce spatially dense prediction maps. 

The proposed system incorporates skip connections to combine information from different layers, enabling the refinement of segmentation output at various scales. The FCN architecture allows for efficient end-to-end learning for dense prediction tasks, such as semantic segmentation. 
![image](https://github.com/s180559/semantic-segmentation-on-pixels-using-FCNN/assets/111356869/98b44553-659b-4823-91fd-f6de537e49e5)
# Implementation
The implementation of Fully Convolutional Networks (FCNs) involves adapting existing classification networks by replacing their fully connected layers with convolutional layers to enable handling inputs of any size and producing dense classification maps. Skip connections are added to combine coarse semantic information from higher layers and local appearance information from lower layers. The shift-and-stitch trick is used to obtain dense predictions by downsampling the outputs, shifting the input image, applying convolution on multiple inputs, and interlacing the predictions. Upsampling is achieved by converting pooling layers to have an input stride of 1 and adjusting filters based on the upsampling factor. Patchwise training is employed by sampling patches within each image to create training batches, excluding certain patches from gradient computation to speed up learning, and correcting class imbalance. These techniques collectively enable accurate semantic segmentation for road and lane images.
![image](https://github.com/s180559/semantic-segmentation-on-pixels-using-FCNN/assets/111356869/416dafa7-9993-4f6a-a327-1c17643f2304)
