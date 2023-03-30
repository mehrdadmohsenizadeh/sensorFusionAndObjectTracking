# Folder Structure
<table>
  <thead>
    <tr>
      <th width="18%">Folder</th>
      <th width="52%">Description</th>
      <th>Sub-Folders/Files</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>📁<code>objdet_models</code></td>
      <td>Contains the $\textbf{object detection models}$ used in this project (i.e., $\textbf{Darknet}$ and $\textbf{ResNet}$).</td>
      <td>
      📁<code>darknet</code>
      <br>
      📁<code>resnet</code>
      </td>
    </tr>
    <tr>
      <td>📁<code>waymo_reader</code></td>
      <td>
      <li> A simple file reader for the <a href="https://waymo.com/open/">Waymo Open Dataset</a> which does not depend on <code>tensorFlow</code> and <code>bazel</code> .
      <li> The main goal is to be able to quickly integrate Waymo’s dataset with other deep learning frameworks without having to pull tons of dependencies (i.e., libraries and packages such as <code>tensorflow</code> ).
      <li> It does not aim to replace the <a href="https://github.com/waymo-research/waymo-open-dataset">whole framework</a>, especially the $\textbf{evaluation metrics}$ that they provide.
      </td>
      <td>
      📁<code>build</code>
      <br>
      📁<code>dist</code>
      <br>
      📁<code>simple_waymo_open_dataset_reader</code>
      <br>
      <img src="../img/icon_shell.png" width="8%"><code>generate_proto</code>
      <br>
      <img src="../img/icon_file.png" width="8%"><code>LICENSE.md</code>
      <br>
      <img src="../img/icon_file.png" width="8%"><code>README.md</code>
      <br>
      <img src="../img/icon_python.png" width="8%"><code>setup.py</code>
      </td>
    </tr>
  </tbody>
</table>
