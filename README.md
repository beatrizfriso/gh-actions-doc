# Github Actions - Resumo 🚀 

Os arquivos de workflow usam a sintaxe YAML e esses workflows devem ficar armazenados em .github/workflows

- **name**: o nome do wokflow

- **run-name**: o GitHub mostra o nome da execução do workflow na aba "Actions" do repositório. Se for omitido ou for apenas um espaço em branco, o nome da execução será definido como informações específicas do evento para a execução do wokflow

   *exemplo*: 
```
run-name: Deploy to ${{ inputs.deploy_target }} by @${{ github.actor }}
```

- **on**: usado para definir quais eventos podem fazer com que esse workflow seja executado.
[Aqui nessa documentação do próprio github](https://docs.github.com/en/actions/writing-workflows/choosing-when-your-workflow-runs/events-that-trigger-workflows) temos uma lista de exemplos desses eventos

*usando um único evento*
```
on: push
```

*usando vários eventos*
```
on: [push, fork]
```

*usando vários tipos de atividade*
alguns eventos têm tipos de atividade que oferecem mais controle sobre quando o workflow deve ser executado. para isso, usamos o : on.<event_name>.types
