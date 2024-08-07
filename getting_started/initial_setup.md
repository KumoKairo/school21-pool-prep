## Привет!
Интенсив может пугать своей сложностью и неизвестностью, особенно если нет никакого опыта в программировании в целом, и на языке С в частности. Чтобы помочь освоиться и получить уверенность в своих силах, я советую начать с книги [Head First C](https://www.oreilly.com/library/view/head-first-c/9781449335649/). 
Самостоятельным поиском в интернете можно найти версию для ознакомления, а также поискать версию на русском, в случае если уровень английского не позволяет эффективно пользоваться оригинальной версией.

Для начала стоит настроить среду разработки и компилятор. Если у вас Windows (что наиболее вероятно), то я советую начинать сразу с Unix команд, так на интенсиве будет проще продолжить. 
Если у вас MacOS, то всё намного проще (инструкцию можно найти в интернете по запросу `install gcc macos`).

В Windows есть удобный функционал WSL (Windows Subsystem for Linux), который позволяет использовать Linux команды на Windows. Более подробно можно прочитать здесь - [What is the Windows Subsystem for Linux?](https://learn.microsoft.com/en-us/windows/wsl/about)

Она выключена по умолчанию, поэтому нужно включить её в настройках Windows - Turn Windows features on or off

<img src="https://github.com/KumoKairo/school21-pool-prep/assets/2943071/b482f4b2-2bc9-4529-ac76-8914a64179bf" alt="drawing" width="450"/>

Открываем меню, листаем вниз, находим Windows Subsystem for Linux и Virtual Machine Platform, ставим галочки:

<img src="https://github.com/KumoKairo/school21-pool-prep/assets/2943071/f62051eb-091c-438b-ad68-3645dbc8f8da" alt="drawing" width="550"/>

Нажимаем ОК и ждём окончания процесса установки, после которого вас попросят перезагрузиться (и нужно перезагрузиться).

После этого можно установить сам дистрибутив Linux. Примеры ниже будут на [Ubuntu](https://apps.microsoft.com/detail/9pdxgncfsczv)

Установите и запустите новое приложение. Если появятся ошибки, то попытайтесь решить их самостоятельно (в частности, используя ссылку на Learn Microsoft, оставленную выше). Чаще всего ошибки возникают из-за неправильно включенных или выключенных компонентов системы и компьютера, в особенности связанные с виртуализацией.

Если всё в порядке, вас встретит окно начальной настройки:

![image](https://github.com/KumoKairo/school21-pool-prep/assets/2943071/b4f1b489-e218-4efe-bc41-3a81b6b2498d)

Здесь вам нужно ввести имя пользователя и пароль нового пользователя системы. Выберите имя на латинице, и придумайте пароль, который сможете вводить часто и без затруднений.

После чего вы окажетесь в основной консоли под только что созданным пользователем.

Обычно после первоначальной установки советуют обновить менеджер пакетов, выполнив поочерёдно команды 
`sudo apt-get update` и `sudo apt-get upgrade`. 

Для выполнения команд наберите их в консоли и нажмите Enter. Иногда вас будут просить ввести пароль. Иногда нужно подтвердить загрузку и установку (Обычно фразой `Do you want to continue? [Y/n]`), на которую нужно ответить, набрав `y` на клавиатуре и нажав `Enter` (y - yes, n - no).

Всё должно завершиться успешно. В случае возникновения ошибок в консоли обычно будут предложены варианты. Настоятельно советую обращать внимания на сообщения в консоли, они часто бывают полезными либо для непосредственного решения проблемы, либо для упрощения поиска решения в интернете.

Единственный оставшийся шаг - установка компилятора. В книге для компиляции используется команда `gcc`, поэтому установим его с помощью команды `sudo apt-get install gcc`

После установки можно проверить текущую версию с помощью команды `gcc --version`. 

![image](https://github.com/KumoKairo/school21-pool-prep/assets/2943071/0677d7ef-7582-4ea7-ad9f-506e309a159d)

Теперь можно создать файл с программой, скомпилировать и запустить. Файлы Linux Subsystem находятся по адресу `\\wsl$\Ubuntu` (нужно ввести в адресную строку в File Explorer). Оттуда перейдите в папку `home`, в которой будет папка вашего созданного пользователя. Создайте там папку `projects`.

<img src="https://github.com/KumoKairo/school21-pool-prep/assets/2943071/3fd7c1c8-46ee-4ee9-979a-ed64213424ab" alt="drawing" width="450"/>

Теперь если в консоли вызвать команду `ls`, то в списке файлов и папок будет только что созданная папка `projects`. Можно перейти в неё комадой `cd projects/`.

В папке `projects` создайте текстовый файл `rocks.c` и откройте его в блокноте или любом текстовом редакторе. В качестве стартовой программы в книге предлагается написать вариацию `Hello World!`, поэтому напишем программу:

```
#include <stdio.h>

int main()
{
  puts("C Rocks!");
  return 0;
}
```

Сейчас и на будущее - старайтесь писать текст программ из примеров вручную. Это позволит привыкнуть к синтаксису и набить руку.

Сохраните файл. Программа готова к компиляции и запуску.

Для компиляции используем команду `gcc rocks.c -o rocks`. На выходе получаем исполняемый файл под названием `rocks` (похож на исполняемый `.exe` файл в Windows).

Для запуска выполняем команду `./rocks`. На выходе получаем строчку `C Rocks!`.

![image](https://github.com/KumoKairo/school21-pool-prep/assets/2943071/5b1df94e-fc96-40a0-95ac-2c3af9400afb)

Готово, вы восхитительны! Удачи на интенсиве.
