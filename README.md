# Poll

## General structure

polls/ · · · · · · · · · · · · · · · · ·· Polls
· └── [id of the poll]/ · · · · · · · · · One poll
· · · ├── info · · · · · · · · · · · · ·· General infos
· · · ├── status · · · · · · · · · · · ·· Current poll status
· · · ├── grades/ · · · · · · · · · · · · Grades used in this polls
· · · │ · ├── [id of grade 1] · · · · · · First grade
· · · │ · └── [id of grade 2] · · · · · · Second grade
· · · ├── options/ · · · · · · · · · · ·· Options offered to voters
· · · │ · ├── [id of option 1] · · · · ·· First option
· · · │ · └── [id of option 2] · · · · ·· Second option
· · · ├── votes/ · · · · · · · · · · · ·· Votes
· · · │ · ├── [id of voter 1] · · · · · · Votes of voter 1
· · · │ · └── [id of voter 2] · · · · · · Votes of voter 2
· · · └── results/ · · · · · · · · · · ·· Results
· · · · · ├── winner · · · · · · · · · ·· Elected option
· · · · · ├── [id of option 1] · · · · ·· Results for first option
· · · · · | · ├── results · · · · · · · · Grade and score obtained by first option
· · · · · | · └── by-grade · · · · · · ·· Results by grade for first option
· · · · · └── [id of option 2] · · · · ·· Results for second option
· · · · · · · ├── results · · · · · · · · Grade and score obtained by second option
· · · · · · · └── by-grade · · · · · · ·· Results by grade for second option

## Example of polls/[id of the poll]/info

```
{
    "title": "My poll"
}
```

## Example of polls/[id of the poll]/status

```
{
    "id": "draft",
    "label": "Draft",
}
```

Status id are:

- draft: poll is not published yet
- open: poll is published and participants can vote
- close: votes are closed and results are availables

## Example of polls/[id of the poll]/grades/[id of grade 1]

```
{
    "id": "yes",
    "label": "Yes",
    "position": 1
}
```

Grade position order goes from absolute Yes to absolute No
For example : yes, meh, no

## Example of polls/[id of the poll]/options/[id of option 1]

```
{
    "id": "blue",
    "label": "Blue",
    "position": 1
}
```

## Example of polls/[id of the poll]/votes/[id of voter 1]

```
{
    "blue": "yes",
    "red": "no"
}
```

## Example of polls/[id of the poll]/results/winner

```
{
    "optionId": "blue"
}
```

## Example of polls/[id of the poll]/results/[id of option 1]/result

```
{
    "gradeId": "yes",
    "score": 2
}
```

## Example of polls/[id of the poll]/results/[id of option 1]/by-grade

```
{
    "yes": 2,
    "no": 1
}
```
