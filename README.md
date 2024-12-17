# Oilu
A new fiducial marker based on a new numeration system and a homogless(no homography) processing methods.

Developed in the [university Mohamed El Bachir El Ibrahimi of Bordj Bou Arreridj](https://www.univ-bba.dz/)


### Contacts
- Email : projectoilu@gmail.com 


# DataSets 
<p><span style="font-size:14">datasets are publicly available at : <a href="https://drive.google.com/drive/folders/1jdIsJ2OG1XgT6t2f4uxCFlXdlKXQPa6q">DataSets</a></span></p>

# Note
The provided binaries are compiled and tested under linux (fedora and ubuntu).
Put the camParams and oiluParams into the same folder.

# Table of contents
1. [Homogles Paper](#)
2. [Contacts](#contacts)
3. [Note](#note)
4. [DataSets](#DataSets)
5. [OILU android App](#OILU-android-App)
6. [OILU Videos](#OILU-Videos)
7. [Usage](#usage)
   1. [Arguments](#arguments)
   2. [Parameters](#parameters)
      - [OiluParams](#oiluparams)
      - [CamParams](#camparams)
8. [ImageOilu](#imageoilu)
9. [ImagePose](#imagepose)
10. [VideoPose](#videopose)
11. [VideoOilu](#videooilu)
12. [Generator](#Generator)
13. [References](#References)

# Data
<p><span style="font-size:14"><a href="https://drive.google.com/drive/folders/1jdIsJ2OG1XgT6t2f4uxCFlXdlKXQPa6q">Paper Data</a></span></p>

# OILU android APP
<p><a href="https://drive.google.com/file/d/1iOyTu1SimKzHVifROQttW1wpidwp-VgP/view?usp=drive_link"><span style="font-size:14"> Download </span></a></p>

# Oilu Videos
<p><a href="https://drive.google.com/file/d/1gz_tGgsR1FlNWoWTlC-yBbE8_ZTysYXZ/view?usp=drive_link"><span style="font-size:14">Pose Demo 1</span></a></p>
<p><span style="font-size:14"><a href="https://drive.google.com/file/d/1gz_tGgsR1FlNWoWTlC-yBbE8_ZTysYXZ/view?usp=drive_link" target="_blank"><img width="110" height="110" border="0" align="center"  alt="" src="https://imagizer.imageshack.com/img923/6847/oVz6BM.gif" /></a></span></p>
<p><a href="https://drive.google.com/file/d/1yCTPqHLpkWQg8QUTKmpBaSZAKYN2iZVJ/view?usp=drive_link"><span style="font-size:14">Aruco - April - Oilu Pose</span></a></p>
<p><span style="font-size:14"><a href="https://drive.google.com/file/d/1yCTPqHLpkWQg8QUTKmpBaSZAKYN2iZVJ/view?usp=drive_link"><img width="110" height="110" border="0" align="center" alt="" src="https://i.top4top.io/p_2992d7smy1.gif" /></a></span></p>
<p><a href="https://drive.google.com/file/d/196fuqixrlnn0MuhPN-Ywn9TtsfnzjlZR/view"><span style="font-size:14">Oilu Angle Test Demo</span></a></p>
<p><span style="font-size:14"><a href="https://drive.google.com/file/d/196fuqixrlnn0MuhPN-Ywn9TtsfnzjlZR/view"><img width="110" height="110" border="0" align="center" alt="" src="https://e.top4top.io/p_2992520l01.gif" /></a></span></p>
<p><a href="https://drive.google.com/file/d/1WvTf75TSWIanEiL-bKGIB07cHd_kYvnE/view?usp=sharing"><span style="font-size:14">Oilu Occlusion Demo</span></a></p>
<p><span style="font-size:14"><a href="https://drive.google.com/file/d/17-9C2eAY_HXdowBIOtEuprWhj-yZrdO2/view?usp=sharing"><img width="110" height="110" border="0" align="center" alt="" src="https://d.top4top.io/p_2992cmkop1.gif" /></a></span></p>
<p><a href="https://drive.google.com/file/d/17-9C2eAY_HXdowBIOtEuprWhj-yZrdO2/view?usp=sharing"><span style="font-size:14">Oilu No Occlusion Demo</span></a></p>
<p><span style="font-size:14"><a href="https://drive.google.com/file/d/1WvTf75TSWIanEiL-bKGIB07cHd_kYvnE/view?usp=sharing"><img width="110" height="110" border="0" align="center" alt="" src="https://h.top4top.io/p_2992g2vgs1.gif" /></a></span></p>

<p><a href="https://drive.google.com/file/d/16LYP2KEWj522mWkQ8j8kmkPo1OmgMNjT/view?usp=sharing"><span style="font-size:14">Oilu Occlusion Demo 2</span></a></p>
<p><span style="font-size:14"><a href="https://drive.google.com/file/d/16LYP2KEWj522mWkQ8j8kmkPo1OmgMNjT/view?usp=sharing"><img width="110" height="110" border="0" align="center" alt="" src="https://s12.gifyu.com/images/SVcMg.gif" /></a></span></p>


# Usage
This section provide a short guide on using the provided binaries.
## Arguments
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Type</th>
      <th>Purpose</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>image/videoPath</td>
      <td>String</td>
      <td>Path to the image or video file</td>
    </tr>
    <tr>
      <td>paramsFolder</td>
      <td>String</td>
      <td>Path to the folder containing oiluParams and camParams.Note we are using cv::Filestorage which may fail to read the files if the path is too large</td>
    </tr>
    <tr>
      <td>segmentsNumber</td>
      <td>Integer</td>
      <td>Number of segments for the oilu marker (max possible segment count)</td>
    </tr>
    <tr>
      <td>keepBiggerCandidate</td>
      <td>Boolean</td>
      <td>Determines whether to keep the bigger or smaller quad candidates (inner quad or outer quad)</td>
    </tr>
    <tr>
      <td>output</td>
      <td>String</td>
      <td>Path to the output video file</td>
    </tr>
    <tr>
      <td>applyGaussianBlur</td>
      <td>Boolean</td>
      <td>Specifies whether to apply Gaussian blur . Use only on the noisy images</td>
    </tr>
  </tbody>
</table>

## Parameters
### OiluParams
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Type</th>
      <th>Purpose</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>MIN_CONTOUR_SIZE</td>
      <td>Integer</td>
      <td>Minimum candidate contour size</td>
    </tr>
    <tr>
      <td>N_SCALES</td>
      <td>Integer</td>
      <td>Number applied adaptive thresholds</td>
    </tr>
    <tr>
      <td>BINARIZATION_THRESH</td>
      <td>Integer</td>
      <td>Binarization threshold</td>
    </tr>
    <tr>
      <td>AVERAGE_DISTANCE_EPSILON</td>
      <td>Float</td>
      <td>Epsilon for average distance calculation</td>
    </tr>
    <tr>
      <td>EPSILON_CURVE_APPROX</td>
      <td>Float</td>
      <td>Epsilon for curve approximation</td>
    </tr>
    <tr>
      <td>WHITE_PIXEL_THRESHOLD</td>
      <td>Integer</td>
      <td>Threshold for white pixels</td>
    </tr>
    <tr>
      <td>SEGMENT_SPACE_RATIO</td>
      <td>Integer</td>
      <td>Ratio for segment space</td>
    </tr>
    <tr>
      <td>WHITE_PIXEL_SATURATION_THRESHOLD</td>
      <td>Integer</td>
      <td>Threshold for white pixel in the saturation channel</td>
    </tr>
    <tr>
      <td>INNER_OUTER_QUAD_RATIO</td>
      <td>Float</td>
      <td>Ratio for estimating outer quad position from inner quadrilateral</td>
    </tr>
  </tbody>
</table>

### CamParams
The default provided params are the ones used in conjuction with the test data . In case you wanted to test it on your own data you will have to calibrate the camera and modify the parameters accordingly.
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Type</th>
      <th>Purpose</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>cameraMatrix</td>
      <td>List</td>
      <td>Matrix representing the camera intrinsics</td>
    </tr>
    <tr>
      <td>distortionCoeff</td>
      <td>List</td>
      <td>Vector representing the distortion coefficients</td>
    </tr>
  </tbody>
</table>



## ImageOilu
Used for detecting and drawing oilu markers on an image.
```
Usage: OMP_NUM_THREADS=n ./ImageOilu <imagePath> <paramsFolder> <segmentsNumber> <keepBiggerCandidate> <applyGaussainBlur>
```
```
Example: OMP_NUM_THREADS=2 ./ImageOilu "/home/path/to/image.jpg" "/home/path/to/params" 6 1 0
```
## ImagePose
Used for estimating oiluMarker pose and drawing the axis on an image.
```
Usage: OMP_NUM_THREADS=n ./ImagePose <imagePath> <paramsFolder> <segmentsNumber> <keepBiggerCandidate>
```
```
Example: OMP_NUM_THREADS=2 ./ImageOilu "/home/path/to/image.jpg" "/home/path/to/params" 6 1 0
```
## VideoPose
Used for estimating oiluMarker pose and drawing the axis on a video.
```
Usage: OMP_NUM_THREADS=n ./VideoPose <videoPath> <output> <paramsFolder> <segmentsNumber> <keepBiggerCandidate>
```
```
Example: OMP_NUM_THREADS=2 ./VideoPose "/home/path/to/video.mp4" "/home/path/to/output/vid.avi" "/home/path/to/params" 6 1 0
```
## VideoOilu
Used for detecting and drawing oilu markers on a video.
```
Usage: OMP_NUM_THREADS=n ./VideoOilu <videoPath> <output> <paramsFolder> <segmentsNumber> <keepBiggerCandidate>
```
```
Example: OMP_NUM_THREADS=2 ./VideoOilu "/home/path/to/video.mp4" "/home/path/to/output/vid.avi" "/home/path/to/params" 6 1 0
```
## Generator
Used for generatin oiluMarkers 
```
Usage: OMP_NUM_THREADS=n ./Generator <outDir> <targetNUmber>
Example: OMP_NUM_THREADS=2 ./Generator /home/path/to/out 999
This would generate oilu codes from 0 to 999
```
## References 
 <p><span style="font-size:14">New Efficient Visual OILU Markers</span></a> The 25th International Conference on Image Processing,Computer Vision, & Pattern Recognition(IPCV 2021)  </p>
<a href="https://drive.google.com/file/d/1kg2H2Qp0kwZyxkbN-PuRnF2Nj469kUOt/view?usp=sharing"><span style="font-size:14">CSCI 2021 BOOK of ABSTRACTS</span></a>
