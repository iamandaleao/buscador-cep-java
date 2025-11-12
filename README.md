# 🔍 Buscador de CEP

Aplicação Java desenvolvida como desafio do programa **ONE - Oracle Next Education** em parceria com a **Alura**, que realiza a consulta de endereços através da API ViaCEP.

## 📋 Sobre o Projeto

Este projeto consiste em uma aplicação que permite ao usuário buscar informações de endereço através do CEP, consumindo a API pública do ViaCEP. Os dados retornados são exibidos na aplicação e salvos em um arquivo JSON.

Similar ao que acontece em formulários web modernos, ao digitar o CEP, o endereço é retornado automaticamente com informações como logradouro, bairro, cidade e estado.

## 🚀 Funcionalidades

- Consumo da API ViaCEP
- Menu interativo para entrada do CEP
- Exibição dos dados do endereço
- Geração automática de arquivo JSON com as informações consultadas

## 🔧 Tecnologias Utilizadas

- Java
- API ViaCEP
- Biblioteca para manipulação de JSON

## 📦 Exemplo de Resposta da API

Ao consultar o CEP `01001-000`, a API retorna:
```json
{
  "cep": "01001-000",
  "logradouro": "Praça da Sé",
  "complemento": "lado ímpar",
  "bairro": "Sé",
  "localidade": "São Paulo",
  "uf": "SP",
  "ibge": "3550308",
  "gia": "1004",
  "ddd": "11",
  "siafi": "7107"
}
```

## 💻 Como Usar

1. Clone este repositório
2. Execute a aplicação Java
3. Informe o CEP desejado no menu interativo
4. Visualize os dados do endereço
5. O arquivo JSON será gerado automaticamente

## 🌐 API Utilizada

- **ViaCEP**: https://viacep.com.br/
- **Endpoint**: `https://viacep.com.br/ws/{CEP}/json/`

## 📚 Aprendizados

Este projeto foi desenvolvido como parte do programa ONE, aplicando conceitos de:
- Consumo de APIs REST
- Manipulação de dados JSON
- Interação com usuário via console
- Manipulação de arquivos em Java

⭐ Projeto desenvolvido durante o programa ONE/Oracle + Alura