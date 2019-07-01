# Deep Learning with Cinematic Rendering: Fine-Tuning Deep Neural Networks Using Photorealistic Medical Images

## Abstract

Deep learning은 의료 영상을 해석하는 강력한 인공지능 도구로 사용. 하지만 이런 방법은 training 중 high-quality annotations된 의료 이미징 데이터의 부족은 성능을 제한함.
또한 의료 데이터는 정보 보호 문제, annotation할 수 있는 전문가의 부재, 제한된 상황, 비용등으로 획득이 어려움.

이 논문에서 deep learning 학습에서 **cinematic rendering을 응용한 applications**을 제안하며, 내시경 검사에서 monocular depth 추정을 위해, **cinematic 방식으로 rendering 된 CT 데이터를 사용해 fine-tune하는 네트워크를 제안함**.

우리는 실험적으로 다음과 같은 것을 입증함. :

(a) synthetic 데이터에 대해 train 해도, **photorealistic cinematically rendering된 데이터에 의해 fine-tune된 CNN은 실제 의료영상에 잘 적응되고, fine-tune 하지 않은 네트워크와 바교할 때 보다 robust performance 보임.**

(b) 이러한 fine-tune 네트워크는 optimal solution에 도달하기 위해 보다 적은 데이터를 필요로 함.

(c) **동일한 장면의 다양한 photorealistic rendering된 데이터를 사용하여 fine-tunning하면 patient-specific information을 학습하지 않아 모델의 generalizability를 도움**.

우리의 empirical evaluation에 따르면 cinematically rendered data로 fine-tune된 네트워크는 그렇지 않은 네트워크에 비해 에러가 56.87 % 감소하였고, 실제 돼지 colon endoscopy image에 대해 27.49%의 적은 오류로 심도를 예측함.

![figure 1](/images/crp/1.png)
***-photorealistic cinematically rendering-
(Cinematic Rendering in CT: A Novel, Lifelike 3D Visualization Technique)***

![figure 1](/images/crp/2.png)
![figure 1](/images/crp/3.png)


정리 : 

3D 모델링을 통해 생성된 데이터로 1차 학습.

CT 실제 모델을 photorealistic cinematically rendering을 사용해 사실적인 다양한 데이터를 획득하고, 2차 (fine-tune) 학습.

photorealistic cinematically rendering는 보다 사실적인(실제 데이터가 가까운) 데이터를 생성할 수 있으며, 보다 generalization 하다.
