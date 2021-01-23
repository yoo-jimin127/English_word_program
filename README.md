# 영어 단어 암기 프로그램 구현

### main화면 : 프로그램 실행 시 가장 먼저 등장하는 기능 선택 화면
-------
 - main_func.c
    * 구현 방향 : <br>
      * 메뉴 화면 출력 <br>
        * user 입력값에 따라 switch문으로 case 1~5 <br>
          * 각 case : first_func.c ~ fourth_func.c 호출 <br>
            * first_func.c ~ fourth_func.c의 choose_setting1~4() 함수 호출 <br>
              * chhose_setting 함수 : 기능에서 사용할 파일명, 속도, 출력 방식 등에 대한 설정 <br>

### project1.h 헤더파일
--------
 - 헤더파일 내용 :
  ##### 전처리 작업
  
  ##### EngWord 구조체 (영단어, 뜻 저장 목적)
   * 영단어 저장 변수 word (1차원 char배열)
   * meaning (3 * 31 2차원 배열)
   * 뜻 카운트 변수
   * 파일에 저장되는 영단어 개수 카운트
   * 구조체 포인터 next *이게 여기 있는게 맞는지 모르겠음..
  
  ##### Node 구조체 (단어들 파일별로 정리 위해 연결하는 구조체)
   * Node 구조체 포인터 next, prev
   * 파일 이름 저장하는 1차원 char 배열 filename
   
  ##### LinkedList 구조체
   * *연결리스트를 어떻게 적용시켜야하는지 아직 감이 안잡히는 상태,,,
   
  ##### first_func.c ~ fourth_func.c 구현 함수 선언 
  

### file_manage.c 파일 관리 소스코드
--------
 ##### 노드 생성 함수 makeNode
  * 메모리 할당 해주고 next, prev 초기화시킨 상태
  ```
  Node *makeNode (char *fileName) {
      Node *newNode;
      
      newNode = (Node*)malloc(sizeof(Node));
      newNode -> next = NULL;
      newNode -> prev = NULL;
      
      return newNode;
      }
  ```
      텍스트 파일 읽어오면 될 것 같음 -> 
  
 
 ##### 노드에 단어 추가하는 함수 addNode
  * *엎어야할 것 같은 느낌... 연결리스트 구조체부터 만들어놓고 해야할 것 같은데 이상함..
  
  
### fuction 1. 영어 단어 맞추기
--------
 ##### choose_setting1() 함수
  파일명, 출력방식 입력 기능 담당
 ##### word_quiz(int day_file, int output_way) 함수
  choose_setting 에서의 입력값 바탕으로 영단어 맞추기 퀴즈 출제 기능
  
   - 인자로 전달받은 day_file.dic 파일 열어서 노드에 저장하고 리스트로 

### function 2. 플래쉬 카드
----------

### function 3. 행맨 (Hangman)
----------

### function 4. 단어장 관리
-----------

### function 5. 프로그램 종료
-----------
 구현 완료 (system("clear"); return 0;
