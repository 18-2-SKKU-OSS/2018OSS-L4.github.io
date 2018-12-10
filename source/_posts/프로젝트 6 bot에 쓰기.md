---
title: custom command 팀 프로젝트 6 bot.py에 쓰기
date: 2018-12-10 15:00:09
tags:
categories: ["PROJECT"]
---

# bot.py에 쓰기

---


bot.py를 수정하고 마크하여 

최종적으로 커스텀 명령어가 작동되게끔 한다.

#modify and mark bot.py
f_botpy = open('bot.py','r+',encoding='UTF8')
strings = f_botpy.read()
commands = readcommand('../config/custom_command.txt')
for key, value in commands.items():
    strings = strings.replace(key,value)
clearwrite(f_botpy,'#custom command\n' + strings)
f_botpy.close()


주소 : https://github.com/18-2-SKKU-OSS/2018-2-OSS-L4/blob/master/musicbot/custom.py
