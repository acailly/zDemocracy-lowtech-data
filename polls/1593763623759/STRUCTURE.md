# Poll

## title.txt (file)

The first line of this file contains the title of the poll

## status.xxx (file)

The filename of this file tells the status of the poll

The format is "status.<insert status here>", for example: "status.open"

Status values are:

- draft: poll is not published yet
- open: poll is published and participants can vote
- close: votes are closed and results are availables

## grades folder

This folder contains one file by grade

The filename format of the grade file is "<position>.<option id>", for example: "1.good"

Grade position order goes from absolute Yes to absolute No
For example : yes, meh, no

The first line of the option file contains the displayed name of the grade

## options folder

This folder contains one file by option

The filename format of the option file is "<position>.<option id>", for example: "1.good"

The first line of the option file contains the displayed name of the option

## votes folder

This folder contains one folder by vote, which name is the voter name

### voter folder

Each voter folder contains voter answers for all options

These answers are files wich filename format is "<option id>.<grade id>"

## results folder

This folder contains several files and folders

### winnner.xxx file

This file indicates the winner

The filename format of this file is "winner.<option id>"

### option result folder

There is one folder by option containing results for this option

#### score.xxx file

This file indicates the score of the option

The filename format of this file is "score.<score>"

#### grade.xxx file

This file indicates the computed grade of the option

The filename format of this file is "grade.<grade id>"

#### by-grade folder

This folder contains a file for each grade

The filename format of these files is "<grade id>.<vote count for this grade>"
