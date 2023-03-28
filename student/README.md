# Files Structure of the <code>../student</code> directory


<table>
  <thead>
    <tr>
      <th width="30%">File</th>
      <th width="30%">Description</th>
      <th width="40%">Methods</th>
    </tr>
  </thead>
  <tbody>
  <!--========================================================================================================
  ============================================================================================================
  ============================================================================================================
                                                association.py
  ============================================================================================================
  ============================================================================================================
  ============================================================================================================>
  <tr>
    <!----------------------------------------------------------------------------------------------------------
                                                   File
    ------------------------------------------------------------------------------------------------------------>
    <td>
      <img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/267_Python-512.png" width="20%"><br>
      <code>association.py</code>
    </td>
    <!----------------------------------------------------------------------------------------------------------
                                                 Description
    ------------------------------------------------------------------------------------------------------------>
    <td>
      Data association class with single nearest neighbor <b>association</b> and <b>gating</b> based on the <b>Mahalanobis distance</b>.
    </td>
    <!----------------------------------------------------------------------------------------------------------
                                                   Methods
    ------------------------------------------------------------------------------------------------------------>
    <td rowspan="2">
      <table style="table-layout: fixed; width: 100%">
        <tr>
          <td style="width: 50%"><code>associate()</code></td>
          <td style="width: 50%">Replaces <code>association_matrix</code> with the actual<br><code>association_matrix</code> based on Mahalanobis distance<br>(see below) for all tracks and all measurements</td>
        </tr>
        <tr>
          <td style="width: 50%"><code>get_closest_track_and_meas()</code></td>
          <td style="width: 50%">Finds closest track and measurement.</td>
        </tr>
        <tr>
          <td style="width: 50%"><code>gating()</code></td>
          <td style="width: 50%">Returns <code>True</code> if measurement lies inside <b>gate</b>,<br>otherwise <code>False</code>.</td>
        </tr>
        <tr>
          <td style="width: 50%"><code>MHD()</code></td>
          <td style="width: 50%">Calculates and returns the <b>Mahalanobis distance</b>.</td>
        </tr>
        <tr>
          <td style="width: 50%"><code>associate_and_update()</code></td>
          <td style="width: 50%">Associate measurements and tracks.</td>
        </tr>
      </table>
    </td>
  </tr>
  </tbody>
  <!--========================================================================================================
  ============================================================================================================
  ============================================================================================================
                                                filter.py
  ============================================================================================================
  ============================================================================================================
  ============================================================================================================>
  <tbody>
  <tr>
    <!----------------------------------------------------------------------------------------------------------
                                                   File
    ------------------------------------------------------------------------------------------------------------>
    <td>
      <img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/267_Python-512.png" width="20%"><br>
      <code>filter.py</code>
    </td>
    <!----------------------------------------------------------------------------------------------------------
                                                 Description
    ------------------------------------------------------------------------------------------------------------>
    <td>
      Kalman filter class.
    </td>
    <!----------------------------------------------------------------------------------------------------------
                                                   Methods
    ------------------------------------------------------------------------------------------------------------>
    <td rowspan="2">
      <table style="table-layout: fixed; width: 100%">
        <tr>
          <td style="width: 50%"><code>F()</code></td>
          <td>Implements and returns the <b>system matrix F</b>.</td>
        </tr>
        <tr>
          <td><code>Q()</code></td>
          <td>Implements and returns the <b>process noise covariance Q</b>.</td>
        </tr>
        <tr>
          <td><code>predict()</code></td>
          <td>Predicts <b>state x</b> and <b>estimation error covariance P</b> to next<br>timestep, saves x and P in the <b>track</b>.</td>
        </tr>
        <tr>
          <td><code>update()</code></td>
          <td>Updates <b>state x</b> and <b>covariance P</b> with associated measurement,<br>saves x and P in the <b>track</b>.</td>
        </tr>
        <tr>
          <td><code>gamma()</code></td>
          <td>Calculates and returns the <b>residual gamma</b>.</td>
        </tr>
        <tr>
          <td><code>S()</code></td>
          <td>Calculates and returns the <b>covariance of residual S</b>.</td>
        </tr>
    </table>
    </td>
  </tr>
  </tbody>
  <!--========================================================================================================
  ============================================================================================================
  ============================================================================================================
                                                measurements.py
  ============================================================================================================
  ============================================================================================================
  ============================================================================================================>
  <tbody>
  <tr>
    <!----------------------------------------------------------------------------------------------------------
                                                   File
    ------------------------------------------------------------------------------------------------------------>
    <td>
      <img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/267_Python-512.png" width="20%"><br>
      <code>measurements.py</code>
    </td>
    <!----------------------------------------------------------------------------------------------------------
                                                 Description
    ------------------------------------------------------------------------------------------------------------>
    <td>
      Sensor and measurement classes.
    </td>
    <!----------------------------------------------------------------------------------------------------------
                                                   Methods
    ------------------------------------------------------------------------------------------------------------>
    <td rowspan="2">
      <table style="table-layout: fixed; width: 100%">
        <tr>
          <td style="width: 50%"><code><b>Sensor</b>.in_fov()</code></td>
          <td style="width: 50%">Checks if an object x can be seen by<br>this sensor (i.e., <b>FOV</b> of the sensor).</td>
        </tr>
        <tr>
          <td style="width: 50%"><code><b>Sensor</b>.get_hx()</code></td>
          <td style="width: 50%">Calculates <b>nonlinear measurement<br>expectation</b> value h(x).</td>
        </tr>
        <tr>
          <td style="width: 50%"><code><b>Sensor</b>.get_H()</code></td>
          <td style="width: 50%">Predicts <b>state x</b> and <b>estimation error </b><b>covariance P</b><br>to next timestep, saves x and P in the track.</td>
        </tr>
        <tr>
          <td style="width: 50%"><code><b>Sensor</b>.generate_measurement()</code></td>
          <td style="width: 50%">Updates <b>state x</b> and <b>estimation error</b> <b>covariance P</b><br>with associated measurement, saves x and P in the track.</td>
        </tr>
    </table>
    </td>
  </tr>
  </tbody>
  <!--========================================================================================================
  ============================================================================================================
  ============================================================================================================
                                                objdet_detect.py
  ============================================================================================================
  ============================================================================================================
  ============================================================================================================>
  <tbody>
  <tr>
    <!----------------------------------------------------------------------------------------------------------
                                                   File
    ------------------------------------------------------------------------------------------------------------>
    <td>
      <img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/267_Python-512.png" width="20%"><br>
      <code>objdet_detect.py</code>
    </td>
    <!----------------------------------------------------------------------------------------------------------
                                                 Description
    ------------------------------------------------------------------------------------------------------------>
    <td>
      Detects 3D objects in lidar point clouds, using deep learning.
    </td>
    <!----------------------------------------------------------------------------------------------------------
                                                   Methods
    ------------------------------------------------------------------------------------------------------------>
    <td rowspan="2">
      <table style="table-layout: fixed; width: 100%">
        <tr>
          <td style="width: 50%"><code>_sigmoid()</code></td>
          <td style="width: 50%">Applies the PyTorch <code>sigmoid</code> activation function.</td>
        </tr>
        <tr>
          <td style="width: 50%"><code>load_configs_model()</code></td>
          <td style="width: 50%">Loads model (<code>darknet</code> or <code>resnet</code>) parameters into<br>an EasyDict <code>edict</code>.</td>
        </tr>
        <tr>
          <td style="width: 50%"><code>load_configs()</code></td>
          <td style="width: 50%">Loads all object-detection parameters into<br>an EasyDict <code>edict</code>.</td>
        </tr>
        <tr>
          <td style="width: 50%"><code>create_model()</code></td>
          <td style="width: 50%">Creates model according to selected model type.</td>
        </tr>
        <tr>
          <td style="width: 50%"><code>detect_objects()</code></td>
          <td style="width: 50%">Detects trained objects in the birds-eye view (BEV).</td>
        </tr>
    </table>
    </td>
  </tr>
  </tbody>
  <!--========================================================================================================
  ============================================================================================================
  ============================================================================================================
                                                objdet_eval.py
  ============================================================================================================
  ============================================================================================================
  ============================================================================================================>
  <tbody>
  <tr>
    <!----------------------------------------------------------------------------------------------------------
                                                   File
    ------------------------------------------------------------------------------------------------------------>
    <td>
      <img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/267_Python-512.png" width="20%"><br>
      <code>objdet_eval.py</code>
    </td>
    <!----------------------------------------------------------------------------------------------------------
                                                 Description
    ------------------------------------------------------------------------------------------------------------>
    <td>
      Evaluates performance of object detection.
    </td>
    <!----------------------------------------------------------------------------------------------------------
                                                   Methods
    ------------------------------------------------------------------------------------------------------------>
    <td rowspan="2">
      <table style="table-layout: fixed; width: 100%">
        <tr>
          <td style="width: 50%"><code>measure_detection_performance()</code></td>
          <td style="width: 50%">Computes various performance<br>measures to assess object<br>detection.</br></td>
        </tr>
        <tr>
          <td style="width: 50%"><code>compute_performance_stats()</code></td>
          <td style="width: 50%">Evaluates object detection<br>performance based on all frames.</td>
        </tr>
    </table>
    </td>
  </tr>
  </tbody>
  <!--========================================================================================================
  ============================================================================================================
  ============================================================================================================
                                                objdet_pcl.py
  ============================================================================================================
  ============================================================================================================
  ============================================================================================================>
  <tbody>
  <tr>
    <!----------------------------------------------------------------------------------------------------------
                                                   File
    ------------------------------------------------------------------------------------------------------------>
    <td>
      <img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/267_Python-512.png" width="20%"><br>
      <code>objdet_pcl.py</code>
    </td>
    <!----------------------------------------------------------------------------------------------------------
                                                 Description
    ------------------------------------------------------------------------------------------------------------>
    <td>
      Processes the point-cloud and prepare it for object detection.
    </td>
    <!----------------------------------------------------------------------------------------------------------
                                                   Methods
    ------------------------------------------------------------------------------------------------------------>
    <td rowspan="2">
      <table style="table-layout: fixed; width: 100%">
        <tr>
          <td style="width: 50%"><code>show_pcl()</code></td>
          <td style="width: 50%">Visualizes <b>LiDAR point-cloud</b>.</td>
        </tr>
        <tr>
          <td style="width: 50%"><code>show_range_image()</code></td>
          <td style="width: 50%">Visualizes <b>range image</b>.</td>
        </tr>
        <tr>
          <td style="width: 50%"><code>bev_from_pcl()</code></td>
          <td style="width: 50%">Creates the LiDAR birds-eye view from LiDAR point-cloud.</td>
        </tr>
        <tr>
          <td style="width: 50%"><code>create_model()</code></td>
          <td style="width: 50%">Creates model according to selected model type.</td>
        </tr>
    </table>
    </td>
  </tr>
  </tbody>
  <tbody>
  <!--========================================================================================================
  ============================================================================================================
  ============================================================================================================
                                              trackmanagement.py
  ============================================================================================================
  ============================================================================================================
  ============================================================================================================>
  <tbody>
  <tr>
    <!----------------------------------------------------------------------------------------------------------
                                                   File
    ------------------------------------------------------------------------------------------------------------>
    <td>
      <img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/267_Python-512.png" width="20%"><br>
      <code>trackmanagement.py</code>
    </td>
    <!----------------------------------------------------------------------------------------------------------
                                                 Description
    ------------------------------------------------------------------------------------------------------------>
    <td>
      Track and track management classes.
    </td>
    <!----------------------------------------------------------------------------------------------------------
                                                   Methods
    ------------------------------------------------------------------------------------------------------------>
    <td rowspan="2">
      <table style="table-layout: fixed; width: 100%">
        <tr>
          <td style="width: 50%"><code><b>Track</b>.set_x()</code></td>
          <td style="width: 50%">Replaces fixed track initialization values by<br>initialization of x based on unassigned<br>measurement transformed from<br>sensor to vehicle coordinates.</td>
        </tr>
        <tr>
          <td style="width: 50%"><code><b>Track</b>.set_P()</code></td>
          <td style="width: 50%">Replaces fixed track initialization values by<br>initialization of P based on unassigned<br>measurement transformed from<br>sensor to vehicle coordinates.</td>
        </tr>
        <tr>
          <td style="width: 50%"><code><b>Track</b>.set_t()</code></td>
          <td style="width: 50%">Creates birds-eye view of lidar data.</td>
        </tr>
        <tr>
          <td style="width: 50%"><code><b>Track</b>.update_attributes()</code></td>
          <td style="width: 50%">Creates model according to selected.</td>
        </tr>
        <tr>
          <td style="width: 50%"><code><b>Trackmanagement</b>.manage_tracks()</code></td>
          <td style="width: 50%">Creates model according to selected.</td>
        </tr>
        <tr>
          <td style="width: 50%"><code><b>Trackmanagement</b>.addTrackToList()</code></td>
          <td style="width: 50%">Adds a track to the <code>track_list</code>.</td>
        </tr>        
        <tr>
          <td style="width: 50%"><code><b>Trackmanagement</b>.init_track()</code></td>
          <td style="width: 50%">Initializes a track based on its <code>meas</code> and <code>id</code>.</td>
        </tr>        
        <tr>
          <td style="width: 50%"><code><b>Trackmanagement</b>.delete_track()</code></td>
          <td style="width: 50%">Deletes a track from the <code>track_list</code>.</td>
        </tr>        
        <tr>
          <td style="width: 50%"><code><b>Trackmanagement</b>.handle_updated_track()</code></td>
          <td style="width: 50%">Implements track management for updated<br>tracks by increasing the track score and set<br>track state to 'tentative' or 'confirmed'.</td>
        </tr>
    </table>
    </td>
  </tr> 
  </tbody>
</table>

# Example

To call the function (method) <code>bev_from_pcl()</code> from file <code>../student/objdet_pcl.py</code> within the file <code>../loop_over_dataset.py</code>, simply use:
```python
from student.objdet_pcl import bev_from_pcl
```

💡 <b>Note:</b> Some of the above files have two or more classes. Hence, when trying to call a method, you will have to call its class first. For example, file <code>trackmanagement.py</code> contains two classes: <code>Track</code> and <code>Trackmanagement</code>. If you want to use the <code>set_x()</code> method of <code>Track</code> class, you should do this:
```python
from student.trackmanagement.Track import set_x
```

or, alternatively:

```python
from student.trackmanagement import Track.set_x
```
