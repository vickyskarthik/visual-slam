# visual-slam

Here is a general pipeline for visual SLAM using ORB feature detector and descriptor, pose estimation, and optimization:
* Feature extraction: Use the ORB feature detector to detect and extract features (such as corners and edges) from the current image.
* Feature description: Use the ORB descriptor to compute a descriptor for each feature, which describes the local appearance of the feature.
* Feature matching: Use the descriptors to match the features between the current image and the previous image, and use the matched features to estimate the camera's motion.
* Pose estimation: Use the matched features to estimate the camera's position and orientation using techniques such as PnP (Perspective-n-Point) algorithm.
* Bundle adjustment: Refine the camera's pose and the 3D positions of the features by minimizing the reprojection error of the features using bundle adjustment.
* Mapping: Build a map of the environment by triangulating the 3D positions of the features and storing them as a point cloud.
* Loop closure detection: Compare the current image to previous images using techniques such as bag of words to detect when the camera has returned to a previously visited location.
* Map optimization: Optimize the map and the camera poses using techniques such as bundle adjustment or non-linear optimization when loop closures are detected.
* Visual odometry: Use the estimated camera poses to estimate the camera's motion over time and correct drift in the camera's pose.
* Filter-based methods: Use filters such as Kalman filters or Particle filters to estimate the camera's pose and the map of the environment.
