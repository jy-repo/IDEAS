# SIFT

by Lowe   
Solves: image rotation, affine transformations, intensity, viewpoint change   
ref) [Image Matching Using SIFT, SURF, BRIEF and ORB: Performance Comparison for Distorted Images](https://arxiv.org/ftp/arxiv/papers/1710/1710.02726.pdf)   
    
step 1: estimate a scale sapce extrema
step 2: key point localization (localization + refining: eliminate low contrast points)
step 3: key points orientation assignment
step 4: descriptor generator -> compute local image descriptor for each key point.

# SURF (Speed-UP Robust Feature)

Similar to SIFT.
Faster.

