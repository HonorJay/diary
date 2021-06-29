# diary

파이토치 설치에 앞서 쿠다 버전 확인

아나콘다 프롬프트를 실행하고 기존에 사용하던 가상환경에 접속한 뒤 아래 명령어를 이용하여 설치된 cuda 버전을 확인

```python

nvcc --version

```

제가 사용하는 쿠다 버전은 11.0이었습니다. 

아래 주소로 들어가서 거기에 맞는 파이토치 버전을 찾아 설치해줍니다.

https://pytorch.org/get-started/previous-versions/

저는 윈도우에 쿠다11.0을 사용중이기에 

pip install torch==1.8.0+cu111 torchvision==0.9.0+cu111 torchaudio==0.8.0 -f https://download.pytorch.org/whl/torch_stable.html

요 명령어를 통해 설치해주었습니다.

용량이 3기가 정도 필요하니 남은 용량을 잘 확인하고 설치해주도록 합시다.

패키지 설치는 완료됐는데 그와는 별개로 에러메세지가 나왔습니다.

아무래도 url를 읽어오는 yarl 버전이 제가 가지고 있는 버전이 필요한 버전보다 더 최신 버전이라 호환이 안된다는 내용 같습니다 ㅠ 

ERROR: pip's dependency resolver does not currently take into account all the packages that are installed. 
this behaviour is the source of the following dependency conflicts.
aiohttp 3.6.3 requires yarl<1.6.0,>=1.0, but you have yarl 1.6.2 which is incompatible 
