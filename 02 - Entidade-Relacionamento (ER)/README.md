# 2. Entidade-Relacionamento (ER)

A abordagem mais amplamente utilizada para modelagem de dados é a técnica de entidade-relacionamento (ER). Nessa técnica, o modelo de dados é representado por um modelo entidade-relacionamento (ER), que geralmente é ilustrado por meio de um diagrama de entidade-relacionamento (DER).

## 2.1. Entidade

Em um modelo entidade-relacionamento (ER), uma entidade representa um conjunto de objetos ou elementos da realidade que possuem características em comum e que são relevantes para o sistema de informação que está sendo modelado. O foco é apenas nos objetos que precisam ser representados no banco de dados, ou seja, aqueles que possuem informações importantes para o contexto da aplicação.

Em um DER, uma entidade é representada por um retângulo que contém seu nome, conforme ilustrado na figura 2.1.

<div align="center">
    <img src="../imgs/representacao_grafica_entidades.png" width="50%"/>
    <p>Figura 2.1: Representação gráfica de entidades.</p>
</div>

No exemplo, o primeiro retângulo representa o conjunto de todas as pessoas sobre as quais se deseja armazenar informações no banco de dados, enquanto o segundo retângulo corresponde ao conjunto de todos os departamentos sobre os quais se deseja manter informações

## 2.2. Relacionamento

Os relacionamentos entre entidades em um banco de dados refletem as associações e interações lógicas entre diferentes entidades. Eles são estabelecidos para modelar as conexões que existem no mundo real, garantindo a integridade e a consistência dos dados armazenados.

Em um Diagrama Entidade-Relacionamento (DER), os relacionamentos são representados por losangos conectados por linhas aos retângulos que simbolizam as entidades envolvidas. A Figura 2.2 ilustra um DER com duas entidades, Pessoa e Departamento, e um relacionamento denominado Lotação.

<div align="center">
    <img src="../imgs/representacao_grafica_relacionamento.png" width="50%"/>
    <p>Figura 2.2: Representação gráfica de relacionamento.</p>
</div>

No exemplo, o relacionamento Lotação representa uma associação específica, formada por uma associação entre uma instância da entidade Pessoa e uma instância da entidade Departamento.