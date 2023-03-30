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

# CNN Models
<table>
  <thead>
    <tr>
      <th>Model</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>$\textbf{Darknet}$</td>
      <td>
      <li> An open source neural network (NN) framework which is fast and highly accurate (accuracy for custom trained model depends on training data, epochs, batch size and other factors) framework for real time object detection (also can be used for images). It is fast because it is written in $\textbf{C}$ and $\textbf{CUDA}$.
      </td>
    </tr>
    <tr>
      <td>$\textbf{ResNet}$</td>
      <td>
      <li> A deep convolutional neural network (CNN) architecture that uses $\textbf{residual (skip) connections}$ to enable the training of very deep networks.
      <li> In object detection, a $\textbf{ResNet}$ model is typically used as a $\textbf{backbone}$ network to $\textbf{extract features}$ from an input image, which are then fed into an object detection $\textbf{head}$ (here, the $\textbf{Complex-YOLOv4}$ model) to predict $\textbf{bounding boxes (bb)}$ and $\textbf{class labels}$ for objects in the image.
      </td>
    </tr>
  </tbody>
</table>
