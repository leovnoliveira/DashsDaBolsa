# Dashboards Contábeis das Empresas da B3

Este repositório contém um aplicativo desenvolvido em [Shiny](https://shiny.rstudio.com/), que apresenta os demonstrativos contábeis e o Balanço Patrimonial de todas as empresas listadas na bolsa de valores brasileira (B3). O aplicativo foi desenvolvido utilizando a linguagem R e pode ser acessado [aqui](https://leovnoliveira.shinyapps.io/dashsdabolsa/).

### Funcionalidades

- **Visualização de Demonstrativos Contábeis**: Acesse e visualize os demonstrativos financeiros de todas as empresas da B3.
- **Balanço Patrimonial**: Acesse os Balanços Patrimoniais Ativo (BPA) e Passivo (BPP) das empresas, apresentados de forma clara e interativa.
- **Indicadores Financeiros**: Consulte indicadores de liquidez (Liquidez Corrente, Liq. Imediata, Liq. Seca, Liq. Geral), de endividamento (Dívida/PL, Dívida/Ativos, Dívida/EBIT, PL/Ativos, Passivos/Ativos) de margem (Margem Bruta, Margem Líquida, Margem EBIT) e de rentabilidade (ROIC, ROE, ROA).
- **Atualização Automática**: Os dados são atualizados automaticamente por meio de um workflow configurado no GitHub Actions.

## Dados

Os dados utilizados neste aplicativo foram obtidos por meio do pacote [GetDFPData2](https://github.com/msperlin/GetDFPData2), desenvolvido por Marcelo S. Perlin. Este pacote permite acessar e manipular os dados financeiros diretamente das demonstrações financeiras publicadas pelas empresas na B3.

### Instalação do GetDFPData2

Para utilizar este pacote, siga os passos abaixo:

1. Instale o pacote `GetDFPData2` diretamente do GitHub utilizando o comando:

    ```r
    # Instale as dependências necessárias
    install.packages("remotes")
    remotes::install_github("msperlin/GetDFPData2")
    ```

2. Carregue o pacote no seu script R:

    ```r
    library(GetDFPData2)
    ```

## Desenvolvimento

O desenvolvimento deste aplicativo foi feito utilizando a IDE [Posit Cloud](https://posit.cloud/), que oferece um ambiente RStudio na nuvem.

### Como Criar uma Conta e Iniciar um Projeto na Posit Cloud

1. Acesse [posit.cloud](https://posit.cloud/) e clique em "Sign Up".
2. Selecione a opção de criar uma conta utilizando o GitHub.
3. Autorize a Posit Cloud a acessar sua conta GitHub.
4. Após criar sua conta, clique em "New Project" e selecione "New RStudio Project" para iniciar seu ambiente de desenvolvimento.

### Automação da Atualização de Dados

A atualização dos dados no aplicativo é realizada de maneira automática utilizando workflows do GitHub Actions. O arquivo YAML responsável pela automação está localizado na pasta `Workflows` dentro deste repositório.

## Relatórios e Dashboards

Os dashboards e relatórios foram escritos em **RMarkdown** e estão disponíveis dentro deste repositório. Eles podem ser executados localmente para gerar as visualizações conforme necessário.

## Acesso ao Aplicativo

O aplicativo está disponível publicamente e pode ser acessado no seguinte link:

- [Dashboards Contábeis das Empresas da B3](https://leovnoliveira.shinyapps.io/dashsdabolsa/)

## Contribuições

Contribuições para o desenvolvimento e aprimoramento deste aplicativo são bem-vindas. Sinta-se à vontade para abrir issues ou enviar pull requests.

## Como contribuir?

1. Faça um fork do projeto.
2. Realize o clone do projeto através do `git clone <link_do_fork_do_repositorio>`
3. Crie uma nova branch com as suas alterações: `git checkout -b <minha-branch>`
4. Salve as alterações e crie uma mensagem de commit contando o que você fez: `git commit -m "feature: <Minha contribuição">`
5. Envie as suas alterações: `git push origin <minha-branch>`

## Licença

Este projeto está licenciado sob a licença MIT - veja o arquivo [LICENSE](LICENSE) para mais detalhes.
