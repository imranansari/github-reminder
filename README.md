# GitHub Reminder

GitHub reminder is a bot that parses issues looking for dates and applies labels according to them.

The bot simply looks for lines like `deadline is June 20th 2015` and every day applies the most
adequate label to it.

The most adequate label is chosen from the labels already exisitng in the repository following
the syntax `deadline < 30`, `deadline < 5` etc.

If the deadline is on 31 days or more no label is applied, if it's in between 6 days and 30
the `deadline < 30` will be applied. Finally for 5 days or less `deadline < 5` will
apply.