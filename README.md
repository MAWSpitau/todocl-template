# todotxt-cli-template

This should be a small script for using **templates** for todo-cli



## how to install


## how to use

> $ todo.sh tmplt <yourtemplate> [-duet|-duer] [YYYY-mm-dd] [optional parameter]

### <yourtemplate>

- This is a file in the path where your todo.txt is.
- This file is build with the todo.txt-syntax
- You can choose when the tasks due-date is.

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
