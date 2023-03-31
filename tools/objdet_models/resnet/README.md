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
      <td>Contains all the files and folders required to implement the $\textbf{FPN-ResNet18}$ model.</td>
      <td>
      <img src="/img/icon_python.png" width="10%"><code>fpn_resnet.py</code>
      <br>
      <img src="/img/icon_python.png" width="10%"><code>resnet.py</code>
      </td>
    </tr>
    <tr>
      <td>📁<code>pretrained</code></td>
      <td>Contains the <code>.pth</code> file of a $\textbf{FPN-ResNet18}$ model, pre-trained for $300$ epochs .
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

# What is a <code>.pth</code> file?
<li>
  In PyTorch, a <code>.pth</code> file is a file extension used for saving and loading trained models. When you train a neural network model in PyTorch, the parameters (weights and biases) of the model are updated during training. Once the training is complete, you can save the state of the model, including the trained parameters, to a <code>.pth</code> file.
</li>
<li>
  This file can be used to reload the trained model later for making predictions or continuing training. It contains the values of the model's parameters and can be loaded into a PyTorch model using the <code>torch.load()</code> function. The <code>torch.load()</code> function returns a Python dictionary that contains the saved state of the model. 
</li>
