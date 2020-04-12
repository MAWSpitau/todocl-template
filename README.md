# todotxt-cli-template

This should be a small script for using **templates** for [todo-cli](https://github.com/todotxt/todo.txt-cli).


## how to install

- Go to your $TODO_ACTIONS_DIR

```
wget https://raw.githubusercontent.com/MAWSpitau/todotxt-cli-template/master/tmplt
chmod u+x tmplt
```
The action is installed.

## how to use

```
$ todo.sh tmplt <yourtemplate> [-duet|-duer YYYY-mm-dd] [optional parameter]
```

- First thing is to call the action. You do this with:

```
$todo.sh tmplt
```

- BUT you have to to tell the script, which action it schould put in your todo.txt
- This template has to be in your $TODO_DIR/tmplt dir.
  - The script will make this dir, if you haven't done it. ;)

### <yourtemplate>

- This is a file in the path where your  is.
- This file is basicly build with the todo.txt-syntax.
- You can choose when the tasks due-date is in two ways.
  - **-duet**: due today
    - The tasks date default is **today**.
    - You can give a startdate realtive to today by giving a task a **+d** or a **-d** at the last option of your template task.
  - **-duer**: due relative
    - The tasks date default is the date your give after **-due** in this format: yyyy-mm-dd.
    - You can give a startdate realtive to the startdate by giving a task a **+d** or a **-d** at the last option of your template task.

#### Example
```
  (A) Do that! +myproject @computer +5
   |  |         |          |         |--- This should be done in 5 days from
   |  |         |          |              (-duer) a relative date or (-duet)
   |  |         |          |              from today.
   |  |         |          |--- this is a context
   |  |         |--- this is a project
   |  |--- the task
   |--- the priority
```

## Example template

### this is my testing tempalate

```
(Z) minus 1 +loeschmich -1
(Z) minus 2 +loeschmich -2
(Z) minus 3 +loeschmich -3
(Z) nix +loeschmich
(Z) null 1 +loeschmich +0
(Z) plus 1 +loeschmich +1
(Z) plus 2 +loeschmich +2
(Z) plus 3 +loeschmich +3
```

### Different Calls

    todo.sh tmplt 001

```
(Z) 2020-04-12 minus 1 +loeschmich
(Z) 2020-04-12 minus 2 +loeschmich
(Z) 2020-04-12 minus 3 +loeschmich
(Z) 2020-04-12 nix +loeschmich
(Z) 2020-04-12 null 1 +loeschmich
(Z) 2020-04-12 plus 1 +loeschmich
(Z) 2020-04-12 plus 2 +loeschmich
(Z) 2020-04-12 plus 3 +loeschmich
```

    todo.sh tmplt 001 -duet

```
(Z) 2020-04-12 minus 1 +loeschmich due:2020-04-11
(Z) 2020-04-12 minus 2 +loeschmich due:2020-04-10
(Z) 2020-04-12 minus 3 +loeschmich due:2020-04-09
(Z) 2020-04-12 nix +loeschmich due:2020-04-12
(Z) 2020-04-12 null 1 +loeschmich due:2020-04-12
(Z) 2020-04-12 plus 1 +loeschmich due:2020-04-13
(Z) 2020-04-12 plus 2 +loeschmich due:2020-04-14
(Z) 2020-04-12 plus 3 +loeschmich due:2020-04-15

```

    todo.sh tmplt 001 -duer 2023-02-01

```
(Z) 2020-04-12 minus 1 +loeschmich due:2023-01-31
(Z) 2020-04-12 minus 2 +loeschmich due:2023-01-30
(Z) 2020-04-12 minus 3 +loeschmich due:2023-01-29
(Z) 2020-04-12 nix +loeschmich due:2023-02-01
(Z) 2020-04-12 null 1 +loeschmich due:2023-02-01
(Z) 2020-04-12 plus 1 +loeschmich due:2023-02-02
(Z) 2020-04-12 plus 2 +loeschmich due:2023-02-03
(Z) 2020-04-12 plus 3 +loeschmich due:2023-02-04
```

    todo.sh tmplt 001 -duet +testproject @testcontext

```
(Z) 2020-04-12 minus 1 +loeschmich +testproject @testcontext due:2020-04-11
(Z) 2020-04-12 minus 2 +loeschmich +testproject @testcontext due:2020-04-10
(Z) 2020-04-12 minus 3 +loeschmich +testproject @testcontext due:2020-04-09
(Z) 2020-04-12 nix +loeschmich +testproject @testcontext due:2020-04-12
(Z) 2020-04-12 null 1 +loeschmich +testproject @testcontext due:2020-04-12
(Z) 2020-04-12 plus 1 +loeschmich +testproject @testcontext due:2020-04-13
(Z) 2020-04-12 plus 2 +loeschmich +testproject @testcontext due:2020-04-14
(Z) 2020-04-12 plus 3 +loeschmich +testproject @testcontext due:2020-04-15
```
