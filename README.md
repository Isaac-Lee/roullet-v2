# 경품 추첨기 프로그램

## 설명

이 프로그램은 FastAPI를 기반으로 한 경품 추첨 웹 애플리케이션입니다. 엑셀 파일(data.xlsx)에 저장된 이메일 목록에서 무작위로 60개의 이메일을 추첨하여 웹 페이지를 통해 표시합니다. 웹 브라우저에서 추첨 버튼을 클릭하면 5초 카운트다운 후 결과가 표시되며, 추첨된 이메일 목록은 전체 이메일 목록과 같은 테마로 보여집니다.

## 주요 기능

- 엑셀 파일(data.xlsx)에서 이름과 이메일을 불러와 웹 페이지에 표시
- "랜덤 추첨" 버튼을 클릭하면 5초 카운트다운 후 무작위로 60개의 이메일을 추첨
- 추첨이 완료된 후에는 "다시 하기" 버튼을 클릭하여 초기화 가능
- 웹 페이지는 어두운 테마를 사용하여 행사의 테마와 일치
- FastAPI 웹 서버를 통해 localhost:8000에서 실행됨

## 요구 사항

- Python 3.8 이상
- 다음 Python 패키지들이 설치되어 있어야 합니다:
  - FastAPI
  - Uvicorn
  - Jinja2
  - Pandas
  - Openpyxl

## 설치 방법

1. **Python 설치**
   - 먼저 Python 3.8 이상이 설치되어 있는지 확인합니다. 설치되지 않은 경우, Python 공식 웹사이트(https://www.python.org/downloads/)에서 다운로드 후 설치합니다.

2. **필수 패키지 설치**
   - 아래 명령어를 사용하여 필요한 패키지들을 설치합니다.
    
   ```bash
    pip install fastapi uvicorn jinja2 pandas openpyxl
   ```

3. **프로젝트 디렉토리 구조**
   - 다음과 같은 구조로 파일들을 준비합니다.

   ```bash
    project-directory/
    │
    ├── app.py               # 메인 실행 파일
    ├── data.xlsx            # 엑셀 파일 (이름, 이메일 리스트)
    └── static/
        ├── index.html       # HTML 파일
        ├── style.css        # CSS 파일
        └── script.js        # JS 파일
    ```

4. **엑셀 파일 준비**
   - data.xlsx 파일에 이름과 이메일을 준비합니다. 엑셀 파일은 두 개의 열로 구성되어 있어야 하며, 첫 번째 열은 name, 두 번째 열은 email이어야 합니다.

## 실행 방법

1. **앱 실행**
   - 터미널에서 프로젝트 디렉토리로 이동한 후 다음 명령어를 입력하여 FastAPI 앱을 실행합니다.

   python app.py

2. **웹 브라우저에서 열기**
   - 프로그램이 실행되면 기본 웹 브라우저에서 http://localhost:8000 주소로 웹 페이지가 자동으로 열립니다.

3. **경품 추첨하기**
   - "랜덤 추첨" 버튼을 클릭하면 5초 카운트다운이 시작되며, 무작위로 60개의 이메일이 추첨되어 화면에 표시됩니다.
   - 추첨이 완료된 후 "다시 하기" 버튼을 클릭하면 전체 이메일 목록 화면으로 돌아갈 수 있습니다.

## 추가 정보

- 이 프로젝트는 FastAPI로 구현되었으며, 정적 파일(index.html, style.css, script.js)은 /static 디렉토리에서 불러옵니다.
- 엑셀 파일은 data.xlsx라는 이름으로 실행 파일과 같은 디렉토리에 위치해야 하며, 프로그램은 엑셀 파일에서 이름과 이메일 정보를 불러와 사용합니다.
