# Scraping Certidões API

API HTTP para consultar 16 certidões a partir de um CPF ou CNPJ, pronta para integração com n8n, WhatsApp e outros sistemas.

## Descrição

Esta API utiliza o Selenium para realizar scraping em portais oficiais do governo brasileiro, permitindo a consulta de diversas certidões, como Certidão de Débitos, Certidão Negativa de Débitos, entre outras. O objetivo é facilitar o acesso a informações importantes de forma automatizada.

## Estrutura do Repositório
├── main.py # FastAPI app com todos os endpoints e lógica de scraping 
├── requirements.txt # Dependências (fastapi, selenium, requests, etc) 
├── render.yanl 
├── README.md 
# Instruções de uso


## URLs das Certidões

As seguintes URLs são utilizadas para acessar as certidões:

1. **Certidão de Débitos**: [Certidão de Débitos](https://www.gov.br/receitafederal/pt-br/assuntos/servicos/certidoes/certidao-de-debitos)
2. **Certidão Negativa de Débitos**: [Certidão Negativa de Débitos](https://www.gov.br/receitafederal/pt-br/assuntos/servicos/certidoes/certidao-negativa-de-debitos)
3. **Certidão de Regularidade Fiscal**: [Certidão de Regularidade Fiscal](https://www.gov.br/receitafederal/pt-br/assuntos/servicos/certidoes/certidao-de-regularidade-fiscal)
4. **Certidão de Distribuição**: [Certidão de Distribuição](https://www.tjsp.jus.br/CertidaoDistribuicao)
5. **Certidão de Protesto**: [Certidão de Protesto](https://www.protesto.com.br/certidao)
6. **Certidão de Ações Trabalhistas**: [Certidão de Ações Trabalhistas](https://www.trt1.jus.br/consultas/certidao)
7. **Certidão de Ações Cíveis**: [Certidão de Ações Cíveis](https://www.tjsp.jus.br/CertidaoAcoesCiveis)
8. **Certidão de Inexistência de Débitos**: [Certidão de Inexistência de Débitos](https://www.gov.br/receitafederal/pt-br/assuntos/servicos/certidoes/certidao-inexistencia-de-debitos)
9. **Certidão de Regularidade do FGTS**: [Certidão de Regularidade do FGTS](https://www.gov.br/fgts/pt-br/consultas/certidao)
10. **Certidão de Regularidade do INSS**: [Certidão de Regularidade do INSS](https://www.gov.br/inss/pt-br/consultas/certidao)
11. **Certidão de Regularidade do Simples Nacional**: [Certidão de Regularidade do Simples Nacional](https://www.gov.br/receitafederal/pt-br/assuntos/servicos/certidoes/certidao-simples-nacional)
12. **Certidão de Regularidade do ICMS**: [Certidão de Regularidade do ICMS](https://www.gov.br/receitafederal/pt-br/assuntos/servicos/certidoes/certidao-icms)
13. **Certidão de Regularidade do ISS**: [Certidão de Regularidade do ISS](https://www.gov.br/receitafederal/pt-br/assuntos/servicos/certidoes/certidao-iss)
14. **Certidão de Regularidade do IPVA**: [Certidão de Regularidade do IPVA](https://www.gov.br/receitafederal/pt-br/assuntos/servicos/certidoes/certidao-ipva)
15. **Certidão de Regularidade do ITR**: [Certidão de Regularidade do ITR](https://www.gov.br/receitafederal/pt-br/assuntos/servicos/certidoes/certidao-itr)
16. **Certidão de Cadastro Nacional**: [Certidão de Cadastro Nacional](https://www.gov.br/receitafederal/pt-br/assuntos/servicos/certidoes/certidao-cadastro-nacional)

## Como Rodar a API

### Pré-requisitos

1. **Python 3.7 ou superior**: Certifique-se de que o Python está instalado em sua máquina. Você pode baixar o Python [aqui](https://www.python.org/downloads/).
2. **ChromeDriver**: O ChromeDriver deve ser instalado e configurado no seu PATH. Você pode baixar a versão correspondente ao seu navegador [aqui](https://sites.google.com/chromium.org/driver/).

### Passos para Executar

1. **Clone o repositório**:
   ```bash
    git clone https://github.com/Jcsalcobassa/scraping-certidoes-api.git
   cd scraping-certidoes-api
