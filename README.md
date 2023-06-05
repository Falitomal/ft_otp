<h1 align="center">
  ft_otp - 42 Bootcamp Cybersec
</h1>

<p align="center">
	<b><i>OTP (Time-Based One Time Password)</i></b><br>
</p>

<p align="center">
	<img alt="GitHub code size in bytes" src="https://img.shields.io/github/languages/code-size/Falitomal/ft_otp?color=lightblue" />
	<img alt="Code language count" src="https://img.shields.io/github/languages/count/Falitomal/ft_otp?color=yellow" />
	<img alt="GitHub top language" src="https://img.shields.io/github/languages/top/Falitomal/ft_otp?color=blue" />
	<img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/Falitomal/ft_otp?color=green" />
</p>



## ✏️ Summary
```

Implement a TOTP (Time-Based One Time Password) system in any language, capable of generating ephemeral passwords from a master key.
Encrypting a text and then generating the TOTP.

```
## 💡 Example 

```

$ echo -n "Hello World" > key.txt
$ ./ft_otp -g ket.txt

Error: the key must be at least 64 hexadecimal characters.

$ echo "794a902e58f454807822904e71150ef100807253d749384848002ec1c8ccc5490b" > key.txt
$ ./ft_otp -g key.txt
Key stored in 'ft_otp.key'.
File 'ft_otp.key' encrypted with password.

$ ./ft_otp -k ft_otp.key

Key (Correct): 557220 = pyotp
Generated Code : 557220

$ sleep 60
$ ./ft_otp -k ft_otp.key

Key (Correct): 453220 = pyotp
Generated Code : 453220

```
## 🛠️ Usage  ft_otp

```

usage: ft_otp [-h] [-g fichero] [-k fichero] [-qr fichero]

optional arguments:
  -h, --help   show this help message and exit
  -g fichero   almacena una clave hexadecimal de 64 caracteres mínimo en un
               fichero 'ft_otp.key'.
  -k fichero   genera una contraseña temporal usando un fichero y la muestra
               por pantalla.
  -qr fichero  muestra un QR con la clave secreta.

```
