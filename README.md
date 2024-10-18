# estudo de comeco NASM
## primeiros comandos

* Programa hello world

```Assembly


global _start
    section .text
    _start:
      mov rax,1       ;prepara o sistema para fazer a escrita de um texto;
      mov rdi,1       ;preparar a saida do texto  na  tela
      mov rsi,message ;imprimir a mensagem na tela
      mov rdx,13      ;quantidade de caracteres
      syscall         ;chama o sistema para a preparar a saida
      mov rax,60      ;chamada para a saida do sistema
      xor rdi,rdi     ;executar a saida do sistema
      syscall         ;invocar o sistema operacional para fechar

      section .data
      message:db "hello,world" ,10    ;O valor 10 representa a quebra de linha 

      ```
