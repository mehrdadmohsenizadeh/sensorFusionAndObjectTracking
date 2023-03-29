# sensorFusionAndObjectTracking
Udacity | Nanodegree (0013) - Self-Driving Car Engineer | Course - Sensor Fusion | Final Project
<!---------------------------------------------------------------------------------------------------------------------------------------------------------------->
<!---------------------------------------------------------------------------------------------------------------------------------------------------------------->
<!---------------------------------------------------------------------------------------------------------------------------------------------------------------->
<!--                                                                      INTRODUCTION                                                                          >
<!---------------------------------------------------------------------------------------------------------------------------------------------------------------->
<!---------------------------------------------------------------------------------------------------------------------------------------------------------------->
<!---------------------------------------------------------------------------------------------------------------------------------------------------------------->
## Introduction
* You can find this project in the [Udacity Self-Driving Car Engineer Nanodegree (SDCND)](https://www.udacity.com/course/self-driving-car-engineer-nanodegree--nd0013) Program, under the $\textbf{Sensor Fusion}$ course. It is called $\textbf{Final Project: Sensor Fusion and Tracking}$.

* In this project, you will:
  * Fuse measurements from $\textbf{LiDAR}$ with those from $\textbf{Camera}$ and track vehicles over time.
  * Use real-world data from the Waymo Open Dataset, detect objects in 3D point clouds and apply an extended Kalman filter for sensor fusion and tracking.

<img src="img/img_title_1.jpeg"/>

<!---------------------------------------------------------------------------------------------------------------------------------------------------------------->
<!---------------------------------------------------------------------------------------------------------------------------------------------------------------->
<!---------------------------------------------------------------------------------------------------------------------------------------------------------------->
<!--                                                                      OBJECTIVES                                                                              >
<!---------------------------------------------------------------------------------------------------------------------------------------------------------------->
<!---------------------------------------------------------------------------------------------------------------------------------------------------------------->
<!---------------------------------------------------------------------------------------------------------------------------------------------------------------->
## Objectives
This project can be divided into two main parts:

<table>
  <thead>
    <tr>
      <th>Section</th>
      <th>Objectives</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Object<br>detection</td>
      <td>
      1. Detecting vehicles in LiDAR data based on a $\textbf{Birds-Eye View (BEV)}$ perspective of the 3D $\textbf{Point-Cloud (PCL)}$, using a deep-learning approach.
      <br></br>
      2. Evaluating the performance of the detections, using a series of performance measures. 
      </td>
    </tr>
    <tr>
      <td>Object<br>tracking</td>
      <td>
      1. Tracking vehicles over time based on the LiDAR detections fused with camera detections, using an $\textbf{Extended Kalman}$ $\textbf{Filter (EKF)}$. 
      <br></br>
      2. Implementing $\textbf{data association}$ and $\textbf{track management}$.
      </td>
    </tr>
  </tbody>
</table>

The following diagram contains an outline of the data flow and of the individual steps that make up the algorithm. 

<img src="img/img_title_2_new.png"/>

Also, the project code contains various tasks, which are detailed step-by-step in the code. More information on the algorithm and on the tasks can be found in the Udacity classroom. 
<!---------------------------------------------------------------------------------------------------------------------------------------------------------------->
<!---------------------------------------------------------------------------------------------------------------------------------------------------------------->
<!---------------------------------------------------------------------------------------------------------------------------------------------------------------->
<!--                                                                      FILE STRUCTURE                                                                          >
<!---------------------------------------------------------------------------------------------------------------------------------------------------------------->
<!---------------------------------------------------------------------------------------------------------------------------------------------------------------->
<!---------------------------------------------------------------------------------------------------------------------------------------------------------------->
## Repo structure

* In this project, we will deal with different file formats (e.g., <code>.py</code>, <code>.tfrecord</code>, <code>.pkl</code>, <code>.proto</code>, <code>.png</code>, <code>.cfg</code>, <code>.pth</code>, <code>.dockerfile</code>).

* This repo contains the following directories and files:
> 💡 <b>Note:</b> Learn more about sub-directories and/or files of each directory by clicking on that directory and reading its <code>README.md</code> file.

<table>
  <thead>
    <tr>
      <th width="30%">Directories/Files</th>
      <th width="40%">Description</th>
      <th width="30%">Sub-directories/Files</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>📁<code>dataset</code></td>
      <td>Contains the <a href="https://console.cloud.google.com/storage/browser/waymo_open_dataset_v_1_2_0_individual_files;tab=objects?pli=1&prefix=&forceOnObjectsSortingFiltering=false&pageState=(%22StorageObjectListTable%22:(%22f%22:%22%255B%255D%22))">Waymo Open Dataset</a> sequences in the <code>.tfrecord</code> format.
      </td>
      <td>
       <img src="https://www.iconpacks.net/icons/2/free-file-icon-1453-thumb.png" width="10%"><code>.tfrecord</code><br>
       .<br>
       .<br>
       .<br>
       <img src="https://www.iconpacks.net/icons/2/free-file-icon-1453-thumb.png" width="10%"><code>.tfrecord</code><br>
       <img src="https://www.iconpacks.net/icons/2/free-file-icon-1453-thumb.png" width="10%"><code>README.md</code>  
      </td>
    </tr>
    <tr>
      <td>📁<code>img</code></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>📁<code>misc</code></td>
      <td></td>
      <td>
       <img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/267_Python-512.png" width="10%"><code>evaluation.py</code><br>
       <img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/267_Python-512.png" width="10%"><code>helpers.py</code><br>
       <img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/267_Python-512.png" width="10%"><code>objdet_tools.py</code><br>
       <img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/267_Python-512.png" width="10%"><code>params.py</code><br>
       <img src="https://www.iconpacks.net/icons/2/free-file-icon-1453-thumb.png" width="10%"><code>README.md</code>
     </td>
    </tr>
    <tr>
      <td>📁<code>results</code></td>
      <td>
      Contains binary (<code>.pkl</code>) files with pre-computed intermediate results.
      </td>
      <td>
      📁<code>results_sequence_1_resnet</code><br>
      📁<code>results_sequence_2_resnet</code><br>
      📁<code>results_sequence_3_resnet</code><br>
      <img src="https://www.iconpacks.net/icons/2/free-file-icon-1453-thumb.png" width="10%"><code>README.md</code>
      </td>
    </tr>
    <tr>
      <td>📁<code>student</code></td>
      <td></td>
      <td>
      <img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/267_Python-512.png" width="10%"><code>association.py</code><br>
      <img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/267_Python-512.png" width="10%"><code>filter.py</code><br>
      <img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/267_Python-512.png" width="10%"><code>measurements.py</code><br>
      <img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/267_Python-512.png" width="10%"><code>objdet_detect.py</code><br>
      <img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/267_Python-512.png" width="10%"><code>objdet_eval.py</code><br>
      <img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/267_Python-512.png" width="10%"><code>objdet_pcl.py</code><br>
      <img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/267_Python-512.png" width="10%"><code>trackmanagement.py</code><br>
      <img src="https://www.iconpacks.net/icons/2/free-file-icon-1453-thumb.png" width="10%"><code>README.md</code>
      </td>
    </tr>
    <tr>
      <td>
        📁<code>tools</code>
      </td>
      <td>
      Contains external tools.
      </td>
      <td>
       📁<code>objdet_models</code><br>
       📁<code>waymo_reader</code><br>
       <img src="https://www.iconpacks.net/icons/2/free-file-icon-1453-thumb.png" width="10%"><code>README.md</code>  
      </td>
    </tr>
    <tr>
      <td style="vertical-align: middle">
       <img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/267_Python-512.png" width="10%">
       <code>bsaic_loop.py</code>
     </td>
      <td></td>
      <td>-</td>
    </tr>
    <tr>
      <td style="vertical-align: middle">
       <img src="https://www.iconpacks.net/icons/2/free-file-icon-1453-thumb.png" width="10%">
       <code>LICENSE.md</code>
     </td>
      <td></td>
      <td>-</td>
    </tr>
    <tr>
      <td style="vertical-align: middle">
       <img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/267_Python-512.png" width="10%">
       <code>loop_over_dataset.py</code>
     </td>
      <td>
        Loops over all frames in a Waymo Open Dataset (<code>.tfrecord</code>) file to:<br>
        1. <b>detect</b> and <b>track</b> objects;<br>
        2. <b>visualize</b> those results.
      </td>
      <td>-</td>
    </tr>
    <tr>
      <td style="vertical-align: middle">
       <img src="https://www.iconpacks.net/icons/2/free-file-icon-1453-thumb.png" width="10%">
       <code>README.md</code>
     </td>
      <td></td>
      <td>-</td>
    </tr>
    <tr>
      <td style="vertical-align: middle">
       <img src="https://www.iconpacks.net/icons/2/free-file-icon-1453-thumb.png" width="10%">
       <code>requirements.txt</code>
     </td>
      <td>A list of all of a project's dependencies. This includes the dependencies needed by the dependencies.</td>
      <td>-</td>
    </tr>
    <tr>
      <td style="vertical-align: middle">
       <img src="https://www.iconpacks.net/icons/2/free-file-icon-1453-thumb.png" width="10%">
       <code>writeup.md</code>
     </td>
      <td></td>
      <td>-</td>
    </tr>
  </tbody>
</table>


📦project<br>
 
 ┣ 📂tools --> external tools<br>
 ┃ ┣ 📂objdet_models --> models for object detection<br>
 ┃ ┃ ┃<br>
 ┃ ┃ ┣ 📂darknet<br>
 ┃ ┃ ┃ ┣ 📂config<br>
 ┃ ┃ ┃ ┣ 📂models --> darknet / yolo model class and tools<br>
 ┃ ┃ ┃ ┣ 📂pretrained --> copy pre-trained model file here<br>
 ┃ ┃ ┃ ┃ ┗ complex_yolov4_mse_loss.pth<br>
 ┃ ┃ ┃ ┣ 📂utils --> various helper functions<br>
 ┃ ┃ ┃<br>
 ┃ ┃ ┗ 📂resnet<br>
 ┃ ┃ ┃ ┣ 📂models --> fpn_resnet model class and tools<br>
 ┃ ┃ ┃ ┣ 📂pretrained --> copy pre-trained model file here <br>
 ┃ ┃ ┃ ┃ ┗ fpn_resnet_18_epoch_300.pth <br>
 ┃ ┃ ┃ ┣ 📂utils --> various helper functions<br>
 ┃ ┃ ┃<br>
 ┃ ┗ 📂waymo_reader --> functions for light-weight loading of Waymo sequences<br>
<!---------------------------------------------------------------------------------------------------------------------------------------------------------------->
<!---------------------------------------------------------------------------------------------------------------------------------------------------------------->
<!---------------------------------------------------------------------------------------------------------------------------------------------------------------->
<!--                                                                      INSTALLATION                                                                          >
<!---------------------------------------------------------------------------------------------------------------------------------------------------------------->
<!---------------------------------------------------------------------------------------------------------------------------------------------------------------->
<!---------------------------------------------------------------------------------------------------------------------------------------------------------------->
## Installation Instructions for Running Locally
### Cloning the Project
In order to create a local copy of the project, please click on "Code" and then "Download ZIP". Alternatively, you may of-course use GitHub Desktop or Git Bash for this purpose. 

### Python
The project has been written using Python 3.7. Please make sure that your local installation is equal or above this version. 

### Package Requirements
All dependencies required for the project have been listed in the file `requirements.txt`. You may install them from <code>terminal</code> using either of these approaches:
  * Individually (e.g., <code>pip3 install numpy</code>.
  * All at once, using `pip3 install -r requirements.txt`.
  	
      💡 <b>Note:</b> In the second case, if you moved the <code>requirements.txt</code> file from the root directory, you'll need to provide its full path to be able run this command and install packages, successfully.

### Waymo Open Dataset Reader
The Waymo Open Dataset Reader is a very convenient toolbox that allows you to access sequences from the Waymo Open Dataset without the need of installing all of the heavy-weight dependencies that come along with the official toolbox. The installation instructions can be found in `tools/waymo_reader/README.md`. 

### Waymo Open Dataset Files
This project makes use of three different sequences to illustrate the concepts of object detection and tracking. These are: 
- Sequence 1 : `training_segment-1005081002024129653_5313_150_5333_150_with_camera_labels.tfrecord`
- Sequence 2 : `training_segment-10072231702153043603_5725_000_5745_000_with_camera_labels.tfrecord`
- Sequence 3 : `training_segment-10963653239323173269_1924_000_1944_000_with_camera_labels.tfrecord`

To download these files, you will have to register with Waymo Open Dataset first: [Open Dataset – Waymo](https://waymo.com/open/terms), if you have not already, making sure to note "Udacity" as your institution.

Once you have done so, please [click here](https://console.cloud.google.com/storage/browser/waymo_open_dataset_v_1_2_0_individual_files) to access the Google Cloud Container that holds all the sequences. Once you have been cleared for access by Waymo (which might take up to 48 hours), you can download the individual sequences. 

The sequences listed above can be found in the folder "training". Please download them and put the `tfrecord`-files into the `dataset` folder of this project.


### Pre-Trained Models
The object detection methods used in this project use pre-trained models which have been provided by the original authors. They can be downloaded [here](https://drive.google.com/file/d/1Pqx7sShlqKSGmvshTYbNDcUEYyZwfn3A/view?usp=sharing) (darknet) and [here](https://drive.google.com/file/d/1RcEfUIF1pzDZco8PJkZ10OL-wLL2usEj/view?usp=sharing) (fpn_resnet). Once downloaded, please copy the model files into the paths `/tools/objdet_models/darknet/pretrained` and `/tools/objdet_models/fpn_resnet/pretrained` respectively.

### Using Pre-Computed Results

In the main file `loop_over_dataset.py`, you can choose which steps of the algorithm should be executed. If you want to call a specific function, you simply need to add the corresponding string literal to one of the following lists: 

- `exec_data` : controls the execution of steps related to sensor data. 
  - `pcl_from_rangeimage` transforms the Waymo Open Data range image into a 3D point-cloud
  - `load_image` returns the image of the front camera

- `exec_detection` : controls which steps of model-based 3D object detection are performed
  - `bev_from_pcl` transforms the point-cloud into a fixed-size birds-eye view perspective
  - `detect_objects` executes the actual detection and returns a set of objects (only vehicles) 
  - `validate_object_labels` decides which ground-truth labels should be considered (e.g. based on difficulty or visibility)
  - `measure_detection_performance` contains methods to evaluate detection performance for a single frame

In case you do not include a specific step into the list, pre-computed binary files will be loaded instead. This enables you to run the algorithm and look at the results even without having implemented anything yet. The pre-computed results for the mid-term project need to be loaded using [this](https://drive.google.com/drive/folders/1-s46dKSrtx8rrNwnObGbly2nO3i4D7r7?usp=sharing) link. Please use the folder `darknet` first. Unzip the file within and put its content into the folder `results`.

- `exec_tracking` : controls the execution of the object tracking algorithm

- `exec_visualization` : controls the visualization of results
  - `show_range_image` displays two LiDAR range image channels (range and intensity)
  - `show_labels_in_image` projects ground-truth boxes into the front camera image
  - `show_objects_and_labels_in_bev` projects detected objects and label boxes into the birds-eye view
  - `show_objects_in_bev_labels_in_camera` displays a stacked view with labels inside the camera image on top and the birds-eye view with detected objects on the bottom
  - `show_tracks` displays the tracking results
  - `show_detection_performance` displays the performance evaluation based on all detected 
  - `make_tracking_movie` renders an output movie of the object tracking results

Even without solving any of the tasks, the project code can be executed. 

The final project uses pre-computed lidar detections in order for all students to have the same input data. If you use the workspace, the data is prepared there already. Otherwise, [download the pre-computed lidar detections](https://drive.google.com/drive/folders/1IkqFGYTF6Fh_d8J3UjQOSNJ2V42UDZpO?usp=sharing) (~1 GB), unzip them and put them in the folder `results`.

## External Dependencies
Parts of this project are based on the following repositories: 
- [Simple Waymo Open Dataset Reader](https://github.com/gdlg/simple-waymo-open-dataset-reader)
- [Super Fast and Accurate 3D Object Detection based on 3D LiDAR Point Clouds](https://github.com/maudzung/SFA3D)
- [Complex-YOLO: Real-time 3D Object Detection on Point Clouds](https://github.com/maudzung/Complex-YOLOv4-Pytorch)


## License
[License](LICENSE.md)
