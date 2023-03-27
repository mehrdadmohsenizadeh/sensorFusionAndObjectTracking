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
      <img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/267_Python-512.png" width="13%">
      <code>association.py</code>
    </td>
    <!----------------------------------------------------------------------------------------------------------
                                                 Description
    ------------------------------------------------------------------------------------------------------------>
    <td>
      Data association class with single nearest neighbor association and gating based on <b>Mahalanobis distance</b>.
    </td>
    <!----------------------------------------------------------------------------------------------------------
                                                   Methods
    ------------------------------------------------------------------------------------------------------------>
    <td rowspan="2">
      <table>
        <tr>
          <td width="41%"><code>associate()</code></td>
          <td>Replaces <code>association_matrix</code> with the actual<br><code>association_matrix</code> based on Mahalanobis distance<br>(see below) for all tracks and all measurements</td>
        </tr>
        <tr>
          <td><code>get_closest_track_and_meas()</code></td>
          <td>Finds closest track and measurement.</td>
        </tr>
        <tr>
          <td><code>gating()</code></td>
          <td>Returns <code>True</code> if measurement lies inside gate,<br>otherwise <code>False</code>.</td>
        </tr>
        <tr>
          <td><code>MHD()</code></td>
          <td>Calculates and returns Mahalanobis distance.</td>
        </tr>
        <tr>
          <td><code>associate_and_update()</code></td>
          <td>Associate measurements and tracks.</td>
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
      <img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/267_Python-512.png" width="13%">
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
      <table>
        <tr>
          <td width="50%"><code>F()</code></td>
          <td>Implements and returns the system matrix F.</td>
        </tr>
        <tr>
          <td><code>Q()</code></td>
          <td>Implements and returns the process noise covariance Q.</td>
        </tr>
        <tr>
          <td><code>predict()</code></td>
          <td>Predicts state x and estimation error covariance P to next<br>timestep, saves x and P in track.</td>
        </tr>
        <tr>
          <td><code>update()</code></td>
          <td>Updates state x and covariance P with associated<br>measurement, saves x and P in track.</td>
        </tr>
        <tr>
          <td><code>gamma()</code></td>
          <td>Calculates and returns the residual gamma.</td>
        </tr>
        <tr>
          <td><code>S()</code></td>
          <td>Calculates and returns the covariance of residual S.</td>
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
      <img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/267_Python-512.png" width="13%">
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
      <table>
        <tr>
          <td width="39%"><code>Sensor.in_fov()</code></td>
          <td>Checks if an object x can be seen by this sensor<br>(i.e., it's in Field of View of the sensor).</td>
        </tr>
        <tr>
          <td><code>Sensor.get_hx()</code></td>
          <td>Calculates nonlinear measurement expectation value h(x).</td>
        </tr>
        <tr>
          <td><code>Sensor.get_H()</code></td>
          <td>Predicts state x and estimation error covariance P<br>to next timestep, saves x and P in track.</td>
        </tr>
        <tr>
          <td><code>Sensor.generate_measurement()</code></td>
          <td>Updates state x and covariance P with associated<br>measurement, saves x and P in track.</td>
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
      <img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/267_Python-512.png" width="13%">
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
      <table>
        <tr>
          <td width="41%"><code>_sigmoid()</code></td>
          <td>Applies the PyTorch <code>sigmoid</code> activation function.</td>
        </tr>
        <tr>
          <td><code>load_configs_model()</code></td>
          <td>Loads model (<code>darknet</code> or <code>resnet</code>) parameters into an <code>edict</code>.</td>
        </tr>
        <tr>
          <td><code>load_configs()</code></td>
          <td>Loads all object-detection parameters into an <code>edict</code>.</td>
        </tr>
        <tr>
          <td><code>create_model()</code></td>
          <td>Creates model according to selected model type.</td>
        </tr>
        <tr>
          <td><code>detect_objects()</code></td>
          <td>Detects trained objects in birds-eye view (BEV).</td>
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
      <img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/267_Python-512.png" width="13%">
      <code>objdet_eval.py</code>
    </td>
    <!----------------------------------------------------------------------------------------------------------
                                                 Description
    ------------------------------------------------------------------------------------------------------------>
    <td>
      Evaluate performance of object detection.
    </td>
    <!----------------------------------------------------------------------------------------------------------
                                                   Methods
    ------------------------------------------------------------------------------------------------------------>
    <td rowspan="2">
      <table>
        <tr>
          <td width="35%"><code>measure_detection_performance()</code></td>
          <td>Computes various performance measures to assess<br>object detection.</td>
        </tr>
        <tr>
          <td><code>compute_performance_stats()</code></td>
          <td>Evaluates object detection performance based on<br>all frames.</td>
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
      <img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/267_Python-512.png" width="13%">
      <code>objdet_pcl.py</code>
    </td>
    <!----------------------------------------------------------------------------------------------------------
                                                 Description
    ------------------------------------------------------------------------------------------------------------>
    <td>
      Process the point-cloud and prepare it for object detection.
    </td>
    <!----------------------------------------------------------------------------------------------------------
                                                   Methods
    ------------------------------------------------------------------------------------------------------------>
    <td rowspan="2">
      <table>
        <tr>
          <td width="50%"><code>show_pcl()</code></td>
          <td>Visualize lidar point-cloud.</td>
        </tr>
        <tr>
          <td><code>show_range_image()</code></td>
          <td>Visualizes range image.</td>
        </tr>
        <tr>
          <td><code>bev_from_pcl()</code></td>
          <td>Creates birds-eye view of lidar data.</td>
        </tr>
        <tr>
          <td><code>create_model()</code></td>
          <td>Creates model according to selected model type.</td>
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
      <img src="https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/267_Python-512.png" width="13%">
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
      <table>
        <tr>
          <td><code>Track.set_x()</code></td>
          <td>Replaces fixed track initialization values by initialization<br>of x based on unassigned measurement transformed<br>from sensor to vehicle coordinates.</td>
        </tr>
        <tr>
          <td><code>Track.set_P()</code></td>
          <td>Replaces fixed track initialization values by initialization<br>of P based on unassigned measurement transformed<br>from sensor to vehicle coordinates.</td>
        </tr>
        <tr>
          <td><code>Track.set_t()</code></td>
          <td>Creates birds-eye view of lidar data.</td>
        </tr>
        <tr>
          <td><code>Track.update_attributes()</code></td>
          <td>Creates model according to selected model type.</td>
        </tr>
        <tr>
          <td><code>Trackmanagement.manage_tracks()</code></td>
          <td>Creates model according to selected model type.</td>
        </tr>
        <tr>
          <td><code>Trackmanagement.addTrackToList()</code></td>
          <td>Creates model according to selected model type.</td>
        </tr>        
        <tr>
          <td><code>Trackmanagement.init_track()</code></td>
          <td>Creates model according to selected model type.</td>
        </tr>        
        <tr>
          <td><code>Trackmanagement.delete_track()</code></td>
          <td>Creates model according to selected model type.</td>
        </tr>        
        <tr>
          <td><code>Trackmanagement.handle_updated_track()</code></td>
          <td>Creates model according to selected model type.</td>
        </tr>
    </table>
    </td>
  </tr> 
  </tbody>
</table>
