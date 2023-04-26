# Intro

Olá esse é um repositório de estudos de como configurar e usar variáveis de ambiente via github action.
Um dos objetivos apoiar membros do curso a construirem seus próprios scripts

## Estrutura do projeto

Existe apenas um arquivo `blank.yml` dentro dele existem a configuração de dois work flows veja a imagem abaixo 👇
![image](https://user-images.githubusercontent.com/41530127/234443734-66e04532-7a0f-400c-9b5b-93a915c3a789.png)

### Apenas dois jobs 

### local-variable-and-repository-variable
Nesse job temos a declaração e consumo de valores..."locais" diretamente do arquivo `.yaml` repare que nesse cenário usamos
a notação de `${{env.variable}}`.

![image](https://user-images.githubusercontent.com/41530127/234446276-a9b29b87-eb94-4ce5-8b28-7699d8d7eaf8.png)

As variáveis de repositório foram configuradas exatamete como a doc oficial [link](https://docs.github.com/en/actions/learn-github-actions/variables#creating-configuration-variables-for-a-repository)
para acessa-las usamos o `${{ vars.repo-variables }}`
![image](https://user-images.githubusercontent.com/41530127/234446657-3869f412-0192-40a1-8c6a-5dadfdff7b72.png)
![image](https://user-images.githubusercontent.com/41530127/234446728-9b7c42e7-7b31-44a6-bab3-c8c7d0b60647.png)

### using-environments
Nesse job nós usamos os environments do github exatamente como a doc sugere [link](https://docs.github.com/en/actions/learn-github-actions/variables#creating-configuration-variables-for-an-environment).
Para acessa-las usamos a `vars` como no highlight abaixo. **Não** podemos nos esqueçer de definir nossa environment.

![image](https://user-images.githubusercontent.com/41530127/234447543-06c23644-f349-48be-bef4-b0af899e5c5c.png)

👇 Abaixo temos a config da nossa environments 👇
![image](https://user-images.githubusercontent.com/41530127/234448015-fca135b7-bcfd-4877-b3a6-aa5c4bbea90f.png)


## Fontes de estudo

[Doc oficial sobre variables gihutb & github_Action](https://docs.github.com/en/actions/learn-github-actions/variables)

[GitHub Actions - Configuration Variables](https://www.youtube.com/watch?v=cPMJpKNqZb8&ab_channel=MickeyGousset)

[Set environment variables](https://www.youtube.com/watch?v=hAAAQL03f9E&ab_channel=KahanDataSolutions)
