# Folder sructure


<table>
  <thead>
    <tr>
      <th>Folder</th>
      <th>Description</th>
      <th>Sub-Folders/Files</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>📁<code>darknet</code></td>
      <td>Contains all the files and folders required to implement this model.</td>
      <td>
      📁<code>__MACOSX</code>
      <br>
      📁<code>config</code>
      <br>
      📁<code>models</code>
      <br>
      📁<code>pretrained</code>
      <br>
      📁<code>utils</code>
      </td>
    </tr>
    <tr>
      <td>📁<code>resnet</code></td>
      <td>Contains all the files and folders required to implement this model.</td>
      <td>
      📁<code>models</code>
      <br>
      📁<code>pretrained</code>
      <br>
      📁<code>utils</code>
      </td>
    </tr>
  </tbody>
</table>

# Object Detection (CNN) Models
<table>
  <thead>
    <tr>
      <th>Model</th>
      <th width="78%">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>$\textbf{Darknet}$<br>(with $\textbf{Complex-YOLOv4}$)</td>
      <td>
      <li> An open source neural network (NN) framework which is fast and highly accurate (accuracy for custom trained model depends on training data, epochs, batch size and other factors) framework for real time object detection (also can be used for images). It is fast because it is written in $\textbf{C}$ and $\textbf{CUDA}$.
      <li> The $\textbf{Complex-YOLOv4}$ model adds complexity to the standard $\textbf{YOLOv4}$ model by incorporating more feature extraction modules, including the $\textbf{CSPDarknet53 backbone}$ and $\textbf{Spatial Attention Module}$, to improve detection accuracy. However, it is still built on the same architecture as YOLOv4, which consists of a $\textbf{backbone}$ network, $\textbf{neck}$, and $\textbf{head}$.
      <li> In object detection, a $\textbf{ResNet}$ model is typically used as a $\textbf{backbone}$ network to $\textbf{extract features}$ from an input image, which are then fed into an object detection $\textbf{head}$ (here, the $\textbf{Complex-YOLOv4}$ model) to predict $\textbf{bounding boxes (bb)}$ and $\textbf{class labels}$ for objects in the image.
      </td>
    </tr>
    <tr>
      <td>$\textbf{FPN-ResNet}$</td>
      <td>
      <li> A deep neural network architecture that combines two popular convolutional neural networks (CNNs):$
        <ol>
        <li> $\textbf{ResNet}$: A deep CNN architecture that introduces the concept of $\textbf{residual blocks}$ and $\textbf{residual (skip) connections}$, which help to alleviate the $\textbf{vanishing gradient problem}$ during training.
        <li> $\textbf{FPN}$: A $\textbf{feature extraction}$ architecture that enhances the feature representation of an input image by using a pyramid of multi-scale feature maps.
        </ol>
      <li> The $\textbf{FPN-ResNet}$ model takes advantage of the strengths of both architectures to improve $\textbf{object detection}$ and $\textbf{semantic segmentation}$ tasks. In this architecture:
        <ol>
        <li>
        The $\textbf{ResNet}$ is used as the $\textbf{backbone}$ network, which extracts the features of the input image.
        </li>
        <li>
        Then, the $\textbf{FPN}$ is applied to these features to create a $\textbf{pyramid of feature maps}$ with different resolutions.
        </li>
        <li>
        Finally, These pyramid of feature maps are used for object detection or semantic segmentation tasks.
        </li>
        </ol>
      </li>
      </td>
    </tr>
  </tbody>
</table>
