# 🧠 AI Research Learning

![Python](https://img.shields.io/badge/Python-3.11-3776AB?logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-2.11-EE4C2C?logo=pytorch&logoColor=white)
![CUDA](https://img.shields.io/badge/CUDA-12.8-76B900?logo=nvidia&logoColor=white)
![WSL](https://img.shields.io/badge/WSL2-Ubuntu_22.04-E95420?logo=ubuntu&logoColor=white)
![VS Code](https://img.shields.io/badge/VS_Code-WSL-007ACC?logo=visualstudiocode&logoColor=white)

> 단계별 학습 기록

---

## 📌 About

2026년 문화체육관광 R&D 과제 **"AI기반 실시간 대화 분석 및 맥락정리 기술개발"** 에 참여하면서, 연구에 필요한 기술들을 단계적으로 학습한 기록입니다.

XR(VR/AR) 환경에서 다자간 대화 시 **표면과 속내의 괴리**를 멀티모달 AI로 포착하는 게 최종 목표예요.

예시:
- 🗣️ "네 좋아요" + 💓 심박 스트레스 → **강요된 동의**
- 🗣️ 칭찬 말투 + 🙅 팔짱 + 👀 눈 굴림 → **비꼬는 표현 (Sarcasm)**

---

## 🚧 현재 진행 중

> *브*02_huggingface** — Transformers 라이러리로 첫 모델 돌려보기

---

## 📂 폴더 구조

```
learning/
├── 01_pandas/             ✅ 완료
│   ├── pandas_meeting_analysis.ipynb       # boolean indexing
│   ├── pandas_time_alignment.ipynb         # merge_asof
│   └── pandas_groupby_aggregation.ipynb    # groupby + agg
│
├── 02_huggingface/        🚧 진행 중
│   └── ...
│
└── (이후 추가 예정)
```

---

## 🗺️ 학습 로드맵

### 🥇 1순위 — 필수

| 폴더 | 주제 | 상태 |
|------|------|------|
| `01_pandas` | 데이터 분석 기초 (boolean indexing, `merge_asof`, `groupby`) | ✅ 완료 |
| `02_huggingface` | Transformers 입문, 감정분석 모델 | 🚧 진행 중 |
| `03_lora` | LLaMA-3 LoRA 파인튜닝 | ⏳ 예정 |

### 🥈 2순위 — 모달리티별

| 폴더 | 주제 |
|------|------|
| `04_librosa` | 음성 처리 (MFCC) |
| `05_mediapipe` | 표정 / 제스처 인식 |
| `06_mne` | 뇌파 (EEG) 분석 |

### 🥉 3순위 — 심화

| 폴더 | 주제 |
|------|------|
| `07_rlhf` | 인간 피드백 기반 강화학습 |
| `08_rag` | 벡터 DB + RAG |
| `09_argument_mining` | 논증 추출 |

---

## 💡 학습 원칙

이 레포의 코드는 **튜토리얼 베끼기가 아닌, 의심하고 응용한 결과물**입니다.

- 🔍 **"왜?" 라는 의심을 던집니다.**
  - "이 값 어디서 왔지?", "이거 정말 같은 거 맞나?" 같은 질문을 자주 코드 주석에 남겨요.
- 🎯 **본인 시나리오로 응용합니다.**
  - 영상/문서에서 본 예제를 그대로 따라치지 않고, 우리 연구 컨텍스트(회의 분석, 강요된 동의)에 맞춰 변형해요.
- 💪 **챌린지는 스스로 풉니다.**
  - 답을 받지 않고 힌트로만 풀어내는 방식을 선호해요.
- 📝 **변수명 + 주석에 신경 씁니다.**
  - 6개월 뒤의 본인이 봐도 이해할 수 있도록.

---

## 🧾 Commit Convention

이 레포의 커밋 메시지는 [Conventional Commits](https://www.conventionalcommits.org/) 컨벤션을 따릅니다.

### 형식

```
<type>: <description>

[optional body]
```

### Type 종류

| Type | 용도 | 예시 |
|------|------|------|
| `feat` | 새 기능 / 새 학습 노트북 추가 | `feat: huggingface 감정분석 노트북 추가` |
| `fix` | 버그 / 코드 오류 수정 | `fix: merge_asof direction 옵션 수정` |
| `docs` | 문서 변경 (README, 주석 등) | `docs: 학습 로드맵 업데이트` |
| `refactor` | 코드 로직 변화 없이 구조 개선 | `refactor: groupby 예제 셀 분리` |
| `style` | 포맷팅, 변수명 변경 등 | `style: df → meeting_df로 변수명 변경` |
| `chore` | 셋업, 설정, 기타 잡일 | `chore: ML 프로젝트용 .gitignore 추가` |
| `test` | 테스트 코드 | `test: sliding window 함수 단위 테스트 추가` |
| `perf` | 성능 개선 | `perf: numpy 벡터화로 루프 최적화` |

### 규칙

- ✅ **`type`은 영문 소문자**, **`description`은 한글** (또는 영문 혼용 가능)
- ✅ `type` 뒤에 콜론(`:`) + 공백
- ✅ 50자 이내 권장
- ✅ 마침표(`.`) 없이 끝내기
- ✅ 한 커밋엔 **하나의 의미**만 담기
- ✅ 영문 단독으로도 가능: `fix: typo in README`

---

## 🛠️ 환경

| 항목 | 버전 / 정보 |
|------|------------|
| **OS** | Windows 11 + WSL2 (Ubuntu 22.04) |
| **Python** | 3.11 (Miniconda `ai` 환경) |
| **GPU** | NVIDIA RTX 5070 (Blackwell, sm_120) |
| **CUDA** | 12.8 |
| **PyTorch** | 2.11.0 + cu128 |
| **에디터** | VS Code (WSL 모드) |

---

## 🔗 Links

- 📝 **velog:** [@xorms](https://velog.io/@xorms/posts)
- 💼 **GitHub:** [@park-taegeun](https://github.com/park-taegeun)