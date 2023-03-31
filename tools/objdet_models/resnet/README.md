# Folder sructure

<table>
  <thead>
    <tr>
      <th width="15%">Folder</th>
      <th>Description</th>
      <th>Sub-Folders/Files</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>📁<code>models</code></td>
      <td>Contains all the files and folders required to implement this model.</td>
      <td>
      <img src="/img/icon_python.png" width="10%"><code>fpn_resnet.py</code>
      <br>
      <img src="/img/icon_python.png" width="10%"><code>resnet.py</code>
      </td>
    </tr>
    <tr>
      <td>📁<code>pretrained</code></td>
      <td>Contains <code>.cfg</code> and <code>.pth</code> files of a pretrained $\textbf{Complex-YOLOv4}$ model within which the $\textbf{configurations}$ and $\textbf{MSE loss}$ values of the model are saved, respectively.
      </td>
      <td>
        <img src="/img/icon_file_config.png" width="10%"><code>fpn_resnet_18_epoch_300.pth</code>
      </td>
    </tr>
    <tr>
      <td>📁<code>utils</code></td>
      <td>Contains useful utility tools which help to calculate the :
        <li> Intersection of rotated boxes
        <li> Evaluation metrics
        <li> $\textbf{Intersection of Union (IoU)}$ of rotated boxes
        <li> PyTorch utilities
      </td>
      <td>
      <img src="/img/icon_python.png" width="10%"><code>evaluation_utils.py</code>
      <br>
      <img src="/img/icon_python.png" width="10%"><code>torch_utils.py</code>
      </td>
    </tr>
  </tbody>
</table>



