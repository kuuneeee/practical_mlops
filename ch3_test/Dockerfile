# instruction
# FROM ubuntu:22.04
# 컨테이너 기반의 이미지를 지정하는 FROM -> centos 버전 8 -> 버전 지정 안하면 일반적으로 latest 사용

# RUN : \\
#     && apt-get update \\
#     && apt-get install -y python38 \\

# 에러
# Error: Failed to download metadata for repo 'appstream': Cannot prepare internal mirrorlist: No URLs in mirrorlist
# -> 8 버전 지원 종료


FROM ubuntu:22.04
RUN : apt-get update
RUN : apt-get install -y python38
RUN : pip install pytest

ENTRYPOINT [ "/bin/bash" ]


# docker build [repository]:[tag]
# docker run -it -d --rm [repository]:[tag]
    # -it : TTY(터미널 에뮬레이터)에 할당 후, stdin 연결
    # -d : 백그라운드 동작
    # --rm : 종료 시 컨테이너 제거
    # --name : 컨테이너 이름 지정
# docker exec -it [container id] bash
    # exec 실행중인 컨테이너에 접속
    # 일회성으로 접속할 수도 있음 : docker exec [contatiner id] tail /var/log/dnf.log

