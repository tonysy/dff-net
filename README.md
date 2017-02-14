# Setup
- excute `make` in the project root

### Data Prepare
1. Make folder `images`, `imglists` in `data/kitti`.
2. Get images  

#### Method I
- `ln -s /data/zhicheng/kitti_training/images ./data/kitti`
- `ln -s /data/zhicheng/kitti_training/imglists ./data/kitti`

#### Method II
1. Download data from /rawdata/kitti_data/data_object_image_2 or http://www.cvlibs.net/download.php?file=data_object_image_2.zip
Put all training images in `images` folder, put all testing images in `images/testing` folder.
2. Get imglists  
Download example imglists from https://www.dropbox.com/s/x0gh5fxt0kn9e87/kitti_imglists.tar.gz?dl=0

3. Get evaluation toolkit  
Download from https://www.dropbox.com/s/5z562s7c1ns8umf/kitti_eval.tar.gz?dl=0
Extract it. Run `make` in `kitti_eval`.
Each time you evaluate, run
```bash
cp data/kitti/results/* kitti_eval/results/frcnn/data
./test.sh
```

### Train (Direct Detection)
1. Make `model` in `HOME`.
2. Rename `vgg16-0000.params` to `vgg16-0001.params`
