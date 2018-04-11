
# O Desafio

Queremos calcular o tempo médio de nossos deployments. Para tal, queremos implementar uma API REST que deve ser chamada no início e fim de cada deploy.

A API deve suportar uma chamada store que receba os seguintes parâmetros: nome do componente que estamos fazendo deploy, se é um início ou fim de deploy e, caso seja um fim, o status (sucesso ou algum código de erro). 

Para este teste, como requerimento mínimo, implemente a chamada store. Grave os parâmetros passados na chamada (junto com o timestamp) em um arquivo CSV persistentemente. Use a linguagem e servidor web de sua preferência, mas precisa ser em LInux e usando docker.

## Opcionais

Opcionalmente, faça o maior número possível dos itens abaixo:

  * Em vez de salvar os dados em um arquivo CSV, salve os dados em um banco de dados sql (Postgresql ou MySQL)
  * Descreva possíveis melhorias para a API. Se possível, implemente-as.
  * Escreva arquivos `docker-compose.yml` para instanciar os containers.
  * Escreva arquivos de configuração para fazer o deploy desses servidores (assuma o uso de duas máquinas, uma para web e outro para o banco). A ferramenta de gerenciamento de configuração que sua preferimos é o Ansible, mas se não a conhecer, use uma outra com a qual se sinta confortável (Salt, Chef, Puppet etc)
  * Escreva arquivos de configuração para fazer deploy em Kubernetes.
  * Faça um script que crie uma instância EC2 (pode ser spot) e que execute um script `xyz.sh` em sua inicialização. Pra simplificação, assuma que `xyz.sh` só faça um sleep de 60s. Ao fim do término de `xyz.sh`, a instância deve ser encerrada.

Note que a descrição não é complementamente detalhada de forma intencional. Você está livre para fazer suposições (contanto que as descreva claramente) e faça suas próprias melhorias que achar que possam fazer sentido.

## Esperemos que entregue:

  * Todo o código fonte, arquivos de configuração etc em um repositório no github
  * Queremos que faça seus commits normalmente. Não faça checkin apenas do resultado final, queremos ver o histórico de commits para entender como a solução foi evoluída
  * Um README contendo instruções de como rodar sua API, assim como exemplos de comando curl para testar a API. Use o arquivo também para descrever possíveis condições que tenha assumido além de informações que nos ajudem a entender o quê e como feito.


## O que levaremos em consideração
  * Corretude, robustez. Faça com qualidade. Prefira fazer menos coisas e com qualidade do que mais coisas e de forma questionável.
  * Simplicidade e legibilidade do código e da solução como um todo
  * Possíveis melhorias em cima daquilo que foi proposto
