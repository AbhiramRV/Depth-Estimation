Task of estimating depth information from images can be done using a sterio camera set.

Camera calibration is the process of calculating intrensic and extrensic parameters.
After camera calibration, image data can be used to extract 3-D information from 2-D
Extrensic parameters are used to translate world points to camera coordinates.Intrensic parameters are used to
    transfer camera coordinates onto image coordinates(2D).
Camera calibration is also used to rectify image distortions.

  [su sv s].T = k [R|t] [X Y Z 1].T
  
  k is intrinsic parameter matrix
  R|t is extrensic parameter matrix

Disparity is the difference in the location of same 3D object in the prospective of two different cameras.
sterio formulation
Z= f.b/(xL-xR) =f.b/d
X= Z.xL/f and Y= Z.yL/f

Accuracy of depth estimation depends on the quality of disparity estimation.
Disparity can be coputed by disparity correspondence(matching pixels in two different images)
