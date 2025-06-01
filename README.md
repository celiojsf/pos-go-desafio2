# Desafio 2 - Desafio Multi Threading

Este projeto consiste em um programa Go que faz consultas concorrentes a duas APIs de CEP (BrasilAPI e ViaCEP) utilizando goroutines e canais. O objetivo é retornar a resposta da API que responder primeiro ou informar timeout após 3 segundos.

## Como executar

```sh
go run main.go <CEP>
```

Exemplo:

```sh
go run main.go 01001-000
```

ou

```sh
go run main.go 01001000
```

## Funcionamento
- O programa recebe o CEP como argumento.
- Faz duas chamadas concorrentes para:
  - https://brasilapi.com.br/api/cep/v1/<CEP>
  - http://viacep.com.br/ws/<CEP>/json/
- Imprime a resposta da API que retornar primeiro.
- Se nenhuma responder em até 3 segundos, imprime mensagem de timeout.

## Requisitos
- Go 1.18 ou superior
- Acesso à internet

---

Projeto para fins de estudo de concorrência em Go.