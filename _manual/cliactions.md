---
title: Command Line Actions
id: cliactions
layout: manual
description:  Tilix supports the use of command line actions to have the running instance execute an action that you would typically do through the user interface, for example splitting a terminal.
---
#### Introduction

Tilix supports the use of command line actions to have the running instance execute an action that you would typically do through the user interface. The use case for this functionality is to be able to run a script within Tilix that causes it to perform certain commands. For example, to have Tilix run the command ```less /etc/issue``` in a new terminal that is split right, the following command can be used:


{% highlight bash %}
tilix -a session-add-right -x "less /etc/issue"
{% endhighlight %}

The ```-a```, or ```--action```, command line switch is what is used to specify the action to be executed. Any action executed is always done relative to the terminal where the command was executed. Any command line parameters that are specified as part of the command get passed to the new terminal. This allows you to do a variety of things such as use a different profile, specify the working directory or as per the example above, execute a command.

#### Supported Actions

The actions are specified using the same keys you see in dconf for the key shortcuts at ```/com/gexperts/Tilix/keybindings```. While any action shown here can be sent via the action parameter, not all of them are supported or will work. Some actions, such as Synchronize Input, would require additional parameters to function correctly.

The table below is the list of officially supported actions at this time:

| Action            | Description                 |
|-------------------|:----------------------------|
| session-add-right | Splits the terminal right   |
| session-add-down  | Splits the terminal down    |
| app-new-window    | Creates a new Tilix window  |
| app-new-session   | Creates a new Tilix session |
