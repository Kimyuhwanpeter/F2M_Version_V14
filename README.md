# F2M_Version_V14
* 리눅스로 환경
* 본컴 및 서브컴에 실험 본컴퓨터 (29 epochs)로는 encoder residual block x 5, 서브컴(19 epchs)은 x 7
* Depth wise + point wise (Depth-wise Separable Convolution, Xception model에 사용했던 기법)을 Residual block (Dilated rate 한 블록을 거칠때마다 3씩 증가.)에 적용(채널에 대한 정보 + spatial space 정보를 각각 분리한것). Attention 추가 (gradient image를 구한 후 sigmoid 처리). 1x1 Depth wise conv encoder 단에 추가. Decoder에 reverse residual block (Dilated rate 한 블록을 거칠때마다 4씩 증가.) 추가. Encoder에 있는 각각의 conv layer에 attention 추가(gradient image 후 sigmoid)
* 나이에 대한 loss 새롭게 구성 (F2M_model_V9_2 와 동일)
* Content loss 추가 설계 (Content란 영상의 주성분이 아닌 그 외 배경성분이라고 가정)



