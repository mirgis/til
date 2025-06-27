# Monday in Calendar

```bash
$ lsb_release -a | grep "Desc"
Description:	Ubuntu 24.04.1 LTS
```

If you have your operating system set to American English but still want to have set Monday as a first day in a week in a calendar [^1], open this file,
```bash
$ sudo vim /etc//usr/share/i18n/locales/en_US
```

search for the word "week" and add these two lines below it,
```vim
week            7;19971130;5
first_weekday   2
first_workday   2
```
update the system,
```bash
$ sudo locale-gen
```
then log out and log in.

### References
[^1]: [Monday as First Day in GNOME Shell (instead of Sunday)](https://askubuntu.com/questions/197613/monday-as-first-day-in-gnome-shell-instead-of-sunday)
