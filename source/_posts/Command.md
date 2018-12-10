---
title: 뮤직봇 커맨드
date: 2018-12-04 19:00:09
tags:
categories: ["WIKI"]
---

# Commands

---

이 문서는 MusicBot에 사용되는 명령어를 설명해놓았습니다. Private message로 MusicBot에게 명령어를 보내면 정상적으로 작동하지 않습니다. 모든 명령어는 사용자가 설정한 문자로 시작합니다. 이 페이지는 해당 문자가 기본 설정인 !라고 가정하고 설명하고 있습니다. 반드시 필요한 파라미터는 <> 로 감싸여 있고 선택적인 파라미터는 []로 감싸여져 있습니다.

### 기본
---

!help [command] - 명령어의 목록이나 특정 명령어의 정보를 출력합니다.
!play <URL/query> - 특정한 URL에서 음악을 재생하거나 YouTube에서 검색어를 검색하고 첫 번째 결과를 대기열에 넣습니다.
!queue - 재생 목록을 표시합니다.
!np - 현재 재생중인 음악을 표시합니다.
!skip - 현재 재생중인 음악을 스킵할 지 투표합니다. 필요한 찬성 비율은 config 파일에서 설정할 수 있습니다. 봇의 주인은 !skip f로 즉시 스킵할 수 있습니다.
!search [service] [#] <query> - <query>에 대해 특정 서비스 (기본값 : YT)를 검색하고 처음 몇 개의 결과를 반환합니다.(기본값은 3개이고 최대 10개의 결과까지 반환합니다) 그 후 유저는 결과값의 일부를 큐에 추가할 수 있습니다.
!shuffle - 재생 목록을 섞습니다.
!clear - 재생 목록을 초기화합니다.
!pause - 현재 음악을 일시정지합니다.
!resume - 현재 음악을 다시 재생합니다.
!volume [number] - 봇의 볼륨을 세팅합니다. number는 1부터 100까지 선택할 수 있습니다. 상대적인 숫자(예를 들어, +10) 도 입력 가능하며 현재 볼륨에 해당 숫자를 더하거나 뺀 수치로 변경됩니다. 파라미터가 없으면 현재 볼륨을 표시합니다.
!summon - 봇을 현재 보이스 채널에 연결시킵니다. 이 명령어를 실행하려면 권한이 있어야 합니다.
!clean <number> - Searches through the number of messages given and deletes those that were sent by the bot, effectively cleaning the channel. If the bot has Manage Messages on the server, it will delete user command messages too, like !play.
!blacklist <status> <@user1>... - Add or remove users from the blacklist. Blacklisted users cannot use any bot commands. This overrides any permissions settings set in the permissions file. The owner cannot be blacklisted. Multiple users can be specified in the command. Users must be @mentioned. Status should be either +, -, add, or remove.
!perms - 유저에게 봇의 권한을 포함한 메세지를 보냅니다.
!stream <url> - URL을 스트리밍합니다. URL은 트위치나 유튜브 등의 라이브 스트리밍 사이트가 될 수 있습니다. 이 명령어는 실험중임으로 약간의 문제가 있을 수 있습니다.
!save - 현재 음악을 오토 플레이 리스트에 저장합니다.
!karaoke - 서버에서 karaoke 모드를 킵니다. karaoke 모드 중에는 BypassKaraokeMode 권한을 가진 유저만이 음악을 플레이 할 수 있습니다.

### 관리
---

!joinserver - Provides the URL that can be used to add the bot to another server. This command is always restricted to the owner of the bot.
!pldump <playlist> - Collects URLs from a YouTube playlist or Soundcloud set and dumps them into a text file that can be copied into the autoplaylist.
!setavatar [url] - Changes the bot’s avatar to the specified URL or uploaded image. A URL does not need to be specified if an image is uploaded with the command as the message (comment).
!setname <name> - 봇의 디스코드 이름을 바꿉니다.(닉네임을 바꾸지는 않습니다).디스코드는 이 변경을 2시간에 한번으로 제한해 놨습니다.
!setnick <nick> - 서버에서의 봇의 닉네임을 바꿉니다. 이 명령어를 실행하기 위해 권한이 필요합니다.
!disconnect - 보이스 채널로부터 봇을 추방시킵니다.
!restart - 봇을 재시작합니다.
!shutdown - 봇을 종료합니다.
!option <option> <y/n> - 봇을 종료하지 않고 설정 옵션을 변경합니다. 자세한 정보는 !help를 입력해서 볼 수 있습니다.
!remove <number> - number위치에 있는 음악을 재생목록에서 제거합니다. 음악의 위치는 !queue를 입력하여 볼 수 있습니다.

### 개발자
---

These commands are intended for people who know how Python works and/or developers of the bot. As such, they are restricted behind additional permissions that must be granted in the options file. Please do not run any of these commands unless you are absolutely sure that you are aware what you are doing and the potential consequences, as they can be very dangerous.

!breakpoint - 디버깅 breakpoint를 활성화합니다.
!objgraph [func] - 오브젝트 그래프를 리턴합니다.
!debug - 임의의 코드를 평가합니다. 이 명령어는 굉장히 위험한 명령어이니 사용에 주의하십시오.
