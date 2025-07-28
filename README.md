# Interpretador de Comandos com Pipes e Redirecionamento (C)

## Linguagem Utilizada

- C (linguagem de programação de baixo nível)
- Uso intensivo de chamadas de sistema Unix (`fork`, `pipe`, `dup2`, `execvp`, `waitpid`)

## Funcionalidades

Este projeto implementa um interpretador de linha de comando com suporte a:

- Execução de comandos digitados na linha de comando
- Uso de **pipes (`|`)** entre comandos (ex: `ls -l | grep txt`)
- **Redirecionamento de entrada (`<`)** e **saída (`>`)** de arquivos (ex: `cat < entrada.txt > saida.txt`)
- Processamento dinâmico com criação de processos filhos para cada comando

### Chamadas de sistema utilizadas

- `fork()` — Criação de novos processos
- `pipe()` — Comunicação entre processos
- `dup2()` — Redirecionamento de entrada e saída padrão
- `execvp()` — Execução de comandos digitados
- `waitpid()` — Espera pela finalização dos processos filhos

## Como Executar

### 🪟 No Windows (com WSL)

> ⚠️ Este projeto exige um ambiente Unix-like. No Windows, é necessário usar WSL ou uma máquina virtual com Linux.

1. Instale o WSL com Ubuntu ou Debian
2. Coloque o `main.c` em uma pasta acessível
3. Compile com:
   ```bash
   gcc main.c -o interpretador
   ```
4. Execute com:
   ```bash
   ./interpretador
   ```

### 🐧 No Linux

1. Abra o terminal e vá até a pasta onde está o `main.c`
2. Compile o código com:
   ```bash
   gcc main.c -o interpretador
   ```
3. Execute o interpretador com:
   ```bash
   ./interpretador
   ```

### Exemplo de uso

```bash
$ ls -l | grep .c > arquivos_c.txt
```

## Nome sugerido para repositório

**interpretador-shell-c**

## Autor

**Igor Resende Brito**
