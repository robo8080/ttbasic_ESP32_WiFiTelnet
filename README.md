TOYOSHIKI Tiny BASIC for Arduino(ESP32/ESP-WROOM-32) WiFi Telnet対応版

オリジナルのArduino版からの変更点<br>
1.WiFi経由でのTelnet接続対応。Portは10001<br>
2.PRINT命令のエスケープシーケンス対応<br>

basic.cppのssidとpasswordは自分の環境に合わせて書き換えて下さい。<br>
ESP32/ESP-WROOM-32に割り振られるIPアドレスはArduino IDEのシリアルモニタで確認して下さい。<br>
Telnet接続の動作確認はWindows10＋TeraTermで行いました。<br>

The code tested in ESP32-DevKitC.<br>
Use UART terminal, or temporarily use Arduino IDE serial monitor.

Operation example

&gt; list<br>
10 FOR I=2 TO -2 STEP -1; GOSUB 100; NEXT I<br>
20 STOP<br>
100 REM Subroutine<br>
110 PRINT ABS(I); RETURN

OK<br>
&gt;run<br>
2<br>
1<br>
0<br>
1<br>
2

OK<br>
&gt;

The grammar is the same as<br>
PALO ALTO TinyBASIC by Li-Chen Wang<br>
Except 3 point to show below.

(1)The contracted form of the description is invalid.

(2)Force abort key<br>
PALO ALTO TinyBASIC -> [Ctrl]+[C]<br>
TOYOSHIKI TinyBASIC -> [ESC]<br>
NOTE: Probably, there is no input means in serial monitor.

(3)Other some beyond my expectations.

(C)2012 Tetsuya Suzuki<br>
GNU General Public License
