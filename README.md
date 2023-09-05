# C|EH Training
[Module 14: Hacking Web Application](CEHv12/Module14-Hacking-Web-Application.md)

[Module 15: SQL Injection](CEHv12/Module15-SQL-Injection.md)

[create an anchor](#anchors-in-markdown)

https://whatcms.org/ - get the CMS or Framework of website. Found and returns social networks also. #detect 

Steghide
□ Платформа: любая
Рис. 4.3. После и до
□ Где скачивать: GitHub(https://github.com/StefanoDeVuono/steghide)
Steghide - консольная утилита, написанная на С++. Скрывает информацию в стан­ дартных файлах форматов JPEG, ВМР, WAV и AU. В арсенале программы полно шифров - даже Blowfish, которого я у других не замечал. Теоретически использо­ вание такой экзотики может помочь запутать следы еще сильнее.
Steghide умеет не просто упаковывать данные в картинку или трек, а еще и шифро­ вать секретную нагрузку.
Но есть и минус: не все фотографии и аудиофайлы подойдут для внедрения в них секретной нагрузки. Если файл слишком маленький - внедрить в него ничего нельзя.
Давай попробуем объединить картинку cats. jpg и секретный файлик save. txt. Открываем терминал и пишем:
steghide emЬed -cf cats.jpg -ef save.txt
□ emЬedfile [-efJ - файл, который мы будем встраивать;
□ coverfile [ -cf] - файл-обложка, в который внедряется секретная инфа;
г-ак1 1
Отмена
f rПр-....тъJ

□-- 60 --□
□ compress [-z J - сжимать данные перед упаковкой; □ encryption [-eJ - шифровать внедряемые данные. Распаковка так же проста, как упаковка:
steghide extract -sf cats.jpg
