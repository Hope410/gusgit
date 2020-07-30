# Gusgit: cli для связывания задач Trello с коммитами git

## Установка

    sudo npm i -g gusgit

## Использование

    gusgit branch <branch>        

Создает git-ветку с названием "T<number>". <branch> - это либо ссылка на Trello, либо название ветки в формате "T<number>".


    gusgit rebase [<from>]        
    
Компанует набор коммитов из текущей ветки в один. <from> - это название ветки, относительно которой должна произойти компановка. По умолчанию <from> = master.

    gusgit land [<to>]            
    
Мержит текущую ветку с веткой <to>, удаляет ее и добавляет ссылку на коммит в карточку Trello, к которой была прикреплена ветка. По умолчанию <to> = master.