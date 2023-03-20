# File Format

The `.h5` files in this directory contain experimental data from uniaxial stretching experiments, and are readable by the Mathematica notebook `template.nb`. Alternatively, their contents are fully described below:

The samples used in each experiment are described in the file name, and in the `description` attribute of `/` in the `.h5` file. Each file contains data derived from up to 5 (five) videos. Not every frame of every video has data available, so the following information is stored for each frame that does have data associated with it:

1. The frame number, in the `/video#/frames` record.
2. The (x,y) position of every tracked pin, in the `/video#/traj` record.
3. The force applied to the sample, in the `/video#/forces` record.

The order in which the tracked pins are stored is by convention:

1. Right pin
2. Left pin
3. Bottom pin (if present)
4. Top pin (if present)
5. Bottom clamp 
6. Top clamp 

Additionally, two properties of the sample are stored in their own record, and are the same across all videos in a file:

1. The distance from one edge of the clamp to the other, measured in pixels, in `/clampSize`. This is used to set the camera scale.
2. The width of the fabric at the clamp, in pixels, in `/fabricSize`. This is used to convert force to stress.




Data Note:

Pearlized Cotton Rib Y only has 4 points to track: one at each clamp and the two transverse points
Each of the glove prototype samples only has 1 experimental video and 4 points to track: one at each clamp and the two transverse points


