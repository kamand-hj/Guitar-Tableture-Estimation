# Guitar-Tableture-Estimation
This project is an attempt to make automatic tablature from a data set of electric guitar recordings based on the Wiggins and Kim  paper. At first a dataset of 48 electric guitar recordings was built. To this regard we played 3 songs in  4 different styles, fast and slow. For each of those ‘categories’, we played the chords, as well as the solo over those chords. After this step, we made CQTs of these recordings. From these CQTs, frames are sampled in an overlapping window with a length of 9 frames. The paper we based our project on had access to hexaphonic pickups, which allowed them to have detailed annotations of their playing. Since we did not have access to that, we used a different method of creating the annotations.  We made some handmade tabs of these recordings using Guitar Pro. From these tabs we generate midi files. From these midi files we create arrays of one-hot vector encodings in a shape of the amount of the frames by 6 by 21. We trained our network based on the dataset used in the original paper, which is the GuitarSet, and then used our own dataset to test it.  At the last step, we calculated the related measures to evaluate the TabCNN model on our own dataset. Our model achieved a score of 0.635 for TDR measure that indicates the probability that our model assigns the correct tablature to the correctly identified pitches is a bit higher than 63 percent.
## Output sample

![output sample](Picture1.png)
## Files and folders in repo
### .ipynb_checkpoints
Metrics for evaluating the model
### midi-visualization-master
Midi files
### Tracks
Tracks, base on our electric guitar recordings
### GUITAR TABLATURE ESTIMATION
This PDF file is the report of our project


