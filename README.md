# SegFormer

SegFormer는 2021년 NVIDIA가 발표한 **Vision Transformer(ViT) 기반 의미론적 분할(Semantic Segmentation) 모델**입니다.

---

## 🔍 주요 특징

### 1. Hierarchical Transformer Encoder
- 기존 ViT는 동일한 크기의 패치를 한 번에 처리하지만,  
  SegFormer는 **다단계 계층 구조**로 해상도를 점차 줄이며 특징을 추출합니다.
- **작은 물체부터 큰 물체까지** 잘 잡아낼 수 있습니다.

### 2. Overlapping Patch Merging
- **겹치는 패치 임베딩** 방식을 사용해 경계 정보 손실을 줄입니다.
- 더 정밀한 특징 맵 생성이 가능합니다.

### 3. Lightweight All-MLP Decoder
- 다른 segmentation 모델처럼 복잡한 디코더 대신,  
  **다층 퍼셉트론(MLP)** 기반의 가벼운 디코더를 사용합니다.
- 멀티스케일 feature를 단순 병합하여 **빠른 추론 속도**와 **낮은 메모리 사용량**을 제공합니다.

### 4. Position Encoding 없음
- 대부분의 Transformer 계열 모델과 달리 위치 인코딩을 사용하지 않습니다.
- **Overlapping Patch**와 **Hierarchical 구조**를 통해 공간 정보를 학습합니다.
- 이미지 크기 변화와 비율 변화에 강합니다.

---


---

## 📊 장점
- **속도와 정확도 균형** (모바일부터 서버까지 적용 가능)
- 복잡한 디코더 없이 **단순하고 빠른 구조**
- 강력한 멀티스케일 특징 추출 능력
- Cityscapes, ADE20K 등에서 **SOTA 성능 달성**

---

## 📦 활용 예시
- **자율주행**: 도로, 차선, 보행자 분할
- **위성 이미지 분석**: 토지 피복 분류
- **의료 영상 분석**: 장기·조직 분리
- **로봇 비전**: 실시간 환경 인식

---

## 📚 참고 자료
- [SegFormer 논문 (arXiv)](https://arxiv.org/abs/2105.15203)
- [mmsegmentation 구현체](https://github.com/open-mmlab/mmsegmentation)
- [Hugging Face Transformers SegFormer](https://huggingface.co/docs/transformers/model_doc/segformer)

# Adas를 이용한 텐서 rt와 Pytoch 비교
https://docs.google.com/document/d/179l9DqTYZJ1oGDWNA-TGtFZjs1PprWVoVlV-dTw_XrM/edit?tab=t.0
