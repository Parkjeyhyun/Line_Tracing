자율주행 자동차 구동 코드

1. 도로 인식 코드

2. 도로방향에 따른 방향조작

3. 아두이노 통신방법 구상

4. 라즈베리파이? or 아두이노? or (라즈베리파이 and 아두이노? -> 제작비 초과 및 제작 복잡성으로 배제함)

4-1. 모터드라이버 제어 코드작성 필요 + 배터리 추가 또는 유선으로 공급 고려

4-2. 아두이노 카메라모듈 구매필요 + OpenCV C++ 코드 변환 및 아두이노 메모리 사용량 테스트 필요

--> 라즈베리파이가 더 용이함

목표 : OpenCV를 이용하여 차선을 인식하고 그에따른 방향조작이 가능한 자율주행자동차 모형을 제작


Note

1. 이미지 파일 포멧은 jpg로 통일 @@@ bmp jfif등의 형식에서 오류 발생
