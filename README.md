Task of estimating depth information from images can be done using a sterio camera set.

Camera calibration is the process of calculating intrensic and extrensic parameters.
After camera calibration, image data can be used to extract 3-D information from 2-D
Extrensic parameters are used to translate world points to camera coordinates.Intrensic parameters are used to
    transfer camera coordinates onto image coordinates(2D).
Camera calibration is also used to rectify image distortions.

  [su sv s].T = k [R|t] [X Y Z 1].T
  
  k is intrinsic parameter matrix
  [R|t] is extrensic parameter matrix

Disparity is the difference in the location of same 3D object in the prospective of two different cameras.
sterio formulation
Z= f.b/(xL-xR) =f.b/d
X= Z.xL/f and Y= Z.yL/f

Accuracy of depth estimation depends on the quality of disparity estimation.
Disparity can be coputed by disparity correspondence(matching pixels in two different images)
Steps involved in depth map estimation are 
    - Read left and right image 
    -Calculate disparity between the images
    -Decompose calibration matirx to get intrinsic and extrensic parameter.
    -Calculate depth of each pixel using the formula Z= f.b/(xL-xR) =f.b/d where d is disparity, b is base line destance between cameras, f is focal length(availabe in intrensic parameters.


Useful opencv functions are
    - cv2.StereoBM or cv2.StereoSGBM
    -cv2.decomposeProjectionMatrix()
   
So inorder to compute depth maps,we need camera calibration matrices(for both left and right camera). 


Visual Odeometry is calcualted using four step process.
1. Feature extraction (ex- SURF, SIFT, ORB and BRIEF)
2. Feature matching from a pair of subsequent frames
3. Trajectory estimation and visualization
