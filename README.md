# 컴퓨팅핵심 실습 자료

2026학년도 2학기 컴퓨팅핵심 수업의 실습 노트북과 조교용 웹 안내 자료입니다.
학생들은 Elice 코딩 플랫폼에서 문제를 풀고, 조교는 노트북과 웹 안내 화면을 활용해 수업을 진행합니다.

## 폴더 구조

```text
.
├── practice/                         # 주차별 실습 노트북
│   ├── 1주차 실습.ipynb
│   ├── 2주차 실습.ipynb
│   └── 3주차 실습.ipynb
├── docs/                             # 이번 학기 강의계획서와 제작 기준
│   ├── 2026-2학기 컴퓨팅핵심 강의계획서.pdf
│   ├── 실습_자료_제작_가이드.md
│   └── 웹사이트_제작_가이드.md
├── images/                           # 주차별 문제 그림 원본
│   ├── week1/                        # week1_chal1.png 등 (4개)
│   ├── week2/                        # week2_chal1.png 등 (5개)
│   └── week3/                        # week3_chal1.png 등 (5개)
├── website/
│   ├── main.html                      # 1~15주차 주제와 실습 목차
│   ├── week1_prac.html
│   ├── week2_prac.html
│   └── week3_prac.html
├── tests/                            # 로컬 전용 검증 자료 (GitHub 업로드 제외)
├── 2026-1학기 이론 교안/               # 로컬 전용 참고 자료 (GitHub 업로드 제외)
├── .github/workflows/pages.yml        # GitHub Pages 자동 배포
├── README.md
└── .gitignore
```

## 주차별 자료

| 주차 | 내용 | 실습 노트북 | 웹 안내 |
| --- | --- | --- | --- |
| 1주차 | Elice 익히기와 파이썬 워밍업 | [1주차 실습](<practice/1주차 실습.ipynb>) | [1주차 웹 안내](website/week1_prac.html) |
| 2주차 | 파이썬 심화 문법과 필수 기능 | [2주차 실습](<practice/2주차 실습.ipynb>) | [2주차 웹 안내](website/week2_prac.html) |
| 3주차 | 클래스와 객체지향 프로그래밍 입문 | [3주차 실습](<practice/3주차 실습.ipynb>) | [3주차 웹 안내](website/week3_prac.html) |

노트북에는 문제 설명, 그림, 학생용 스켈레톤 코드와 조교용 Solution 코드가 함께 들어 있습니다.

## 웹 안내 사용하기

[배포 사이트](https://smkim37.github.io/Computing-2026-Fall/)에서 웹 안내를 이용할 수 있습니다. 최초 배포가 완료된 뒤 접속할 수 있습니다.

저장소를 내려받은 뒤 [주차별 실습 목차](website/main.html)를 웹브라우저에서 엽니다.
1~15주차의 요일과 주제를 확인하고, 완성된 1~3주차 실습으로 이동할 수 있습니다. 아직 제작하지 않은 주차는 비활성화되어 있습니다.
각 실습의 상단에서 **전체 주차**를 누르면 목차로 돌아갑니다.
Windows와 macOS 데스크탑에서 파일을 더블 클릭해 사용할 수 있습니다.
그림과 글꼴이 HTML에 포함되어 있어 별도 설치나 서버, 인터넷 연결이 필요하지 않습니다.
GitHub의 파일 보기 화면에서는 HTML이 실행되지 않으므로 파일을 내려받아 여세요.

각 문제는 **문제 이해 → 코드 구현 → 실행 시각화** 순서로 진행합니다.
코드 구현 화면에서는 다음 단계로 넘길 때 코드가 한 줄씩 입력되며, 실행 화면에서는 변수, 자료구조 또는 객체의 변화를 확인할 수 있습니다.
코드 복사 버튼으로 현재 화면의 코드를 복사할 수 있습니다.

| 조작 | 기능 |
| --- | --- |
| `→` 또는 `Space` | 다음 단계 |
| `←` | 이전 단계 |
| `F` | 전체 화면 전환 |
| 상단 문제 메뉴 | 원하는 문제로 이동 |

## 노트북 열기

Python 3 환경에서 저장소 루트를 작업 폴더로 열고 실행합니다.

```bash
python -m pip install notebook
python -m notebook
```

열린 Jupyter 화면에서 `practice/`의 노트북을 선택합니다.
환경에 따라 `python` 대신 `python3` 또는 `py`를 사용하세요.
노트북의 그림 경로는 `../images/week{n}/week{n}_chal{k}.png` 또는 `../images/week{n}/week{n}_extra{k}.png`입니다.
예를 들어 1주차 첫 도전문제는 `../images/week1/week1_chal1.png`를 참조하므로 `practice/`와 `images/`의 상대 위치와 주차별 하위 폴더를 유지해야 합니다.
새 주차의 그림은 `images/week{n}/` 폴더를 만들어 저장합니다.
웹 안내는 그림을 HTML 내부에 포함하므로 원본 그림의 폴더 이동에 영향을 받지 않습니다. 그림 내용을 바꾸면 해당 HTML의 포함 이미지도 갱신해야 합니다.

## 자료 제작과 검증

새 자료를 만들 때는 [이번 학기 강의계획서](<docs/2026-2학기 컴퓨팅핵심 강의계획서.pdf>)와 [실습 자료 제작 가이드](docs/실습_자료_제작_가이드.md)를 참고합니다.

웹 안내 제작에는 [웹사이트 제작 가이드](docs/웹사이트_제작_가이드.md)를 참고합니다.

`tests/`와 `2026-1학기 이론 교안/`은 로컬에서만 보관하며 GitHub 저장소에는 포함하지 않습니다. 아래 검증 명령은 `tests/`가 있는 로컬 작업 폴더에서 실행합니다.

1~2주차 실습 코드, 노트북 구성, 이미지와 웹페이지의 원본 및 출력 검증은 저장소 루트에서 실행합니다.

```bash
python -m pip install nbformat pillow
python -m unittest discover -s tests -v
```

실제 브라우저의 오프라인 이동, 예제 재생, 초기화, 복사 대체 기능과 반응형 화면은 다음으로 검사합니다.

```bash
python -m pip install playwright
python -m playwright install chromium
python tests/check_practice_browser.py -v
```

`.gitignore`는 노트북 체크포인트, Python 캐시, 가상환경과 로컬 도구 설정 등을 Git 추적에서 제외합니다.
실습 노트북, 그림, `docs/`의 강의계획서 PDF와 수업용 HTML은 저장소에 포함합니다.

## GitHub Pages 배포

저장소 **Settings → Pages → Build and deployment → Source**를 **GitHub Actions**로 설정합니다.
`main` 브랜치에 푸시하면 `.github/workflows/pages.yml`이 `website/`의 파일을 배포합니다. 필요하면 **Actions → Deploy GitHub Pages → Run workflow**에서 수동으로 배포할 수 있습니다.

첫 화면의 원본은 `website/main.html`입니다. 배포 과정에서 같은 내용을 `index.html`로 복사하며 `main.html`도 유지하므로 주차별 페이지의 목차 이동 링크가 계속 동작합니다. 웹에는 `website/`의 파일만 배포합니다.
