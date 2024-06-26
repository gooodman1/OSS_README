리눅스 명령어 중 top, ps, jobs, kill 명령어 조사          //  20243098 박진석
==================================================


top 명령어
-------------

# 기본 사용법
  - top: 시스템 요약 정보(시스템 시간, 업타임, 사용자 수, 평균 시스템 부하 와 프로세스 요약 정보(프로세스 상태 요, CPU 사용량, 메모리 사용량, 스왑 사용량) 그리고 프로세스 목록과 같은 정보를 실시간으로 표시한다.
 
## top 명령어 중 유용한 옵션

  - top -h: 도움말을 표시한다.
  - top -q: top 명령어를 종료한다.
  - top -k: 특정 PID를 입력받아 해당 프로세스를 종료한다.
  - top -r: 특정 PID를 입력받아 해당 프로세스의 우선순위를 변경한다.
  - top -f 또는 top -o: 필드 관리 화면을 띄워서 표시할 필드를 선택하거나 순서를 변경한다.
  - top -s: 갱신 주기를 설정한다 (기본 값:3초).
  - top -P: CPU 사용량 기준으로 정렬합다 (기본값).
  - top -M: 메모리 사용량 기준으로 정렬한다.
  - top -N: PID 기준으로 정렬한다.
  - top -T: 실행 시간 기준으로 정렬한다.

### top 명령어를 쓰는 이유
  - 시스템 모니터링에 있어 필수적이고, 시스의 현재 상태를 실시간으로 파악하고 관리할 수 있도록 하기 위해서 top 명령어를 사용한다.


ps 명령어
------------

# 기본 사용법
  - ps: 기본적으로 현재 터미널에서 실행 중인 프로세스 목록을 보여다.

## 명령어 중 유용한 옵션
  - ps -e 또는 ps -a: 시스템에서 실행 중인 모든 프로세스를 보여준다.
  - ps -u (username): 지정된 사용자가 실행 중인 모든 프로세스를 표시한다.
  - ps -f: 전체 형식으로 출력합니다. 프로세스의 자세한 정보를 보여준다.
  - ps -e --forest 또는 ps --forest: 프로세스들이 트리 구조로 어떻게 연결되어 있는지 보여준다.
  - ps -p: 특정 PID를 가진 프로세스의 정보를 표시한다.
  - ps -t: 특정 TTY와 연결된 프로세스를 표시한다.
  - ps aux 또는 ps -ef: 시스템의 모든 프로세스에 대한 자세한 정보를 표시한다.
    - a: 다른 사용자의 프로세스도 포함하여 보여줌
    - u: 사용자 친화적인 포맷으로 보여줌
    - x: 터미널에 연결되지 않은 프로세스도 포함


jobs 명령어
---------------

# 기본 사용법
  - jobs: 현재 쉘 세션의 모든 작업을 표시한다.

## 명령어 중 유용한 옵션
  - jobs -l: 각 작업의 프로세스 ID(PID)를 함께 표시한다.
  - jobs -n: 최근 상태가 변경된 작업만 표시한다. (*상태가 변경된 작업이 있는 경우에만 표시된다.)
  - jobs -p: 각 작업의 프로세스 ID만 표시한다.
  - jobs -r: 실행 중인 작업만 표시한다.
  - jobs -s: 정지된(중지된) 작업만 표시한다.


kill 명령어
-----------------

# 기본 사용법
  - kill: 기본 종료 신호를 보낸다.

## 명령어 중 유용한 옵션
  - kill -9 또는 kill -KILL: 프로세를 즉시 종료하는 강제 신호를 보낸다.
  - kill -l: 사용 가능한 모든 신호를 리스트로 표시한다.
  - kill -s 또는 kill --signal: 지정된 신호를 프로세스에 보낸다.
  - kill -p 또는 kill --process-group: 특정 프로세스 그룹에 신호를 보낸다.

### 주요 신호 목록
  - kill -1: 프로세스를 종료하고 재시작한다.
  - kill -2: 인터럽트 신호, 일반적으로 Ctrl+C로 보낸다.
  - kill -9: 강제 종료 신호.
  - kill -15: 기본 종료 신호.
  - kill -18: 정지된 프로세스를 계속 실행합니다.
  - kill -19: 프로세스를 정지시킨다. 재시작할 수 없다.
  - kill -20: 터미널 정지 신호, 일반적으로 Ctrl+Z로 보낸다.
