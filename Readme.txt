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
* Web crawley para buscar os arquivos PDF em cada biblioteca
