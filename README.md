# Raspagem-de-Dados

# Web Scraper para Mercado Livre

Este projeto é um script simples de Web Scraping desenvolvido em Python, projetado para extrair informações de produtos do site Mercado Livre. Ele busca por um item específico, coleta dados como descrição, preço e link, e os organiza em um arquivo CSV para fácil visualização e análise.

## Funcionalidades

-   **Busca Dinâmica:** Pesquisa por qualquer produto no Mercado Livre alterando apenas uma linha no código.
-   **Extração de Dados:** Coleta as seguintes informações de cada item na página de resultados:
    -   Descrição do produto
    -   Preço
    -   Link direto para a página do produto
-   **Exportação para CSV:** Salva todos os dados coletados em um arquivo `.csv` chamado `produtos_mercado_livre_novo.csv`.

## Como Usar

Siga os passos abaixo para executar o script e realizar sua própria busca.

### 1. Pré-requisitos

Certifique-se de que você tem o **Python 3** instalado em sua máquina.

### 2. Instalação

Primeiro, clone ou faça o download deste projeto. Em seguida, instale as bibliotecas necessárias executando o seguinte comando no seu terminal:

```bash
pip install requests beautifulsoup4
```

### 3. Execução

1.  Abra o arquivo de script Python em um editor de texto ou IDE.
2.  Navegue até a **última linha** do arquivo.
3.  Altere o nome do produto dentro da função `pesquisa_mercado_livre()` para o item que você deseja pesquisar.

    ```python
    # Altere para o produto que você deseja pesquisar
    pesquisa_mercado_livre('card pokemon')
    ```

4.  Salve o arquivo e execute-o pelo terminal:

    ```bash
    python seu_script.py
    ```

Após a execução, um arquivo chamado `produtos_mercado_livre_novo.csv` será criado no mesmo diretório, contendo a lista de produtos encontrados.

## Dependências

Este script depende das seguintes bibliotecas Python:

-   `requests`: Para realizar as requisições HTTP e obter o conteúdo HTML da página.
-   `BeautifulSoup4`: Para fazer o parsing do HTML e facilitar a busca por elementos.
-   `csv`: (Biblioteca padrão do Python) Para criar e escrever no arquivo de saída `.csv`.

## Melhorias Futuras

O projeto pode ser aprimorado com as seguintes funcionalidades:

-   **Implementar a ordenação por preço:** Adicionar uma lógica para organizar a lista de produtos do **mais barato para o mais caro** antes de salvar os dados no arquivo CSV.
-   **Suporte a múltiplas páginas:** Adicionar a capacidade de navegar pelas páginas de resultados para coletar mais produtos.
