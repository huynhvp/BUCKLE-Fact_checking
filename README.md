# Benchmark Fact-Checking
This benchmark continues our previous work **[P. Huynh, P. Papotti, 2017](http://www.eurecom.fr/fr/publication/5468/download/data-publi-5468.pdf)** on fact checking by providing the first comprehensive and publicly available infrastructure for evaluating fact checking methods across a wide range of assumption about the facts and the reference information.

It is an additional material of the publication "A Benchmark for Fact Checking Algorithms Built on Knowledge Bases", from **[P. Huynh, P. Papotti](http://www.eurecom.fr/en/publication/5996/download/data-publi-5996.pdf)**, accepted to International Conference on Information and Knowledge Management (CIKM), 2019

## Download & Install
1. The benchmark server is written by **[Nodejs](https://nodejs.org/en/download/)**. Follow `package.json` to install dependencies.
2. For the Knowlegde graph, we employ the DBPedia repository from `KGMiner [2]`, including enties, predicates and facts in the form of triples. 
   * Download: https://www.dropbox.com/s/yqlom6t5ehze0uq/data.zip?dl=1
   * Extract the zip file and place the files `node_dict.tsv`, `edge_dict.tsv` in folder `../data/dbpedia/graphs/` and file `edges.tsv` in folder `../data/dbpedia/graphs/graph_chi/` 
      * node_dict.tsv: contains entities and corresponding indices. Ex: Paris 12345, France 25672
      * edge_dict.tsv: contains predicates. Ex: capital 100
      * edges.tsv: contains fact triples in the form of (s, o, p). Ex: 12345 25672 100 represents for (Paris, France, capital)
   * To load the graph server: please navigate to KG-Miner folder and run ./run_server.sh
      
3. Follow base folders for downloading and installing benchmarking systems: `Knowledge Linker (KL) [1]`, `Discriminative Predicate Path (KGMiner) [2]`, `Subgraph Feature Extraction (SFE) [3]`, `Parallel Graph Embedding (Para_GraphE) [4]`, `Rule Discover [5]` 
   
   Each system has some modifications from the original version, according to the experiments considered in this work.
   
## References:
1. https://github.com/glciampaglia/knowledge_linker
2. https://github.com/nddsg/KGMiner
3. https://github.com/matt-gardner/pra
4. https://github.com/LIBBLE/LIBBLE-MultiThread/tree/master/ParaGraphE
5. https://github.com/stefano-ortona/rudik







