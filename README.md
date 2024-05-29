# UM ADENDO
## Por Pedro Antonio
* Por Alguma razão quando tentei rodar a API. Meu dotnet não abria e levava ao seguinte erro:
  ## MSBUILD : error MSB1011: Especifique o arquivo de solução ou de projeto a usar porque esta pasta contém mais de um arquivo de solução ou de projeto.

* Eu tentei pesquisar por algumas soluções no StackOverFlow e até encontrei uma [Issue](https://github.com/dotnet/sdk/issues/33674) no github onde várias pessoas estão relatando sobre esse erro.
* A conclusão é que este erro ocorre porque tem mais de um arquivo .csproj/.sln dentro do projeto/diretório, e por isso causa conflito.
* Além disso o erro pode ser por supostamente no VSCODE ao instalar a extensão do VSCODE de C# ele automaticamente adiciona um arquivo.sln no projeto (razão pela qual causa o conflito na minha API).
* Eu não consegui achar no entanto nenhum arquivo .sln/.csproj adicional nas pastas/diretorio do projeto. Portanto não tenho 100% de certeza se a API está funcional ou não. No entanto.
* Eu GARANTO que fiz este projeto com base nos projetos passados e nas vídeos aulas que vi na DIO. segui passo a passo e COMPREENDI o funcionamento/desenvolvimento de uma API em dotnet.














# DIO - Trilha .NET - API e Entity Framework
www.dio.me

## Desafio de projeto
Para este desafio, você precisará usar seus conhecimentos adquiridos no módulo de API e Entity Framework, da trilha .NET da DIO.

## Contexto
Você precisa construir um sistema gerenciador de tarefas, onde você poderá cadastrar uma lista de tarefas que permitirá organizar melhor a sua rotina.

Essa lista de tarefas precisa ter um CRUD, ou seja, deverá permitir a você obter os registros, criar, salvar e deletar esses registros.

A sua aplicação deverá ser do tipo Web API ou MVC, fique a vontade para implementar a solução que achar mais adequado.

A sua classe principal, a classe de tarefa, deve ser a seguinte:

![Diagrama da classe Tarefa](diagrama.png)

Não se esqueça de gerar a sua migration para atualização no banco de dados.

## Métodos esperados
É esperado que você crie o seus métodos conforme a seguir:


**Swagger**


![Métodos Swagger](swagger.png)


**Endpoints**


| Verbo  | Endpoint                | Parâmetro | Body          |
|--------|-------------------------|-----------|---------------|
| GET    | /Tarefa/{id}            | id        | N/A           |
| PUT    | /Tarefa/{id}            | id        | Schema Tarefa |
| DELETE | /Tarefa/{id}            | id        | N/A           |
| GET    | /Tarefa/ObterTodos      | N/A       | N/A           |
| GET    | /Tarefa/ObterPorTitulo  | titulo    | N/A           |
| GET    | /Tarefa/ObterPorData    | data      | N/A           |
| GET    | /Tarefa/ObterPorStatus  | status    | N/A           |
| POST   | /Tarefa                 | N/A       | Schema Tarefa |

Esse é o schema (model) de Tarefa, utilizado para passar para os métodos que exigirem

```json
{
  "id": 0,
  "titulo": "string",
  "descricao": "string",
  "data": "2022-06-08T01:31:07.056Z",
  "status": "Pendente"
}
```


## Solução
O código está pela metade, e você deverá dar continuidade obedecendo as regras descritas acima, para que no final, tenhamos um programa funcional. Procure pela palavra comentada "TODO" no código, em seguida, implemente conforme as regras acima.
