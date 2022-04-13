Bootcamp IGTI: Engenheiro(a) de Dados Cloud

Desafio

Módulo 3 Desenho de Arquiteturas de Dados Escaláveis

Objetivos
Exercitar os seguintes conceitos trabalhados no Módulo:
✓ Kubernetes.
✓ Pipelines de Dados.
✓ Orquestração.
✓ Processamento de Big Data.

Enunciado
Você é Engenheiro(a) de Dados em uma consultoria de soluções educacionais EDCenter,
na área de Filosofia. A EDCenter está expandindo seu negócio para outras áreas do
Brasil. A fonte de dados mais atualizada para entender o cenário atual da educação
superior em Filosofia no Brasil é o Enade 2017.
Você deve fazer a ingestão dos microdados do Enade 2017 em uma estrutura de Data
Lake na AWS (ou em outro provedor de sua escolha). Depois disso, você deve utilizar o
Spark Operator para, dentro do Kubernetes, converter os dados para o formato parquet
e escrever os resultados em uma outra camada do Data Lake. Em seguida, disponibilize
os dados para consulta no AWS Athena (ou outra engine de Data Lake de outra nuvem
ou no BigQuery, no caso do Google Cloud) e faça uma consulta para demonstrar a
disponibilidade dos dados. Por fim, utilize a ferramenta de Big Data ou a engine de Data
Lake para realizar investigações nos dados e responder às perguntas do desafio.
Atenção! Todo o processamento de dados e transformações, bem como a extração
dos microdados e ingestão devem ser realizados no Kubernetes. Fique à vontade para
escolher a melhor forma de implementar os processos (manifestos, argo CD, Airflow
etc.).

DIVIRTA-SE!

Atividades

Os alunos deverão desempenhar as seguintes atividades:

1. Criar um cluster Kubernetes para a realização das atividades (local ou baseado
   em nuvem). Recomendamos utilizar um cluster baseado em nuvem para
   comportar o volume de dados trabalhado.
2. Realizar a instalação e configuração do Spark Operator conforme as instruções
   das aulas.
3. Realizar a instalação e configuração de outas ferramentas que se deseje utilizar
   (Airflow, Argo CD etc.).
4. Realizar a ingestão dos dados do Enade 2017 no AWS S3 ou outro storage de
   nuvem de sua escolha. Dados disponíveis em: https://www.gov.br/inep/pt-br/acesso-a-informacao/dados-abertos/microdados/enade. Os dados devem
   ser ingeridos de maneira automatizada na zona raw, zona crua ou zona bronze
   do seu Data Lake.
5. Utilizar o SparkOperator no Kubernetes para transformar os dados no formato
   parquet e escrevê-los na zona staging ou zona silver do seu data lake.
6. Fazer a integração com alguma engine de data lake. No caso da AWS, você deve
   a. Configurar um Crawler para a pasta onde os arquivos na staging estão
   depositados.
   b. Validar a disponibilização no Athena.
7. Caso deseje utilizar o Google, disponibilize os dados para consulta usando o Big
   Query. Caso utilize outra nuvem, a escolha da engine de Data Lake é livre.
8. Use a ferramenta de Big Data ou a engine de Data Lake (ou o BigQuery, se
   escolher trabalhar com Google Cloud) para investigar os dados e responder às
   perguntas do desafio.
9. Quando o desenho da arquitetura estiver pronto, crie um repositório no Github
   (ou Gitlab, ou Bitbucket, ou outro de sua escolha) e coloque os códigos de
   processos Python e implantação da estrutura Kubernetes
