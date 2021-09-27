# Notebooks

<br>

## Convention

<br>

- 이 폴더에는 .ipynb 파일들만 저장되어 있습니다.
- .ipynb 파일들은 Google COLAB 에서 실행해야만 합니다.

<br><br>

### principles

<br>

- 모든 노트북은 TensorBoard 를 지원합니다.

<br>

### prefix, posfix

<br>

- "something_" : 서드파티 라이브러리를 적극적으로 활용하는 파일입니다.
- "_test" : 다양한 모델을 빠르게 실행해 보는 파일입니다.
- "_load" : .py 파일로 구성되어 있는 모델을 불러와 실행해 주는 파일입니다.
- 위에 해당하지 않는다면 해당 .ipynb 파일은 노트북 안에서 모델을 만들고 구동하는 파일입니다. 논문 그 자체의 구현에 가장 충실한 파일로, end-to-end 예제를 보기에 가장 적절합니다.

<br><br>

## Models

<br><br>

### ResNet - Deep residual learning for image recognition

<br>

![resnet_00](https://github.com/ProtossDragoon/paper_implementation_and_testing_tf2/blob/main/docs/img/resnet_00.png?raw=true)

<br>

![resnet_01](https://github.com/ProtossDragoon/paper_implementation_and_testing_tf2/blob/main/docs/img/resnet_01.png?raw=true)

<br>

![resnet_02](https://github.com/ProtossDragoon/paper_implementation_and_testing_tf2/blob/main/docs/img/resnet_02.png?raw=true)

<br><br>

## sm - Segmentation Models

<br>

### support

<br>

- [x] Google COLAB GPU + Google Drive + tf.keras
- [x] Google COLAB GPU + Google Cloud Storage + tf.keras
- [ ] Google COLAB TPU + Google Cloud Storage + tf.keras *tf.keras 데이터로더로는 TPU용 모델 훈련이 불가능함.*
- [x] Google COLAB GPU + Google Drive + tf.data
- [x] Google COLAB GPU + Google Cloud Storage + tf.data
- [x] Google COLAB TPU + Google Cloud Storage + tf.data
  - [x] grayscaled mask *Multiclass Segmentation 을 위한 Grayscale mask 영상의 픽셀값이 1채널 정수값을 나타냄.*
  - [x] rgb colored mask
- [x] Google COLAB GPU + Google Drive + tfrecord
- [x] Google COLAB GPU + Google Cloud Storage + tfrecord
- [x] Google COLAB TPU + Google Cloud Storage + tfrecord
  - [x] grayscaled mask
  - [x] rgb colored mask

<br>

- CPU
  - no support
- Google COLAB GPU
  - [ ] read mask
    - [x] classid 로 구성된 마스크
    - [ ] classid 로 구성된 마스크, 여러 클래스를 묶어서 하나의 클래스로 학습
    - [x] 색상으로 구성된 마스크
    - [x] 색상으로 구성된 마스크, 여러 클래스를 묶어서 하나의 클래스로 학습
  - [x] resize
  - [x] augmentation
    - [x] albumentation
  - [x] trainingset aware preprocessing (현재로써는 imagenet)
- Google COLAB TPU
  - [ ] read mask
    - [x] classid 로 구성된 마스크
    - [ ] classid 로 구성된 마스크, 여러 클래스를 묶어서 하나의 클래스로 학습
    - [x] 색상으로 구성된 마스크
    - [x] 색상으로 구성된 마스크, 여러 클래스를 묶어서 하나의 클래스로 학습
  - [x] resize
  - [ ] augmentation
  - [ ] trainingset aware preprocessing (지원 안함, [참고 issue](https://github.com/ProtossDragoon/paper_implementation_and_testing_tf2/issues/4))

<br>

![sm_00](https://github.com/ProtossDragoon/paper_implementation_and_testing_tf2/blob/main/docs/img/sm_00.png?raw=true)

<br>

- 이 노트북은 내부 문서와 함께 관리됩니다. 아래 스크린샷은 예시입니다.

![sm_uml](https://github.com/ProtossDragoon/paper_implementation_and_testing_tf2/blob/main/docs/img/sm_uml.png?raw=true)

<br>

- 이 노트북은 CamVid dataset 을 지원합니다. 다운로드 코드가 내장되어 있습니다.

![sm_camvid](https://github.com/ProtossDragoon/paper_implementation_and_testing_tf2/blob/main/docs/img/sm_camvid.png?raw=true)

<br>

- 이 노트북은 Aihub 의 Pedestrian dataset (인도 보행 영상) 의 Segmentation Masking 을 지원합니다.

![sm_aihubpedestrian](https://github.com/ProtossDragoon/paper_implementation_and_testing_tf2/blob/main/docs/img/sm_aihubpedestrian.png?raw=true)

<br>

- 이 노트북은 아래와 같이 원본 클래스 정보를 바탕으로 마스크를 불러들이면서 직접 여러 클래스를 묶어줄 수 있어요.

![sm_customize_class](https://github.com/ProtossDragoon/paper_implementation_and_testing_tf2/blob/main/docs/img/sm_customize_class.png?raw=true)

<br>

- 이 노트북은 아래와 같이 Albumentation 라이브러리를 통해 다양한 augmentation 을 지원하고, 쉽게 시각화하며 디버깅해볼 수 있어요.
- 참, TPU 모드에서는 Albumentation 과 augmentation 을 사용할 수 없어요.

![sm_support_augmentation](https://github.com/ProtossDragoon/paper_implementation_and_testing_tf2/blob/main/docs/img/sm_support_augmentation.png?raw=true)

<br>

- 이 노트북은 keras.Sequence 로더를 기반으로 한 numeric validation 을 지원합니다.

![sm_aihubpedestrian](https://github.com/ProtossDragoon/paper_implementation_and_testing_tf2/blob/main/docs/img/sm_aihubpedestrian_cherrypick.png?raw=true)
![sm_aihubpedestrian](https://github.com/ProtossDragoon/paper_implementation_and_testing_tf2/blob/main/docs/img/sm_aihubpedestrian_validation_1.png?raw=true)
![sm_aihubpedestrian](https://github.com/ProtossDragoon/paper_implementation_and_testing_tf2/blob/main/docs/img/sm_aihubpedestrian_validation_2.png?raw=true)
![sm_aihubpedestrian](https://github.com/ProtossDragoon/paper_implementation_and_testing_tf2/blob/main/docs/img/sm_aihubpedestrian_validation_3.png?raw=true)
![sm_aihubpedestrian](https://github.com/ProtossDragoon/paper_implementation_and_testing_tf2/blob/main/docs/img/sm_aihubpedestrian_validation_4.png?raw=true)

<br>

```
4635/4635 [==============================] - 7667s 2s/step - loss: 0.9736 - iou_score: 0.7639 - f1-score: 0.7904 - categorical_acc: 0.8548
what - if your <prediction input size> == <training input size>
evaluate shape : (1,320,320,3)
mean iou_score: 0.76389
mean f1-score: 0.79038
mean categorical_acc: 0.85481
```

<br>
