## Objetivo

```bash
Este repositório foi criado para o estudo de DevOps.
Ele utiliza as ferramentas mínimas necessárias para criação
de uma esteira de CI/CD.
```

## Informações

- O `jenkinsfile` utilizado está disponível na raíz do projeto.

## Resumo

    O Pipeline Script (jenkinsfile) realiza a instalação dos pacotes
    do projeto, executa os testes, formata o código, executa o lint,
    gera o build, executa o SonarQube Scanner afim de verificar
    problemas como code smells, vulnerabilidades e etc. Além disso,
    gera uma imagem docker com as tags latest e com o hash do
    último commit antes da execução do pipeline, envia as imagens
    para o dockerhub e por fim atualiza o arquivo deployment.yml
    alterando a imagem docker utilizada pelo kubernetes, essa última
    ação aciona o trigger do ArgoCD que verifica que tem alteração
    no repositório onde está o arquivo deployment.yml e cria um novo
    POD com a versão atualizada do código.

## Links de Ajuda

- https://grishabh1992.medium.com/jenkins-with-sonarqube-for-nodejs-582385f5f076

- https://stackoverflow.com/questions/51445846/elasticsearch-max-virtual-memory-areas-vm-max-map-count-65530-is-too-low-inc
