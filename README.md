# 책 추천 딥러닝 모델 관련 파일 안내

## `book.ipynb`

모델 설계, 학습 및 테스트가 담긴 Python 코드입니다.

이전 과정에 수집된 데이터인 JSON 파일은 저작권 이슈로 제공해 드릴 수 없는 점 양해 부탁드립니다. 이에 따라 해당 코드가 실제로 작동되지는 않습니다.

해당 과정을 거쳐 생성된 SavedModel은 `book-to-books.zip`의 `result`와 동일합니다.

## `book-to-books.zip`

모델 호스팅을 위해 현재 Google Cloud Storage에 실제로 등록된 파일입니다. 해당 압축 파일의 내용은 다음과 같습니다.

- `result` 폴더: `book.ipynb`를 통해 생성된 SavedModel 형태의 모델입니다.
- `requirements.txt`: Python 환경을 구동하기 위한 필요 패키지 목록입니다.
- `main.py`: 모델을 불러와 실행하는 `handler` 함수가 있는 Python 파일입니다.

Google Cloud Functions 기능을 통해 실행될 수 있는 구조이며, HTTP 통신으로 `main.py`의 `handler` 함수가 호출되는 형태입니다.
