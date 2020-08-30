## 환경
Windows 10 + WSL2 (Ubuntu 18.04) + Docker Desktop 으로 WSL 에 docker 주입

## 참고
[공식 문서](https://minikube.sigs.k8s.io/docs/start/) + Kubernetes In Action

## 순서

### 1) 다운로드
```bash
:~$ curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
```

### 2) 설치, 아무 로그 없이 완료
```bash
:~$ sudo install minikube-linux-amd64 /usr/local/bin/minikube
```

### 3) 시작, 1분 이상 소요
```bash
:~$ minikube start
😄  minikube v1.12.3 on Ubuntu 18.04
✨  Automatically selected the docker driver

❗  'docker' driver reported a issue that could affect the performance.
💡  Suggestion: enable overlayfs kernel module on your Linux

👍  Starting control plane node minikube in cluster minikube
🚜  Pulling base image ...
💾  Downloading Kubernetes v1.18.3 preload ...
    > preloaded-images-k8s-v5-v1.18.3-docker-overlay2-amd64.tar.lz4: 510.91 MiB
🔥  Creating docker container (CPUs=2, Memory=3100MB) ...
🐳  Preparing Kubernetes v1.18.3 on Docker 19.03.8 ...
🔎  Verifying Kubernetes components...
🌟  Enabled addons: default-storageclass, storage-provisioner
🏄  Done! kubectl is now configured to use "minikube"

❗  /usr/local/bin/kubectl is version 1.16.6-beta.0, which may be incompatible with Kubernetes 1.18.3.
💡  You can also use 'minikube kubectl -- get pods' to invoke a matching version
```

### 기타) 대시보드 활성화
명령어 실행 시에만 떠있고, 종료 시 내려감
http://127.0.0.1:37775/api/v1

```bash
:~$ minikube dashboard
🔌  Enabling dashboard ...
🤔  Verifying dashboard health ...
🚀  Launching proxy ...
🤔  Verifying proxy health ...
🎉  Opening http://127.0.0.1:37775/api/v1/namespaces/kubernetes-dashboard/services/http:kubernetes-dashboard:/proxy/ in your default browser...
👉  http://127.0.0.1:37775/api/v1/namespaces/kubernetes-dashboard/services/http:kubernetes-dashboard:/proxy/
```