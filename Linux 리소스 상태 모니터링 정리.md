#### uname
→ 시스템과 커널의 정보를 확인하는 명령
- 주요 옵션
    ```
    [-a, --all]: 전체 내용 출력
    [-s, --kernel-name]: 커널 명 출력
    [-n, --nodename]: 네트워크 노드의 호스트 명 출력
    [-r, --kernel-release]: 커널 릴리즈 정보 출력
    [-v, -kernel-version]: 커널 버전 출력
    [-m, --machine]: 머신 하드웨어 이름 출력
    [-p, --processor]: 프로세서 종류 또는 'unknown' 출력
    [-i,- -hardware-platform ]: 하드웨어 플랫폼 또는 'unknown' 출력
    [-o, --operating-system ]: 운영체제 'unknown' 출력
    ```

#### top
→ 시스템 프로세스들의 CPU/Memory 점유율을 실시간으로 볼 수 있는 명령
- %Cpu(s) 설명
    ```
    [us]: 사용자가 사용중인 사용률
    [sy]: 시스템이 사용중인 사용률
    [ni]: 프로세스 우선순위를 기반으로 사용되는 사용률(사용자 공간에서 사용됨)
    [id]: 아무 일도 하지 않는 여유률
    [wa]: 입출력을 기다리는 프로세스 사용률
    [hi]: 하드웨어 인터럽트 사용률
    [si]: 소프트웨어 인터럽트 사용률
    [st]: 가상화 환경에서 손실률
    ```

- PROCESS 설명
    ```
    [PID]: 프로세스 ID
    [USER]: 프로세스를 실행시킨 사용자 ID
    [PR]: 프로세스의 우선순위
    [NI]: NICE 값, 마이너스를 가지는 값이 우선순위가 높음
    [VIRT]: 가상 메모리의 사용량(SWAP+RES)
    [RES]: 현재 페이지가 상주하고 있는 크기
    [SHR]: 가상 메모리 중 사용중인 메모리를 제외한 잔여 가상 메모리
    [S]: 프로세스의 상태
    [%CPU]: 프로세스가 사용하는 CPU의 사용률
    [%MEM]: 프로세스가 사용하는 메모리의 사용률
    [TIME+]: 프로세스가 CPU를 사용한 시간
    [COMMAND]: 실행된 명령어
    ```

- PROCESS 정렬 기준
    ```
    [SHIFT + M]: 메모리 사용률 정렬
    [SHIFT + N]: PID 기준 정렬
    [SHIFT + P]: CPU 사용률 정렬
    [SHIFT + T]: 실행시간 기준 정렬
    [SHIFT + R]: 정렬 기준변경 (오름차순인 경우 내림차순, 내림차순인 경우 오름차순으로 변경)
    ```

#### free
→ 메모리에 대한 정보를 확인할 수 있는 명령
    ```
    [free -b # or –bytes]: show output in bytes
    [free -k # or –kilo]: show output in kilobytes
    [free -m # or –mega]: show output in megabytes
    [free -g # or –giga]: show output in gigabytes
    ```

#### vmstat
→ 시스템 정보 모니터링
    ```
    [verstat 3 5]: 3초 간격으로 모니터링 정보를 5번 출력
    ```

#### netstat
→ 네트워크 상태, 라우팅 테이블, 인터페이스 상태 등을 볼 수 있는 명령
    ```
    [netstat -r]: 서버의 라우팅 테이블 출력
    [netstat -na --ip]: tcp/udp의 세션 목록 표시
    [netstat -na | grep ESTABLISHED | wc -l]: 활성화된 세션 수 확인
    [netstat -nap | grep:80 | grep ESTABLISHED | wc -l]: 80포트 동시 접속자수
    [netstat -nltp]: LISTEN 중인 포트 정보 표시
    ```

#### df
→ 현재 디스크의 전체 용량 및 남은 용량을 확인할 수 있는 명령
    ```
    [-h]: 용량을 읽기 쉽게 단위를 계산하여 출력
    [-T]: 파일 시스템 종류와 함께 디스크 정보 출력
    ```