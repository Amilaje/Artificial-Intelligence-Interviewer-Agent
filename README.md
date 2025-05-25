# LangGraph 기반 AI 면접관 Agent

## Outline
본 프로젝트는 LangChain과 LangGraph를 활용하여  
이력서 기반 맞춤형 질문을 생성하고 피드백을 제공하는 **AI 면접관 Agent**를 구축한 팀 프로젝트입니다.

---

## Objects
- 사용자의 이력서를 바탕으로 자동화된 질문 생성
- 답변 평가 및 피드백 제공
- Gradio UI를 통해 실제 인터뷰 환경과 유사하게 구성
- LangGraph 기반의 멀티 Node 파이프라인 구현

---

## My Role
- 팀 프로젝트 총괄 (PM)  
- 전체 코드베이스 1차 설계 및 배포  
- Vector DB 구축 및 이력서 기반 검색 시스템 구성
- 인터뷰 질문-응답 흐름 설계 및 최종 검토

---

## Project configuration
1. **이력서 업로드** → 문서 요약 및 키워드 추출
2. **질문 생성 Node** → 역할별 질문 전략에 따라 문항 구성
3. **답변 평가 Node** → GPT 기반 평가 및 피드백 출력
4. **최종 결과 출력 Node** → 점수, 피드백, 추가 질문 제공

---

## Team composition
| 이름 | 역할 |
|------|------|
| 김영진, 고현민 | 질문 생성 Node |
| 박진우, 정민기 | 답변 평가 Node |
| 동민아, 정재은 | 피드백/출력 Node |
| 이승환 | 보조 로직 & 테스팅 |
| **최진호 (PM)** | Vector DB, 인터뷰 흐름 설계, 최종 코드 정리 |

---

## Framework

- LangChain, LangGraph, OpenAI API
- Gradio (인터뷰 UI)
- ChromaDB (벡터 기반 검색)
- Python, Jupyter Notebook

---

## File

| 파일명 | 설명 |
|--------|------|
| `Step1_개인과제_AI면접관 Agent v1.0.ipynb` | 초기 개인 개발 버전 |
| `Step2_팀과제_AI면접관 Agent v2.0.ipynb` | 팀 고도화 버전 (Gradio 포함) |
| `Resume_sample.pdf` | 테스트용 이력서 |
| `requirements.txt` | 실행 환경 패키지 목록 |

---

## How To Used

1. 패키지 설치
```bash
pip install -r requirements.txt
노트북 실행
```
```bash

jupyter notebook Step2_팀과제_AI면접관 Agent v2.0.ipynb
실행 후 Gradio 링크 접속
→ 로컬 인터뷰 시뮬레이션 환경이 브라우저에 출력됩니다.
```
---

## 참고 사항

- 본 프로젝트는 KT Aivle School 실습 과제로 진행되었습니다.
- 실제 이력서를 기반으로 Agent가 질문 생성부터 평가까지 자동 수행합니다.
- 향후 Retrieval 전략 개선 및 다중 이력서 대응 기능 고도화 예정입니다.
