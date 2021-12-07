# echocardiography_analysis_image
** 해당 코드는 jupyter 에서 실행되는 코드입니다.
    
test_code.ipynb 파일을 실행합니다.

------

### 테스트 실행 가이드



<ol>
1.데이터 경로 설정

2.가중치 경로 설정

3.데이터 불러오기

4.평가

</ol>

-------

<br>

1. 데이터 경로 설정

두 번 째 코드 블록의 데이터 경로를 수정해줍니다.

train, validation의 A2C, A4C 폴더 경로를 입력합니다.

코랩에서 실행할 경우 첫 번째 블록의 drive mount도 수행해줍니다.

ex)

    a2c_train_PATH = '../echocardiography/train/A2C/'# train a2c

    a4c_train_PATH = '../echocardiography/train/A2C/'# train a4c

    a2c_test_PATH =  '../echocardiography/validation/A2C/' # test a2c

    a4c_test_PATH =  '../echocardiography/validation/A4C/'  # test a4c

<br>

2. 가중치 경로 설정

같은 블록의 weights 경로도 수정해줍니다.

a2c와 ac4를 잘 구분해주세요.

<br>

3. 데이터 불러오기

이제 처음부터 'A2C 모델 학습하기' 이전 까지의 블록을 전부 실행합니다.

데이터와 평가에 필요한 함수가 로드됩니다.

<br>

4. 평가

'A2C 모델 학습하기', 'A4C 모델 학습하기', '가중치 불러오기' 부분은 건너뛰고

'가중치 불러와서 모델 테스트하기' 부터 끝까지 실행합니다.

가중치를 불러오고 데이터를 평가하여 출력합니다.

결과 예시 ( BCE loss, accuracy, DSC, JI ))

    4/4 [==============================] - 37s 8s/step - loss: 0.0123 - accuracy: 0.9953 - dice_coef: 0.9535 - jaccard: 0.9114
    [0.012305477634072304,
    0.9953113198280334,
    0.9534980058670044,
    0.9114193916320801]