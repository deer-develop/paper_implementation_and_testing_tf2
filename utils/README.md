# utility notebooks

<br>

## Info

<br>

### Convert TFTRT

<br>

- 모델을 TF-TRT 로 변환하는 예제코드입니다.
- `NOTE:` TF-TRT 는 타겟 디바이스에서만 정상적으로 작동하기 때문에, 실제 성능을 확인할 수는 없습니다.

<br><br>

### GDrive to GCS

<br>

- 구글 드라이브 (gdrive, local) 의 파일이나 데이터셋을 정확하게 구글 클라우드 스토리지 (gs, google cloud storage) 로 옮길 수 있습니다.
- 그 반대도 가능합니다.

<br><br>

### Generate TFRecord

<br>

- 이 노트북은 TFRecord 파일 생성 타이밍의 Augmentation 을 지원합니다. 
- 이 작업을 통해 ```tf.data``` 파이프라인이 단순화되고 학습시간을 단축시킬 수 있습니다.

![tfrecord_aug](https://github.com/ProtossDragoon/paper_implementation_and_testing_tf2/blob/main/docs/img/tfrecord_aug.png?raw=true)

<br><br>

### View TensorBoard

<br>

- Google COLAB 에서 학습을 진행하다 보면 세션이 자주 다운되기 때문에 TensorBoard 만 따로 볼 수 있는 노트북이 필요합니다.
- 정확한 디렉터리의 로그 파일들로부터 TensorBoard 를 띄워주는 노트북입니다.
- 구글 드라이브, 구글 클라우드 스토리지 둘 모두 지원합니다.

![tboard](https://github.com/ProtossDragoon/paper_implementation_and_testing_tf2/blob/main/docs/img/colab_tboard.png?raw=true)

<br><br>

### Qualitative Evaluation Realworld Data

<br>

- Real World 문제를 풀고자 할 때, 내가 real world 에서 수집하는 데이터셋의 레이블이 존재하지 않는 경우가 있습니다. 
- 이런 경우에 매번 데이터셋에 레이블링을 해서 사용하기는 현실적으로 불가능할 때가 많습니다. 
- 당연히 lean 하게 우선적으로 해 보아야 하는 방법은 정성적인 결과물 평가입니다. 
- 이를 통해 대략적인 해상도/augmentation 의 방향/모델의 capacity 등 적합성을 빠르게 평가해볼 수 있습니다.

![qualitative](https://github.com/ProtossDragoon/paper_implementation_and_testing_tf2/blob/main/docs/img/qualitative_result.png?raw=true)

<br><br>

### rosutils

<br>

- ROS 와 딥러닝에 관련된 노트북입니다.

<br><br>
