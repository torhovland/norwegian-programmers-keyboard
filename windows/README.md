# Note about Backspace and Caps Lock
It seems that the Windows keyboard layouts don't support swapping Backspace and
Caps Lock. But you can do it with AutoHotkey by adding the following lines to
your AutoHotkey.ahk file:

    #IfWinNotActive ahk_class VMPlayerFrame
    Capslock::Backspace
    Backspace::Capslock
    #IfWinNotActive
