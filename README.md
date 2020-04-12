# todotxt-cli-template

This should be a small script for using **templates** for [todo-cli](https://github.com/todotxt/todo.txt-cli).


## how to install

- Go to your $TODO_ACTIONS_DIR

```
wget https://raw.githubusercontent.com/MAWSpitau/todotxt-cli-template/master/tmplt
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
    - you can give a startdate realtive to today by giving a task a **+d** or a **-d** at the last option of your template task.
  - **-duer**: due relative
    - The tasks date default is the date your give after **-due** in this format: yyyy-mm-dd.
    -

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
