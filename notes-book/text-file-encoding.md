# Test File Encoding

| Hexadecimal Representation  | Encoding                                                   | Decimal Representation  |
|-----------------------------|------------------------------------------------------------|-------------------------|
| `EF BB BF    `              | UTF-8                                                      | 239 187 191             |
| `FE FF       `              | UTF-16, big endian                                         | 254 255                 |
| `FF FE       `              | UTF-16, little endian (Notepad++ calls this UCS-2 LE BOM)  | 255 254                 |
| `00 00 FE FF `              | UTF-32, big-endian                                         | 0 0 254 255             |
| `FF FE 00 00 `              | UTF-32, little endian                                      | 255 254 0 0             |
| `2B 2F 76 38 `              | UTF-7                                                      | 43 47 118 56            |
| `2B 2F 76 39 `              | UTF-7                                                      | 43 47 118 57            |
| `2B 2F 76 2B `              | UTF-7                                                      | 43 47 118 43            |
| `2B 2F 76 2F `              | UTF-7                                                      | 43 47 118 47            |
| `F7 64 4C    `              | UTF-1                                                      | 247 100 76              |
| `DD 73 66 73 `              | UTF-EBCDIC                                                 | 221 115 102 115         |
| `0E FE FF    `              | SCSU                                                       | 14 254 255              |
| `FB EE 28    `              | BOCU-1                                                     | 251 238 40              |
| `84 31 95 33 `              | GB-18030                                                   | 132 49 149 51           |


https://msdn.microsoft.com/en-us/library/windows/desktop/dd374101(v=vs.85).aspx
https://en.wikipedia.org/wiki/Byte_order_mark




```
Note   Windows default is UTF-16, little endian byte order.



  
ASCII Code Space is 0-255 broken up like this
0:       NUL
0-31:    Control characters
32-126:  Printable characters


1-127: Standard codes
128-255: Locale specific codepage, often Windows 1252, or ISO 8859


ASCII: https://en.wikipedia.org/wiki/ASCII



Decimal  Hex  Abbr  CC     Esc  Name
0        00   NUL   ^@     \0   Null
1        01   SOH   ^A          Start of Heading
2        02   STX   ^B          Start of Text
3        03   ETX   ^C          End of Text, Interrupt
4        04   EOT   ^D          End of Transmission
5        05   ENQ   ^E          Enquiry
6        06   ACK   ^F          Acknowledgement
7        07   BEL   ^G     \a   Bell
8        08   BS    ^H     \b   Backspace
9        09   HT    ^I     \t   Horizontal Tab
10       0A   LF    ^J     \n   Line Feed
11       0B   VT    ^K     \v   Vertical Tab, Line Tabulation
12       0C   FF    ^L     \f   Form Feed
13       0D   CR    ^M     \r   Carriage Return
14       0E   SO    ^N          Shift Out
15       0F   SI    ^O          Shift In
16       10   DLE   ^P          Data Link Escape
17       11   DC1   ^Q          Device Control 1 (often XON)
18       12   DC2   ^R          Device Control 2
19       13   DC3   ^S          Device Control 3 (often XOFF)
20       14   DC4   ^T          Device Control 4
21       15   NAK   ^U          Negative Acknowledgement
22       16   SYN   ^V          Synchronous Idle
23       17   ETB   ^W          End of Transmission Block
24       18   CAN   ^X          Cancel
25       19   EM    ^Y          End of Medium
26       1A   SUB   ^Z          Substitute, ***EOF?***
27       1B   ESC   ^[     \e   Escape
28       1C   FS    ^\          File Separator
29       1D   GS    ^]          Group Separator
30       1E   RS    ^^[k]       Record Separator
31       1F   US    ^_          Unit Separator
127      7F   DEL   ^?          Delete



Character Type                 Seq      Number of symbols
C0 controls                    0-31     32 control codes
Space                          32       The only "invisible" printable
Punctuation and Symbols        33-47    !"#$%&'()*+,-./
ASCII digits                   48-57    0123456789
Punctuation and Symbols        58-64    :;<=>?@
Uppercase Latin Alphabet       65-90    
Punctuation and Symbols        91-96    [\]^_`
Lowercase Latin Alphabet       97-122   
Punctuation and Symbols        123-126  {|}~
Control character              127      1 control code containing the "Delete" character.


 
 
https://en.wikipedia.org/wiki/Whitespace_character
Other printables from Latin-1 Supplement
133      85                     Next line
160      A0                     No-break space
183      B7                     Middle dot



```

