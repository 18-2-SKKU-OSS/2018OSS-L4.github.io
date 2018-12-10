---
title: README.md
date: 2018-12-04 19:00:09
tags:
categories: ["WIKI"]
---

# MusicBot

---
### 이 브랜치는...

이 Musicbot의 브랜치는 rewrite 버전의 discord.py 라이브러리와만 호환 가능합니다. 해당 라이브러리는 python3 -m pip install -U git+ ht tps://github.com/Rapptz/discord.py@rewrite#egg=discord.py [voice]로 설치 가능합니다. 또한 requirements.txt의 목록을 dependency로 가지고 있습니다. 이것들은 bot을 설치할 때 update.py를 실행하면 자동으로 설치됩니다.

### GitHub release v1.9.8_2 Python 3.5, 3.6 Discord

MusicBot은 Python 3.5+로 짜여진 디스코드 음악 봇입니다. discord.py라이브러리를 사용합니다. 이 봇은 하나 이상의 디스코드 서버에 유튜브나 기타 플랫폼에서 요청받은 음악을 재생합니다. 만약 요청 큐가 비었다면 재생 리스트에서 음악을 재생하게 설정할 수 있습니다. 봇의 소유자는 봇이 특정 사람의 명령어만 받아들이게 제한할 수 있습니다. MusicBot은 음악 재생뿐만 아니라 라이브 미디어를 음성 채널로 스트리밍 할 수 있습니다. 이는 아직 미완성된 기능입니다.

![good](https://camo.githubusercontent.com/25363218509757cbb6e597e81cc24b6e505ee489/68747470733a2f2f692e696d6775722e636f6d2f455a6c6a5935322e706e67)

*******************************************************

# 설정
---
MusicBot을 설치하는 것은 굉장히 쉽습니다. 우리가 준비한 이 [가이드](https://just-some-bots.github.io/MusicBot/) we have created for you. After that, you can begin to configure your bot to ensure that it can connect to Discord.만 따라하면 됩니다. 가이드를 따라 한 뒤에, 디스코드에 봇을 연결하기 위한 설정을 시작하면 됩니다.

가장 중요한 설정 파일은 config/options.ini이지만 이 파일은 레포지토리에 포함되어 있지 않습니다. example_options.ini의 이름을 options.ini로 바꾸세요. example_options.ini 에 설정을 위한 더 많은 정보들이 적혀져 있습니다.

### 명령어들
봇을 위해 굉장히 많은 명령어들이 있습니다. 가장 중요한 명령어는 play <url> 입니다(preceded by your command prefix). 이 명령어는 유튜브나 다른 플랫폼에서 음악을 다운로드하고 플레이합니다. 모든 명령어를 보려면 [여기](https://just-some-bots.github.io/MusicBot/using/commands/).를 클릭하세요.

### 추가적인 문서
[Support Discord server](https://discordapp.com/invite/bots)
[Project license](https://github.com/18-2-SKKU-OSS/2018-2-OSS-L4/blob/master/LICENSE)
