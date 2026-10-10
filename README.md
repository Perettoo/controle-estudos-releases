# Controle de Estudos — releases

Este repositório existe só para distribuir os instaladores do app
**Controle de Estudos**. O código-fonte fica em um repositório privado.

Cada release traz três arquivos:

| Arquivo | Para que serve |
| --- | --- |
| `Controle de Estudos_<versão>_x64-setup.exe` | o instalador |
| `..._x64-setup.exe.sig` | a assinatura do instalador (minisign / Ed25519) |
| `latest.json` | o manifesto que o atualizador do app lê |

O app instalado consulta o `latest.json` da release mais recente, compara
a versão anunciada com a sua e, antes de instalar qualquer coisa, confere
a assinatura contra a chave pública embutida no próprio binário. Um
arquivo que não bate com a chave é recusado.

## Primeira instalação

Baixe o `.exe` da release mais recente e execute. Dali em diante o
próprio app avisa quando há versão nova.
