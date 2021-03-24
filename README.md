# fctletterhead

Letterhead paper for FCT-NOVA (NOVA School of Science and Technology)

## Preâmbulo

A versão mais recente deste pacote está disponível para download em:

https://github.com/joaomlourenco/fctletterhead

Se não tem a certeza se está a utilizar a versão mais recente, aproveite e [faça download](https://github.com/joaomlourenco/fctletterhead/archive/refs/heads/main.zip) da última versão!   Já agora, se achar este pacote útil, [ofereça um café](https://www.paypal.com/donate/?hosted_button_id=8WA8FRVMB78W8) ao meu alter-ego *NOVAthesis* e na caixa de comentários diga que é para o pacote “*fctletterhead*”! ;)


## Ler o Pacote “*fctletterhead*”

Na verdade é muito simples usar este pacote ““*fctletterhead*””…  basta adicionar no preâmbulo do ficheiro fonte, i.e., depois do `\docuemntclass{…}` e antes do `\begin{document}`, o seguinte comando:

```latex
\begin{verbatim}
  \usepackage{fctletterhead}
\end{verbatim}
```

onde apenas a primeira página será *timbrada*; ou

```latex
\begin{verbatim}
  \usepackage[everypage]{fctletterhead}
\end{verbatim}
```

onde todas as páginas serão timbradas.

## Configurar o Pacote “*fctletterhead*”

Depois, ainda no preâmbulo, deverá configurar os seus dados e os do seu departamento

| Opção | Efeito |
|----------|----------|
| \fctdepartment | Este comando recebe dois argumentos, o primeiro com o nome do departamento em Português e o segundo com o nome do departamento em Inglês, a serem apresentados no canto superior direito (convertidos em maiúsculas).  *Se omitido nada será apresentado em cima à direita.*|
| \fctphone+   | Este comando recebe como argumento o telefone do autor, a colocar no rodapé (em baixo à direita). *Se omitido apresentará o telefone geral da FCT-NOVA.*|
| \fctext   | Este comando recebe como argumento uma extensão telefónica, a colocar no rodapé à direita do telefone. *Se omitido será apresentado apenas o número de telefone (sem extensão).*|
| \fctemail  | Este comando recebe como argumento um email, a colocar no rodapé por baixo do telefone/extensão. *Se omitido nada será apresentado.*|
| \fcturl   | Este comando recebe como argumento um url, a colocar no rodapé por baixo do email. *Se omitido nada será apresentado.*|
| \fctauthor     | Este comando recebe como argumento o nome do autor, a colocar na zona de assinatura.  *Se omitido nada será apresentado.*|
| \fctposition   | Este comando recebe como argumento o cargo do autor (ou outro texto), a colocar na zona de assinatura, por baixo do nome.  Pode-se utilizar `\\` para partir este campo em várias linhas.*Se omitido nada será apresentado.*|


## Configurar e Apresentar a Zona de Assinatura

Há também um comando para criar uma zona para colocar uma assinatura.  Este comando tem três argumentos, sendo que o primeiro (entre “`[…]`”) é opcional.

```latex
\begin{verbatim}
  \fctsignature[tamanho_da_linha]{posição_da_zona}{afastamento_do_texto_acima}
\end{verbatim}
```

onde:

| argumento | valor |
|----------------|--------|
| tamanho_da_linha | *Opcional* — Indicação do tamanho da linha (em qualquer unidade válida no LaTeX, por exemplo, *6cm*, *2in*, *30pt*, etc).  *Se omitido desenha uma linha com 5cm.*|
| posição_da_zona | *Obrigatório* — Indicação da localização da zona de assinatura.  Valores possíveis: `l` zona de assinatura à esquerda; `l` zona de assinatura centrada; e `r`  zona de assinatura à direita. |
| afastamento_do_texto_acima | *Obrigatório* — Indicação do espaço a deixar para colocar a assinatura (em qualquer unidade válida no LaTeX, por exemplo, *3cm*, *2.5in*, *10ex*, etc). |

A zona de assinatura que termina este documento, localizada em baixo à direita, foi criada com:

```latex
\begin{verbatim}
  \fctsignature[6cm]{r}{2cm}
\end{verbatim}
```
