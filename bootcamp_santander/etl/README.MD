# Pipeline ETL com Python

O processo de ETL é dividido em três etapas:

## Extração

A primeira etapa é extrair os dados dos clientes. No caso deste exemplo, os dados são extraídos de um arquivo CSV chamado SDW2023.csv. O arquivo contém uma lista de IDs de usuário do Santander.

A primeira linha de código importa o módulo pandas para trabalhar com dados em formato CSV. A segunda linha lê o arquivo CSV e armazena os dados em um objeto DataFrame. A terceira linha extrai a lista de IDs de usuário do DataFrame.

## Transformação

A segunda etapa é transformar os dados extraídos. No caso deste exemplo, os dados são transformados para incluir uma mensagem de marketing personalizada para cada usuário. A mensagem de marketing é gerada usando a API do OpenAI GPT-4.

A primeira linha de código importa o módulo requests para fazer requisições HTTP. A segunda linha importa o módulo json para trabalhar com dados JSON. A terceira linha define uma função chamada get_user() que faz uma requisição GET para a API do Santander para obter os dados de um usuário.

A quarta linha define uma variável chamada users que armazena uma lista de objetos dict que representam os dados dos usuários. A quinta linha itera sobre a lista de IDs de usuário e usa a função get_user() para obter os dados de cada usuário.

A sexta linha define uma função chamada generate_ai_news() que usa a API do OpenAI GPT-4 para gerar uma mensagem de marketing personalizada para um usuário. A sétima linha itera sobre a lista de usuários e usa a função generate_ai_news() para gerar uma mensagem de marketing personalizada para cada usuário.

A oitava linha adiciona a mensagem de marketing personalizada à lista de "news" de cada usuário.


## Carga

A terceira etapa é carregar os dados transformados de volta para a API. No caso deste exemplo, os dados são carregados usando o endpoint PUT https://sdw-2023-prd.up.railway.app/users/{id}.

A primeira linha define uma função chamada update_user() que faz uma requisição PUT para a API do Santander para atualizar os dados de um usuário.

A segunda linha itera sobre a lista de usuários e usa a função update_user() para atualizar os dados de cada usuário.

A terceira linha imprime uma mensagem para indicar se a atualização dos dados do usuário foi bem-sucedida.

[Acesso o código ETL aqui](/bootcamp_santander/etl/SantanderDevWeek2023.ipynb)
