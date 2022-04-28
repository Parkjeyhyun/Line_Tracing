자율주행 자동차 구동 코드

진행 상태 : 진행중

1. 도로 인식 코드

2. 도로방향에 따른 방향조작

3. 아두이노 통신방법 구상

4. 라즈베리파이? or 아두이노? or (라즈베리파이 and 아두이노? -> 제작비 초과 및 제작 복잡성으로 배제함)

4-1. 모터드라이버 제어 코드작성 필요 + 배터리 추가 또는 유선으로 공급 고려

4-2. 아두이노 카메라모듈 구매필요 + OpenCV C++ 코드 변환 및 아두이노 메모리 사용량 테스트 필요

--> 라즈베리파이가 더 용이함

목표 : OpenCV를 이용하여 차선을 인식하고 그에따른 방향조작이 가능한 자율주행자동차 모형을 제작

Code

1. 비디오 불러오기

2. 흰색, 황색 검출

3. 마스크 적용 및 Gaussian blur & canny Edge 적용

4. ROI 적용

5. Hough 변환

6. 차선 예측 -> 선형회귀 이용

7. 4개 pts를 이용하여 4각형 폴리곤으로 차선영역을 지정

8. 차선 시각화.


Note

1. 이미지 파일 포멧은 jpg로 통일 @@@ bmp jfif등의 형식에서 오류 발생 -> 이미지 형식변환으로 해결가능하나 당장 급한 문제가 아니라서 귀찮고 !2022-01-20

2. 메인 코드 작성 및 파일 분활 및 분류 !2022-01-21

3. !@!@테스트 이미지 추가 및 정확도 상승 필요 -> 코드초기화...... 코드를 처음부터 동영상테스트로 변경 !2022-01-21

4. canny.py에서 canny적용후 gaussian canny 한번 더 적용 @후반에 테스트 필요 -> 실패 한번의 적용이 더 효과적인 듯 !2022-01-23

5. line.py 에서 적합한 선분 찾기에서 에러 발생 !2022-01-23

6. 차선 예측 코드 작성 시작  !2022-01-24

7. 차선 예측 및 시각화 코드 완성 !2022-01-27

8. 갑자기 시작한 프로젝트 갑자기 멈추다.......(그냥 내 마음대로...어차피 중요한 코드는 다 작성 나머지 귀찮아~) !2022-01-29

9. 곡선문제를 개선하기 위해서 프로젝트 다시 시작 (오픈랩에서 보여진다니..... 좀더 개선하고 싶어짐) !2022-04-26

10. y축을 일정한 크기로 나눠서 각각의 ROI별로 선을 검출				!2022-04-28
		만약 중간에 ROI가 검출되지 않으면 그 부위는 빼고 상위 ROI랑 연결함 휴...
		원근법때문에 상위 ROI의 간격이 짧아지므로 상위 간격은 좁게 설정!
		+) 계층간의 기울기 조정은 고려@@

