# Folder sructure


<table>
  <thead>
    <tr>
      <th width="15%">Folder</th>
      <th>Description</th>
      <th width="33%">Sub-Folders/Files</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>📁<code>__MACOSX</code></td>
      <td>Contains the <code>pre-trained</code> folder for the $\textbf{Mac OS X}$ users.</td>
      <td>📁<code>pretrained</code></td>
    </tr>
    <tr>
      <td>📁<code>config</code></td>
      <td>Contains a <code>.cfg</code> file that sets different configurations for the $\textbf{Complex-YOLOv4}$ model.</td>
      <td><img src="/img/icon_file_config.png" width="10%"><code>complex_yolov4.cfg</code></td>
    </tr>
    <tr>
      <td>📁<code>models</code></td>
      <td>Contains all the files and folders required to implement this model.</td>
      <td>
      <img src="/img/icon_python.png" width="10%"><code>darknet_utils.py</code>
      <br>
      <img src="/img/icon_python.png" width="10%"><code>darknet2pytorch.py</code>
      <br>
      <img src="/img/icon_python.png" width="10%"><code>yolo_layer.py</code>
      </td>
    </tr>
    <tr>
      <td>📁<code>pretrained</code></td>
      <td>Contains <code>.cfg</code> and <code>.pth</code> files of a pretrained $\textbf{Complex-YOLOv4}$ model whithin which the $\textbf{configurations}$ and $\textbf{MSE losses}$ are saved, respectively.
      </td>
      <td>
        <img src="/img/icon_file_config.png" width="10%"><code>complex_yolov4.cfg</code>
        <br>
        <img src="/img/icon_file_config.png" width="10%"><code>complex_yolov4_mse_loss.pth</code>
      </td>
    </tr>
    <tr>
      <td>📁<code>utils</code></td>
      <td>Contains useful utility tools which help to calculate:
        <li> intersection of rotated boxes
        <li> Evaluation metrics
        <li> $\textbf{Intersection of Union (IoU)}$ of rotated boxes
        <li> PyTorch utilities
      </td>
      <td>
      <img src="/img/icon_python.png" width="10%"><code>cal_intersection_rotated_boxes.py</code>
      <br>
      <img src="/img/icon_python.png" width="10%"><code>evaluation_utils.py</code>
      <br>
      <img src="/img/icon_python.png" width="10%"><code>iou_rotated_boxes_utils.py</code>
      <br>
      <img src="/img/icon_python.png" width="10%"><code>torch_utils.py</code>
      </td>
    </tr>
  </tbody>
</table>


