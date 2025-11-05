# Indigenous and Slavery Project
 
Sequência dos scripts:
* Rodar o notebook data_unifier.ipynb
* Criar um base no Stardog chamada "IndigenousSlavery"
* Usar a ontologia Ontology/IndigenousSlaveryOnto.ttl como modelo para a base "IndigenousSlavery"
* Rodar o notebook graph-population.ipynb
* Rodar o notebook NER.ipynb
* A Ontologia "IndigenousSlaveryOnto.ttl" povoada pelos notebooks "graph-population.ipynb" e "NER.ipynb" está salva como "2025_05_09_IndigenousSlavery_onto_povoada_NER.ttl".

(O ideal seria utilizer apenas uma base de dados para o grafo de conhecimento. No entanto, como um dos propósitos desse projeto foi ganhar experiência com diversas tecnologias, utilizamos Stardog para a modelagem da ontologia e seu povoamento com os dados da BDTD e o Neo4j para povoar o conteúdo das teses e implementar o GRaphRAG)
* Importar ontologia para o Neo4j usando o Neosemantics toolkit
* Web crawler para buscar os arquivos PDF em cada biblioteca, cada universidade possui um notebook similar mas com pequenas adaptacões demandadas por cada repositório institucional (em data/crawler_bibliotecas)
* Os web crawlers fazem o download de cada arquivo PDF do repositório da universidade, extraem o texto de cada página, identificam as entidades pessoas e local, e carrega toda informacão extraída no NEO4J.
* Rodar o notebook Embeddings.ipynb para gerar em uma representacão vetorial para cada página e para o abstract de cada tese e dssertacão.
* Usar o notebook EDA.ipynb para realizar uma análise de dados exploratória. Essas análises servem de guia para a lompezas e preprocessamentos implementados no Notebook graph_cleaning.ipynb.