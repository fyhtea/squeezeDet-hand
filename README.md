# SqueezeDet for gesture
Forked from [SqueezeDet](https://github.com/BichenWuUCB/squeezeDet) and modified for gesture images in Pascol VOC format.
Original paper: [SqueezeDet: Unified, Small, Low Power Fully Convolutional Neural Networks for Real-Time Object Detection for Autonomous Driving](https://arxiv.org/abs/1612.01051). Bichen Wu, Forrest Iandola, Peter H. Jin, Kurt Keutzer (UC Berkeley & DeepScale)

-------------
## CNN pretrained Model:
- Download SqueezeDet model parameters from [here](), and change to pkl format:

  ```Shell
  To do
  ```

## Training/Validation:
- Prepare the Dataset in Psacol Voc style:
  ```Shell
  $Path_to_data/VOC2007/
                    |->Annotations/
                    |     |-> 00****.xml
                          L-> ...    
                    |->JPEGImages/
                    |     L-> 00****.jpg
                    L->ImageSets/Main
                          |-> test.txt
                          |-> train.txt
                          |-> trainval.txt    
                          L-> val.txt
  ```

- Now we can start training. Training script can be found in `$SQDT_ROOT/scripts/train.sh`
  ```Shell
  cd $SQDT_ROOT/
  ./scripts/train.sh squeezeDet
  ```

- At the same time, you can launch evaluation by 

  ```Shell
  cd $SQDT_ROOT/
  ./scripts/eval_train.sh
  ./scripts/eval_val.sh
  ```

- Finally, to monitor training and evaluation process, you can use tensorboard by

  ```Shell
  tensorboard --logdir=$LOG_DIR
  ```
## Demo
  ![alt text](https://github.com/fyhtea/squeezeDet-hand/tree/master/img/sample.jpg)
  ![alt text](https://github.com/fyhtea/squeezeDet-hand/tree/master/img/out_sample.jpg)
