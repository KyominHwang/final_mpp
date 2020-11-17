[secondPage.java]
1. 주요 기능 : 
-> firstpage에서 선택한 날짜의 할 일들을 시간표로 출력해준다.
-> 만약 firstpage의 날짜가 변경되면 변경된 날짜의 시간표를 출력한다.(황교민학우의 도움)
2. 구현
-> 1. onCreateView : 초기 화면의 상태를 지정
	- nullActionIdx(nullcontent의 index) 초기화
	- pieChart : 시간표를 나타내는 piechart
-> 2. changeState : database를 읽어 시간표를 출력
	- timetable : 하루 24시간을 10분단위로 쪼개 144개의 index로 나누어 각각의 index에는 해당하는 시간동안 
		     완료한 content를 저장한다.
		     ex) 02시 10분 >> 2 x 60 +10 = 130 (10분단위로 쪼개지므로 뒤에 있는 0의 값은 삭제) >> index 13 (02시 10분~ 02 20분)
		          00시 00분 ~ 02시 10분 까지 공부라는 content를 완료했을 경우 0부터 12까지의 index에 공부가 저장된다.
	- nullActionIdx : 아무 content도 하지 않은 시간대의 piechart의 색을 같은 색으로 지정하기 위해 할 일 index를 따로 생성해서
		          nullActionIdx에 따로 저장해 처리한다. (황교민학우의 도움)
*전체적인 UI는 김지원 학우의 도움을 받았습니다.


[Search.java]
1. 주요 기능 :
-> 검색창에 특정 문자를 검색하면 daily와 monthly에서 해당 문자가 포함된 데이터를 읽어와 화면에 출력해준다.

2. 구현
* 전체적인 UI는 김지원 학우의 도움을 받았습니다.
