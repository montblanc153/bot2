# 토트넘 홋스퍼 팬클럽 웹사이트

## 뉴스레터 봇 설정 방법

### 1. 텔레그램 봇 생성
1. 텔레그램에서 [@BotFather](https://t.me/botfather)를 검색
2. `/newbot` 명령어로 새 봇 생성
3. 봇 이름과 사용자명 설정
4. BotFather가 제공하는 API 토큰을 저장

### 2. News API 키 발급
1. [News API](https://newsapi.org/) 웹사이트 방문
2. 회원가입 후 API 키 발급

### 3. GitHub Secrets 설정
GitHub 저장소의 Settings > Secrets and variables > Actions에서 다음 시크릿을 추가:
- `TELEGRAM_BOT_TOKEN`: 텔레그램 봇 토큰
- `TELEGRAM_CHAT_ID`: 뉴스레터를 받을 채팅방 ID
- `NEWS_API_KEY`: News API 키

### 4. 워크플로우 실행
- 자동 실행: 매일 UTC 12시(한국시간 21시)에 자동으로 실행
- 수동 실행: GitHub Actions 탭에서 "Tottenham Hotspur Newsletter" 워크플로우를 선택하여 수동 실행 가능

## 기능
- 매일 토트넘 홋스퍼 관련 최신 뉴스 수집
- 최대 5개의 주요 뉴스를 텔레그램으로 전송
- 뉴스 제목과 링크 제공
- HTML 포맷팅 지원

## 기술 스택
- Python 3.10
- GitHub Actions
- News API
- python-telegram-bot

# 경제 뉴스레터 봇

매일 아침 7시에 주요 경제 뉴스를 수집하여 요약본을 텔레그램으로 전송하는 봇입니다.

## 주요 기능
- 주요 경제 뉴스 자동 수집
- 뉴스 기사 자동 요약
- 매일 아침 7시 자동 발송
- HTML 포맷팅 지원
- 다중 뉴스 소스 지원

## 설정 방법

### 1. 텔레그램 봇 생성
1. 텔레그램에서 [@BotFather](https://t.me/botfather)를 검색
2. `/newbot` 명령어로 새 봇 생성
3. 봇 이름과 사용자명 설정
4. BotFather가 제공하는 API 토큰을 저장

### 2. News API 키 발급
1. [News API](https://newsapi.org/) 웹사이트 방문
2. 회원가입 후 API 키 발급

### 3. GitHub Secrets 설정
GitHub 저장소의 Settings > Secrets and variables > Actions에서 다음 시크릿을 추가:
- `TELEGRAM_BOT_TOKEN`: 텔레그램 봇 토큰
- `TELEGRAM_CHAT_ID`: 뉴스레터를 받을 채팅방 ID
- `NEWS_API_KEY`: News API 키

### 4. 워크플로우 실행
- 자동 실행: 매일 아침 7시(한국시간)에 자동으로 실행
- 수동 실행: GitHub Actions 탭에서 "Economy News Summary" 워크플로우를 선택하여 수동 실행 가능

## 수집하는 뉴스 주제
- 한국 경제
- 주식 시장
- 금리
- 환율
- 부동산
- 인플레이션
- 고용
- 수출입
- GDP
- 금융

## 뉴스 소스
- 조선일보
- 중앙일보
- 동아일보
- 한국일보
- 매일경제
- 한국경제
- 아시아경제
- 서울경제

## 기술 스택
- Python 3.10
- GitHub Actions
- News API
- python-telegram-bot
- newspaper3k (뉴스 요약) 