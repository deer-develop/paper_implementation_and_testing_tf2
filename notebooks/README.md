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
- [ ] Google COLAB TPU + Google Cloud Storage + tf.data
  - [x] grayscaled mask *Multiclass Segmentation 을 위한 Grayscale mask 영상의 픽셀값이 1채널 정수값을 나타냄.*
  - [ ] rgb colored mask *도와주세요: 왜 안되는지 모름*
- [x] Google COLAB GPU + Google Drive + tfrecord
- [x] Google COLAB GPU + Google Cloud Storage + tfrecord
- [ ] Google COLAB TPU + Google Cloud Storage + tfrecord
  - [x] grayscaled mask
  - [ ] rgb colored mask

<br>

![sm_00](https://github.com/ProtossDragoon/paper_implementation_and_testing_tf2/blob/main/docs/img/sm_00.png?raw=true)
