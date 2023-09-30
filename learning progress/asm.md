
# Assembly Language

> ## Documentando a documentação
>
> - Qualquer coisa entre '-' é conseiderada um argumento  
> - Em maiusculo são instruções  
>

---

> ## Sumário
>
> 1. [Conceitos](#conceitos_básicos);
> 1. [Comandos](#commads);
>
>    - [Load](#ld_--value);
>    - [Store](#st_--value);
>    - [Transfer](#t__);
>    - [Increment](#in_);
>    - [Decrement](#de_);
>
> 1. [Fontes](#fontes);

---

> ## Conceitos_Básicos
>
> **Registradores**:
>
>
>
> - X | A | Y:
>   - São os registradores mutaveis e utilizaveis.
>   - Cada um consegue segurar no máximo 1 byte (#$ff)
> - PC | SP:
>   - SP(Stack Pointer) é alguma coisa
>   - PC(Program Counter) Contador/ mostra onde o programa está(Linha tal)
> - NV-BDIZC:
>   - Essas são as flags do processador.
>   - Flags:
>       1. **C** = **C**arry flag
>           - Setada quando tem um overflow dos 8 bits ou um underflow.  
>       1. **Z** = **Z**ero Flag
>           - Setada quando a ultima operação deu 0
>       1. **I** = **I**nterrupt Disable
>           - Setada a partir da instrução SEI(Set Interrupt Disable).
>           - Faz com que não seja possivel interromper o programa até que apareça a instrução CLI(Clear Interrupt Disable)
>       1. **D** = **D**ecimal Mode
>           - Setada a partir do SED(Set Decimal Flag)
>           - Quando ativa(Valor 1) Utiliza as regras do [BCD](https://www.osdata.com/topic/language/asm/bcdarith.htm)(binary Coded Decimals)
>       1. **B** = **B**reak command
>           - Setado com a intrução BRK
>           - Pode ser de 2 bits em algumas situações (aparentemente)
>           - N entendi
>       1. **V** = o**V**erflow Flag
>           - Define se ultrapassou o limite de bits em um número.
>       1. **N** = **N**egative flag
>           - Definida quando o ultimo bit é 1
>           - Significando que o resultado é negativo
> - **Branches**: São pontos de voltar.  
>   

---

> ## Commads
>
> ### **LD_** -value-
>
> - X: Carrega o valor -value- ao registrador X
> - Y: Carrega o valor -value- ao registrador Y
> - A: Carrega o valor -value- ao registrador A
>
> ### **ST_** -value-
>
> - X: Salva o valor do registrador X no -value- que é um espaço de memória
> - Y: Salva o valor do registrador Y no -value- que é um espaço de memória
> - A: Salva o valor do registrador A no -value- que é um espaço de memória
>
> ### **ADC** -value-
>
> - Adiciona ao carry flag o -value-
>
> ### **SBC** -value-
>
> - Subtrai o -value- do carry flag
>
> ### **IN_**
>
> - X: Incrementa 1 em X.
> - Y: Incrementa 1 em Y.
>
> ### **DE_**
>
> - X: Decrementa 1 em X.
> - Y: Decrementa 1 em Y.
>
> ### **T__**
>
> - AX: Copia o valor de A para X.
> - XA: Copia o valor de X para A.
> - AY: Copia o valor de A para Y.
> - YA: Copia o valor de Y para A.
> - YX: Copia o valor de Y para X.
> - XY: Copia o valor de X para Y.
>
> ### **CP_** -value-
>
> - X: Compara o valor de X com o -value-.
> - Y: Compara o valor de Y com o -value-.
> 

---

> ## Fontes
>
> - [Easy 6502](http://skilldrick.github.io/easy6502/)
> - [Free-Programming-Books](https://github.com/EbookFoundation/free-programming-books)
> - [Registradores](https://web.archive.org/web/20210626024532/http://www.obelisk.me.uk/6502/registers.html)