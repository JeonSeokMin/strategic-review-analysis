# Strategic Review Analysis — 프로젝트 개요

소비자 리뷰를 활용해 **감정 분류 → 라벨 품질 탐색 → 고객 불만 분석 → LLM 기반 전략 제안**으로 분석 범위를 확장한 연구·실험 모음입니다.

- **전체 활동 기간:** 2024.03~2024.10
- **저장소 성격:** 관련 주제의 개별 프로젝트 5개를 모은 아카이브
- **공통 목표:** 소비자 리뷰를 기업의 제품 개선 및 전략적 의사결정 지원 정보로 연결할 가능성 탐색

## 프로젝트별 상세 안내

| 폴더 | 시기 및 성격 | 내용 |
| --- | --- | --- |
| [01_kobert_finetuning_prediction](./01_kobert_finetuning_prediction/README.md) | 2024.03~06, 캡스톤디자인2 | AI-HUB 데이터 전처리·언더샘플링, KoBERT 학습 및 Q사 리뷰 감정 예측 |
| [02_kobert_embedding_cosine_relabeling](./02_kobert_embedding_cosine_relabeling/README.md) | 캡스톤 관련 후속 탐색 | 별점과 텍스트 감정의 불일치 문제를 고려한 KoBERT 임베딩·코사인 유사도 기반 재라벨링 |
| [03_kcc_paper_model_comparison](./03_kcc_paper_model_comparison/README.md) | 2024.05~06, KCC 논문 | KoBERT·KLUE-BERT 비교, Q사 리뷰 분석 모델 선정 및 부정 키워드 분석 |
| [04_claude_marketing_suggestion](./04_claude_marketing_suggestion/README.md) | 2024.07~08, 교내 SW 경진대회 | 부정 리뷰를 Claude로 분석하여 불만 요인과 마케팅 개선안 생성 |
| [05_absa_swot_newsletter](./05_absa_swot_newsletter/README.md) | 2024년 하반기, 교내 AI 경진대회 | GPT-4o 기반 ABSA, SWOT, 뉴스 요약 및 시장 전망 워크플로 |

## KCC 연구의 모델 선정과 한계

실제 Q사 리뷰 분석에 적용할 모델을 선정해야 했기 때문에, KoBERT와 KLUE-BERT의 당시 비교 실험 결과를 바탕으로 **KoBERT를 선택**했습니다. 이 선택은 연구 수행을 위한 모델 선정이지, 실환경에서의 우수한 성능이 충분히 입증되었다는 뜻은 아닙니다.

당시 Q사 리뷰의 별점 기반 라벨은 긍정 18,479건, 부정 71건으로 극심한 불균형을 보였고, 별점과 리뷰 내용의 감정이 다를 수 있다는 한계도 있었습니다. 따라서 높은 F1-score를 실제 부정 리뷰 탐지 능력으로 일반화하지 않습니다.

이후 재라벨링 실험은 이러한 문제를 탐색하기 위한 시도이며, 라벨 정확도 개선 효과가 독립적으로 검증된 것은 아닙니다.

## 활용 기술

Python, Pandas, PyTorch, Hugging Face Transformers, KoBERT, KLUE-BERT, Scikit-learn, Claude, GPT-4o, LangChain, FAISS, Google Serper API, Streamlit

## 공개 범위

기업 리뷰 원본 및 일부 모델·결과 파일은 비공개입니다. 공개 노트북은 당시 작업을 재구성하거나 아카이빙한 자료가 포함되어 있으며, 전체 실험을 즉시 재현할 수 있다는 보장은 없습니다.

저장소 첫 화면용 요약은 [README.md](./README.md)를 참고해 주세요.
