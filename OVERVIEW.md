# Strategic Review Analysis 프로젝트

이 프로젝트는 기업의 소비자 리뷰 데이터를 활용하여 전략적인 분석을 자동화하는 것을 목표로 합니다. 다양한 감정 분석 기법과 AI 모델을 사용하여, 리뷰 데이터를 기반으로 소비자 불만 요소를 도출하고, 이를 기업의 전략적 의사결정에 반영할 수 있도록 돕습니다.

## 프로젝트 구성

본 프로젝트는 총 5개의 주요 폴더로 구성되어 있으며, 각각의 폴더는 특정한 분석 및 자동화 작업을 수행합니다.

1. **01_KoBERT_Fine-Tuning & 기업 리뷰 감정 분석**
   - AI-HUB 감정 분석 데이터를 활용하여 KoBERT 모델을 파인튜닝하고, 이를 기업의 리뷰에 적용하여 감정을 예측하는 프로젝트입니다.

2. **02_감정 라벨 재태깅 시스템 설계 및 구현 (KoBERT + Cosine Similarity)**
   - 별점 기반 감정 라벨링의 한계를 해결하기 위해, KoBERT 임베딩과 코사인 유사도를 활용하여 리뷰의 감정을 재정의하는 시스템을 설계하고 구현했습니다.

3. **03_감정 분석 모델 비교 기반 기업 전략 분석 (KCC 학술지 정리)**
   - 한국정보과학회(KCC)에 제출한 논문을 바탕으로 KoBERT와 KLUE-BERT를 비교하여 기업의 전략적 의사 결정을 지원하는 분석을 수행한 내용입니다.

4. **04_Claude 기반 부정 리뷰 분석 & 마케팅 전략 도출**
   - LLM인 Claude를 활용하여 부정 리뷰를 분석하고, 이를 기반으로 마케팅 전략을 도출하는 실험입니다.

5. **05_ABSA 기반 SWOT 분석 및 뉴스레터 자동화**
   - GPT 기반의 ABSA(Aspect-Based Sentiment Analysis) 기법을 활용하여 리뷰 데이터를 분석하고, SWOT 분석과 뉴스레터 생성을 자동화하는 파이프라인을 구축한 프로젝트입니다.

## 주요 기술 스택

- **Python, PyTorch**: 모델 학습 및 데이터 처리
- **KoBERT, KLUE-BERT, GPT, Claude**: 감정 분석 및 전략 분석
- **HuggingFace, Langchain, Streamlit**: 데이터 파이프라인 및 시각화
- **Scikit-learn, Pandas**: 데이터 처리 및 모델 성능 평가

이 프로젝트는 다양한 AI 모델을 결합하여 소비자 리뷰 분석을 고도화하고, 이를 전략적 의사결정에 활용할 수 있는 자동화 시스템을 구현하는 것을 목표로 했습니다.

---

## 📁 전체 프로젝트 구조

📁 strategic-review-analysis
├── 01_kobert_finetuning_prediction/
├── 02_kobert_embedding_cosine_relabeling/
├── 03_kcc_paper_model_comparison/
├── 04_claude_marketing_suggestion/
├── 05_absa_swot_newsletter/
└── OVERVIEW.md


## 프로젝트 진행 기간

- 2024년 3월 ~ 2024년 10월

## 프로젝트 목표

- 소비자 리뷰 분석을 통해 기업의 전략적 의사결정을 지원할 수 있는 시스템을 구축
- AI 모델을 사용하여 리뷰의 감정을 예측하고, 이를 바탕으로 전략적 제안을 자동으로 생성
- 리뷰 데이터를 기반으로 기업이 고객의 불만 요소를 파악하고, 이를 해결하기 위한 전략을 도출