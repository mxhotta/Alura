# Buscador de Oportunidades de Emprego por Região e Área de Atuação

Este projeto consiste em um script Python que atua como um buscador de oportunidades de emprego, permitindo que usuários encontrem empresas que correspondam à sua região de interesse e área de atuação profissional. Ele utiliza agentes autônomos para realizar a busca e, posteriormente, auxilia na redação de e-mails de apresentação para as empresas selecionadas.

## Funcionalidades

1.  **Agente de Busca de Vagas (`ag_busca`)**:
    * Permite ao usuário especificar uma cidade e uma distância máxima para a busca de vagas.
    * O usuário também informa a área de atuação desejada (ex: indústria, tecnologia, comércio).
    * Utiliza o Google Maps para identificar empresas dentro da área e distância especificadas.
    * Prioriza empresas de maior porte.
    * Busca informações de contato, com preferência para e-mails de recrutamento, RH ou recursos humanos.
    * Retorna uma lista de até 5 empresas relevantes, ordenadas pela proximidade da cidade do usuário.
    * As informações retornadas para cada empresa incluem nome, cidade, área de atuação, e-mail de contato, telefone e site.

2.  **Agente Redator de E-mails (`ag_redator`)**:
    * Após a busca, o usuário pode selecionar até 3 empresas da lista para as quais deseja enviar um e-mail de apresentação.
    * O script coleta dados pessoais e profissionais do usuário (nome, idade, e-mail, telefone, escolaridade, formação, competências, vaga pretendida e um breve perfil).
    * Gera três e-mails distintos, um para cada empresa selecionada, utilizando um tom formal.
    * Cada e-mail inclui as informações do usuário e informa que o currículo está anexado.
    * Os e-mails são finalizados com os dados de contato do usuário.

3.  **Interface de Usuário Interativa**:
    * O script guia o usuário através de prompts no terminal para inserir os dados de busca (cidade, distância, área de atuação).
    * Exibe os resultados da busca de forma clara.
    * Solicita a seleção de empresas para contato.
    * Pede as informações pessoais e profissionais necessárias para a redação dos e-mails.
    * Apresenta os e-mails gerados ao final do processo.

## Como Utilizar

Para utilizar este buscador de oportunidades de emprego, siga os seguintes passos:

1.  **Clone ou faça o download deste repositório para o seu ambiente local.**
2.  **Certifique-se de ter um ambiente Python configurado.**
3.  **Instale as bibliotecas necessárias.** Embora o código fornecido não especifique as bibliotecas de agentes utilizadas, é provável que dependa de alguma biblioteca para a criação e interação com agentes de linguagem (como `langchain`, `autogen`, ou alguma outra). Consulte a documentação da biblioteca que você pretende usar e instale-a via pip:
    ```bash
    pip install nome_da_biblioteca
    ```
    Se o código utilizar a biblioteca `google-generativeai`, instale-a também:
    ```bash
    pip install google-generativeai
    ```
    E configure a chave da API conforme necessário.
4.  **Execute o script Python.** Navegue até o diretório onde o arquivo foi salvo e execute:
    ```bash
    python seu_arquivo_python.py
    ```
    (substitua `seu_arquivo_python.py` pelo nome do arquivo, caso seja diferente).
5.  **Siga as instruções no terminal.** O script irá solicitar as informações necessárias para a busca de vagas e, posteriormente, seus dados para a redação dos e-mails.
6.  **Visualize os resultados.** O script exibirá as empresas encontradas e os e-mails de apresentação gerados.

## Observações

* Este código depende de uma biblioteca de agentes para funcionar corretamente. O exemplo fornecido sugere uma estrutura com classes `Agent` e uma função `call_agent`, mas a implementação real pode variar dependendo da biblioteca escolhida.
* A eficácia da busca de empresas e a qualidade dos e-mails gerados podem depender da capacidade do modelo de linguagem subjacente e da precisão das informações encontradas através do Google Maps.
* Para utilizar modelos de linguagem como o Gemini, pode ser necessário configurar chaves de API e seguir as diretrizes de uso da respectiva plataforma.

Este projeto visa simplificar o processo de busca de emprego, conectando candidatos a potenciais empregadores de forma direcionada e auxiliando na comunicação inicial.
