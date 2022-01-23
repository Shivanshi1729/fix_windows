---
title: "software"
bg: purple
color: white
fa-icon: cloud-upload
---

Make another autohotkey file for this `shortcut.ahk` and add this to startup.

- Here is how you block certain annoying windows shortcuts
  - Like `Start` + `c`, opens cortana, 
    which is annoying, you can add this to `shortcut.ahk` file

```ahk
; stop cortana from opening
#c::
sleep 1
return
```

- We don't use `Capslock` that often, so i switched it with `Esc`

```ahk
; switch capslock with esc key
Capslock::Esc
```

- We close windows many times, but the shortcut to close windows is
  not that easy to press, so i changed it to `Start` + `Shift` + `q`

```ahk
; close a window
#<+q::WinClose A
return
```

- Window clipboard history is not that feature rich, so I use copyQ,
  and override the `Start` + `v` shortcut with `copyQ toggle` one.
  Make sure to change the location to where `copyQ` is installed.

```ahk
; open copy q
#v::
 run, C:\Program Files (x86)\CopyQ\copyq.exe toggle
return
```

- I also use this to open a terminal, but I still have some
  problems with how it works.

```ahk
; open terminal ---> too slow didn't work cannot focus the terminal
#Enter::
    run wt
return
```

> Now you can shortcut to programs you open frequently.