# Time Track Kata

## The Problem

You were asked to track your starting and finishing everyday. 
For that you decided to create a CLI application that will help you with that. 

The command line has two commands to record the data. `Start`, and `Stop` and they will be used like this:

```shell
$ app start
Your day 10/10/2019 is staring at 10:10:50
```

You can also override the starting time by passing the option `--time`.

```shell
$ app start --time "07/10/2019 09:00:00"
Your day 07/10/2019 is staring at 09:00:00
```

For the `Stop` you will have the same interface

```shell
$ app stop
Your day 10/10/2019 is stopping at 19:10:50

$ app start --time "07/10/2019 18:00:00"
Your day 07/10/2019 is stopping at 18:00:00
```

Of course you need to retrieve the data that you stored, So you are going to need the `List` command. 

When you use `List` the dates recorded has to show in chronological order from the oldest to the newest and the start and stop times has to be shown in the same line. 

```shell
$ app list
Date       Start    Stop
07/10/2019 09:00:00 18:00:00
10/10/2019 10:10:50 19:10:50
```

## The Implementation

Alright, I'm not the boss of you, and you don't have to do what I say **BUT** you might want to follow some rules when doing this kata. 

### Only Acceptance tests

Forget about unit tests, when doing Outside-In TDD you start with an acceptance test to guide your implementation, and in this case you it's the only thing that will guide you through the implementation. 

### Text File Database

It's a CLI application, you can't have an in-memory database because no one wants to keep the application running, so you have to store everything inside a text file. The format doesn't matter, it can be YAML, JSON, XML, or any other crazy format that you can think of. You will have to take that in account when writing your tests. But your tests can't access the file system, keep that in mind. 


