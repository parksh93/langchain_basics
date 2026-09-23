# langchain 기초
## 실습환경
* python3.11 <br/>
* pyenv virtualenv<br/>
* ollama local<br/>
* llama3.2:1b

## 학습목표
1. Langchain과 RAG에 대한 이해
2. langchain을 활용하여 모델을 호출하고 프롬프트를 전송하여 결과 도출
3. chain을 통해 LLM간 결과 연결

## 기초 설정 (mas OS)
### 1. pyenv 설치
```
brew update
brew install pyenv

# 설치 확인
pyenv -v

# 환경변수 설정
export PYENV_ROOT="$HOME/.pyenv"
export PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init --path)"

#설정 적용
source ~/.zshrc

# 설치 확인
git clone https://github.com/pyenv/pyenv-doctor.git "$(pyenv root)/plugins/pyenv-doctor"
pyenv doctor

# python 설치
pyenv install <버전>

# 설치 확인
pyenv versions

# 기본 사용 python 버전 설정
pyenv global <버전> # 전역설정
pyenv local <버전> # 프로젝트 한정
pyenv shell <버전> # 현재 터미널 세션
```
### 2. pyenv-virtualenv 설치
```
git clone https://github.com/pyenv/pyenv-virtualenv.git "$(pyenv root)/plugins/pyenv-virtualenv"

# 환경변수 설정
echo 'eval "$(pyenv virtualenv-init -)"' >> ~/.zshrc
source ~/.zshrc

# 가상환경 생성
pyenv virtualenv <python 버전> <가상환경명>
```