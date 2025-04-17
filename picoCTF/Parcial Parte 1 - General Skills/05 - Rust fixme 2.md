## **Descripción**
Have you heard of Rust? Fix the syntax errors in this Rust file to print the flag!Download the Rust code [here](https://challenge-files.picoctf.net/c_verbal_sleep/3f0e13f541928f420d9c8c96b06d4dbf7b2fa18b15adbd457108e8c80a1f5883/fixme1.tar.gz).
## Hints
1. Cargo is Rust's package manager and will make your life easier. See the getting started page [here](https://doc.rust-lang.org/book/ch01-03-hello-cargo.html)
2. Rust has some pretty great compiler error messages. Read them maybe?
3. printIn
## **Solución** 
Para este reto haremos lo siguiente:
- Descargamos el codigo Rust con wget.
- Lo ejecutamos utilizando cargo run.
- Pare este reto solo basta con leer y entender el código y el lenguaje de programación para arreglar los problemas de sintaxis.
```
┌──(kali㉿kali)-[~/…/GENERAL SKILLS/Rust_FixMe_2/fixme2/src]
└─$ cargo run main.rs
   Compiling rust_proj v0.1.0 (/home/kali/Documents/COMPETICION PICOCTF/GENERAL SKILLS/Rust_FixMe_2/fixme2)
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.31s
     Running `/home/kali/Documents/COMPETICION PICOCTF/GENERAL SKILLS/Rust_FixMe_2/fixme2/target/debug/rust_proj main.rs`
Using memory unsafe languages is a: PARTY FOUL! Here is your flag: picoCTF{4r3_y0u_h4v1n5_fun_y31?}

```

## **Notas adicionales**

## **Referencias**
https://doc.rust-lang.org/book/ch01-03-hello-cargo.html
https://doc.rust-lang.org/std/macro.println.html
	