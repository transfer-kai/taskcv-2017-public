## Data

First of all, you probably need some data. You should be able to get it with 
    
    $ cd your-data-location
    
    # ..G
    $ wget http://csr.bu.edu/ftp/visda17/clf/train.tar
    # if link does not work, you can use the backup: 
    $ tar xvf train.tar
    
    # 2.8G
    $ wget http://csr.bu.edu/ftp/visda17/clf/validation.tar
    $ tar xvf validation.tar  

Images are structured in folders as 

- `synth-v3/{category}/{object_id}/{object_id}_{cam_yaw}_{light_yaw}_{cam_pitch}.png` for training synthetic data and
- `coco/{category}/{object_id}.png` or valiation

with a single `.txt` file in the root or each dataset that lists all images and corresponding labels. Folder names won't be avaliable on test time :).

## Code

We have several base models with data readers in `/models` folder. Each model has a short README on how to run it.

- "Adversarial Discriminative Domain Adaptation" (ADDA) with LeNet and VGG16 in Tensorflow [`paper`](https://arxiv.org/abs/1702.05464) [`code`]()
- "Learning Transferable Features with Deep Adaptation Networks" (DAN) with Alexnet in Caffe [`paper`](https://arxiv.org/pdf/1502.02791.pdf) [`code`]()
- "Deep CORAL: Correlation Alignment for Deep Domain Adaptation" with Alexnet in Caffe [`code`]()

Please, look at [challange rules]() to make sure you are doing the right thing.

## Evaluation

Models generate output files We have a single evaluation script shared across evaluation server and . We are using only a subset of data on evaluation server to encourage participants to share their perfomance more frequently to understand how their results compare to other participants.