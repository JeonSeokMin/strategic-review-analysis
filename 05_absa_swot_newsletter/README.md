# 05. ABSA 기반 SWOT 분석 및 뉴스레터 자동화

📅 **2024 하반기 교내 ChatGPT 활용 AI 경진대회용 프로젝트**

---

## 📌 개요

본 프로젝트는 리뷰 데이터를 기반으로 다음과 같은 고도화된 전략 분석 흐름을 자동화하는 데 목적이 있습니다:

> **ABSA → SWOT 분석 → 뉴스 요약 → 향후 전망 → 뉴스레터 생성**

---

### ✨ 왜 ABSA인가?

기존 감정 분석은 그저 리뷰가 긍정/부정인지 분류하는 데 그쳤지만,  
**Aspect-Based Sentiment Analysis (ABSA)** 를 활용하면  
- 제품의 어떤 **측면(aspect)** 에 대해  
- 어떤 **의견(opinion)** 이  
- 어떤 **감정(sentiment)** 으로 표현되었는지를  
구체적으로 파악할 수 있습니다.

👉 이 정보는 SWOT 분석이나 **전략적 의사결정**으로 연결하기에 매우 유용합니다.

---

GPT-4o와 Langchain, Supper API 등을 활용하여, 단순 감정 분석을 넘어서  
**의사결정에 활용 가능한 전략 보고서 수준의 콘텐츠 생성**을 목표로 합니다.

---

## 🔍 전체 흐름 요약

1. **ABSA 분석**  
   - GPT-4o를 활용하여 리뷰에서 Aspect, Opinion, Sentiment 추출

2. **SWOT 생성**  
   - ABSA 결과를 바탕으로 LLM이 SWOT 인사이트 자동 생성

3. **뉴스 수집 및 요약**  
   - FAISS 기반 검색 + Supper API 뉴스 크롤링 → GPT 요약

4. **향후 전망 도출**  
   - 수집된 정보 기반 GPT 분석을 통해 향후 제품 브랜드 전망 생성

5. **뉴스레터 생성**  
   - 전체 내용을 사용자에게 전달 가능한 콘텐츠 형태로 재구성

---

## 🧠 사용 기술

- **OpenAI GPT-4o**: ABSA 분석, 뉴스 요약, SWOT, 시장 전망 도출
- **Langchain**: 체인 구성 및 프롬프트 관리
- **Google Serper API**: 뉴스 기사 검색
- **FAISS**: 뉴스 문서 임베딩 및 벡터 검색
- **Streamlit** (초기 버전에서 사용): 대시보드 형태의 시각화

---

## 🖼️ 분석 결과 예시

📎 분석 전 과정을 하나로 담은 결과 이미지:

![ABSA_SWOT_newsletter](./results/ABSA_SWOT_newsletter.png)

> ABSA 감정분석 → SWOT 분석 → 기회/위협 뉴스 요약 → 향후 전망까지 한 번에 확인 가능

---

## 📁 폴더 구조 예시

```
05_absa_swot_newsletter/
├── code/ # 주요 분석 로직 (4개 파일로 분할)
│ ├── absa_analysis.ipynb # ABSA 수행
│ ├── swot_generator.ipynb # SWOT 분석 수행
│ ├── news_summerizer.ipynb # 키워드 기반 뉴스 검색 및 요약
│ └── market_outlook.ipynb # 향후 시장 전망 도출
├── results/
│ └── ABSA_SWOT_newsletter.png # 실제 발표 시 사용된 결과 이미지
├── .env.example # 필요한 API KEY 예시 템플릿
└── README.md # 현재 문서
```

---

## 🔐 환경변수 설정 (.env)

```
OPENAI_API_KEY=your_openai_api_key
SERPER_API_KEY=your_google_serper_key
```

> `.env.example` 파일 참고해서 `.env` 따로 생성 필요

---

## 🚫 실행 관련 유의사항

- 본 프로젝트는 현재 직접 실행이 불가능합니다.
- 이유:
  - 당시 대회 제공 API Key 및 내부 모듈 (예: Supper, Crawling 모듈) 미보유
  - 일부 Web 기반 결과 재현 불가 가능성 있음
- 따라서 현재 코드는 **워크플로우 기록 및 코드 구조 아카이빙 목적**으로 남겨져 있습니다.

---

## 🙋🏻 담당 역할

- ABSA / SWOT / 뉴스 수집 / 콘텐츠 생성 전체 파이프라인 설계 및 연결
- 프롬프트 설계 및 체인 연결
- 전체 자동화 구조 Streamlit 대시보드 구현
- 실험 결과 정리 및 시각화

---

## 🏁 마무리

이 프로젝트는 단순 감정분석을 넘어서 **LLM 기반 전략 분석 자동화의 실현 가능성**을 보여준 실험입니다.  
실제 기업 리뷰를 바탕으로 사용되었으며, 향후 다양한 인사이트 분석 파이프라인으로 확장 가능합니다.
