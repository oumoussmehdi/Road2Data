
## SMOTE 
algorithmic approach to generating new dataset samples. 
The SMOTE algorithm is parameterized with :
- k_neighbors (the number of nearest neighbors it will consider) 
- the number of new points you wish to create. 

Each step of the algorithm will:
1.Randomly select a minority point.
2. Randomly select any of its k_neighbors nearest neighbors belonging to the same class.
3. Randomly specify a lambda value in the range [0, 1].
4. Generate and place a new point on the vector between the two points, located lambda percent of the way from the original point.

The weakness of SMOTE is readily apparent from this quick test. Because the algorithm doesn't have any jitter, for minority class sample clouds with few enough points it tends to result in long "data lines". This results in some very funky looking resultant datasets

SMOTE has also done something here that I am less comfortable with: it's constructed a "bridge" between the main red point cloud and a handful of outlier points located in the blue cluster
Why does this happen? This surprising new structure shows up prominently because in the "line constructor" nature of SMOTE, a few of the outlier points inside of the blue point cloud will match up sometimes with points in the main body of the class cluster. These will then get interpolated into long spaghetti lines.

This is an artifact of the SMOTE algorithm, and is problematic because it introduces a feature into the dataset, this "point bridge", which doesn't actually exist in the underlying dataset.


imlearn includes several adaptations of the naive SMOTE algorithm which attempt to address this weakness in various ways. 
There are in total four "modes" in imlearn. 
* kind='regular' : classic SMOTE algorithm
* kind='borderline1' and 
* kind='borderline2' are one class of adaptations.
* kind='svm'. imlearn documentation is very vague as to how this works, simply stating that it "uses an SVM classifier to find support vectors and generate samples considering them":



## ADASYN : adaptive synthetic sampling
ADASYN is similar to SMOTE, and derived from it, featuring just one important difference. 
it will bias the sample space (that is, the likelihood that any particular point will be chosen for duping) towards points which are located not in homogenous neighborhoods


ref : 
- https://www.kaggle.com/residentmario/oversampling-with-smote-and-adasyn
