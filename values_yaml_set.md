  gitSync:
    # true값 설정
    enabled: true

    # git repo clone url
    # ssh example: git@github.com:apache/airflow.git
    # https example: https://github.com/apache/airflow.git
    # repo 주소 설정 https형식
    repo: https://github.com/dragonhail/airflow_gke.git
    # branch 설정
    branch: main
    rev: HEAD
    # The git revision (branch, tag, or hash) to check out, v4 only
    ref: v2-2-stable
    depth: 1
    # the number of consecutive failures allowed before aborting
    maxFailures: 0
    # subpath within the repo where dags are located
    # should be "" if dags are at repo root
    # 폴더 수정 필요
    subPath: "dags"
    # sshkeysecret gke 시크릿 설정
    sshKeySecret: airflow-gke-git-secret