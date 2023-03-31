# Folder sructure

<table>
  <thead>
    <tr>
      <th width="15%">Folder</th>
      <th>Description</th>
      <th width="30%">Sub-Folders/Files</th>
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
      <td>Contains the <code>.pth</code> file of a pretrained $\textbf{FPN-ResNet18}$ model within which the $\textbf{MSE loss}$ values of the model are saved.
      </td>
      <td>
        <img src="/img/icon_file_config.png" width="10%"><code>fpn_resnet_18_epoch_300.pth</code>
      </td>
    </tr>
    <tr>
      <td>📁<code>utils</code></td>
      <td>Contains useful utility tools which help to calculate the :
        <li> Evaluation metrics
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



