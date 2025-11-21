# Consumidor de API ViaCEP

Aplicação Java para consulta de endereços via API REST e salvamento dos dados em JSON.

## 🎯 Sobre o Projeto

Sistema que consome a API do ViaCEP para buscar informações de endereço através do CEP. A aplicação faz requisições HTTP, processa a resposta JSON e salva os dados em arquivo local.

## 🚀 Funcionalidades

-  Consumo da API REST ViaCEP
-  Requisições HTTP com HttpClient
-  Conversão de JSON para objetos Java com Gson
-  Salvamento de dados em arquivo JSON formatado
-  Tratamento de exceções
-  Interação via linha de comando

## 🛠️ Tecnologias Utilizadas

- **Java 21** (OpenJDK)
- **Gson 2.13.2** - Manipulação de JSON
- **HttpClient** (java.net.http) - Cliente HTTP nativo
- **Records** - Estrutura de dados imutável
- **ViaCEP API** - Consulta de CEPs

## 📁 Estrutura do Projeto
```
src/
├── ConsultaCep.java         # Requisições HTTP à API
├── Endereco.java            # Record para dados do endereço
├── GeradorDeArquivo.java    # Gravação de arquivos JSON
└── Principal.java           # Classe principal (main)
```

## 💻 Como Executar

**Pré-requisitos:**
- Java 21 ou superior
- Biblioteca Gson 2.13.2

**Compilar:**
```bash
javac -cp "dependencias/gson-2.13.2.jar" src/*.java
```

**Executar:**
```bash
java -cp "src:dependencias/gson-2.13.2.jar" Principal
```

**Uso:**
```
Digite um número de CEP para consulta:
01001000
```

**Saída:**
```
Endereco[cep=01001-000, logradouro=Praça da Sé, complemento=lado ímpar, localidade=São Paulo, uf=SP]
```

## 📊 Arquivo Gerado

A aplicação cria um arquivo JSON com o nome do CEP consultado:

**01001-000.json:**
```json
{
  "cep": "01001-000",
  "logradouro": "Praça da Sé",
  "complemento": "lado ímpar",
  "localidade": "São Paulo",
  "uf": "SP"
}
```

## 🔧 Conceitos Aplicados

- **HttpClient** - Cliente HTTP nativo do Java para requisições
- **HttpRequest** - Construção de requisições HTTP
- **Records** - Estrutura de dados imutável (Java 14+)
- **Gson** - Serialização e deserialização JSON
- **FileWriter** - Escrita de arquivos
- **Try-Catch** - Tratamento de exceções (IOException, RuntimeException)
- **Scanner** - Leitura de entrada do usuário

## 🔗 API Utilizada

[ViaCEP](https://viacep.com.br/) - API gratuita para consulta de CEPs brasileiros

**Endpoint:** `https://viacep.com.br/ws/{cep}/json/`

## ⚙️ Detalhes Técnicos

- **URI.create()** - Criação de URIs para requisições
- **HttpRequest.newBuilder()** - Padrão Builder para requisições HTTP
- **HttpResponse.BodyHandlers.ofString()** - Tratamento de resposta como String
- **GsonBuilder().setPrettyPrinting()** - Formatação legível do JSON
- **Record** - Classe imutável com cep, logradouro, complemento, localidade e uf

## 👨‍💻 Desenvolvimento

Projeto desenvolvido para praticar:
- Consumo de APIs REST
- Manipulação de JSON em Java
- Requisições HTTP
- Persistência de dados

---

⭐ Projeto criado para estudos de integração com APIs em Java