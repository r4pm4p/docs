# Concepção de DDD e estruturação de pasta/projeto

### Entidades

    São classes que possuem signifaco para o dominio e podem ser identifacadas por um ID
    Ex: Usuairo, Administrador e Batalha

### Objetos de Valor

    Objetos que só carregam valores, mas que não possuem distinção de identidade para o negocio.
    Ex: Endereço.
    Pensando em endereço como um campo de uma entidade, como por exemplo campo da entidade Batalha.

### Agregados

    Seriam as consolidações do modelo, onde são de fato realizados as uniões de Entidades e Objetos de valor.
    Ex: BatalhaAgregate, onde se tem um modelo de batalha e de Endereco, para posteriormente serem persistidos

### Factorys

    Seriam as responsáveis pela criação de Agregados e Objetos de valores
    Ex: BatalhaFactory

### Serviços

    Classes que contem Regras de negocios, mas que não pertencem a nenhuma entidaade ou agregado
    Ex: ParticiparBatalhaService
    Seria a classe que define as regras de quem pode solicitar participar na batalha, como por exemplo somente um mc.

### Repositorios

    Classes que persistem os dados no banco de dados, controlando toda a dinamica presente nos modos de persistencia




## Pensando em estruturas de pastas, teriamos:

    nome_projeto
        .../
        src/
            application/
                Routes/
                    Routes.ts
                Controllers/
                    BatalhaController.ts
                Request/
                    ParticiparBatalhaRequest.ts
                Services/
                    ParticiparBatalhaService.ts
                ....
    
            domain/
                Rules/
                    ParticiparBatalhaRule.ts
                Repository/
                    BatalhaRepository.ts
                Entities/
                    Batalha.ts
                ValueObjects/
                    Endereco.ts
                Aggregates/
                    BatalhaAggregate.ts
                Interfaces/
                    --- caso necessário --- 
                Facades/
                    --- caso necessário --- 
                ....

            infrastructure/
                Database/
                    Connection.ts
                Repository/
                    BatalhaRepositoryImplementation.ts
                DTO/
                    BatalhaDTO.ts
                Interfaces/
                    --- caso necessário ---             
                ....




















