# hexdump2bin

## What's this?

    $ python hexdump2bin.py -h
    Usage: ./hexdump2bin.py [options] IN_FILE OUT_FILE
    
    Options:
      -h, --help  show this help message and exit

`IN_FILE`に、**hexdump**などによって出力されたバイナリデータのアスキー文字列を指定すると、  
`OUT_FILE`に元のバイナリデータを抽出します。

## Example
こんなかんじで使います。

    $ hexdump /bin/ls > ls_org.hex
    $ hexdump /bin/ls > ls_org.hex
    $ python hexdump2bin.py ls_org.hex ls.bin
    [*] Reading from ls_org.hex
    [*] Analyzing...
    [*] Dumping to ls.bin
    $ diff /bin/ls ls.bin 
    $ 
