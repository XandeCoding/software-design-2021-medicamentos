# Design de Software

## Requisitos

_Cada município oferece um conjunto específico de medicamentos, disponíveis em pontos geográficos distintos e em quantidades específicas. Profissionais de saúde, muitas vezes, desconhecem os medicamentos oferecidos, ou aqueles alternativos oferecidos, ou aqueles disponíveis apenas em casos de saúde específicos (e não em outros), além dos pontos onde podem ser obtidos. Naturalmente, o indivíduo também não sabe onde obter um medicamento de sua necessidade. A intenção é oferecer um sistema escalável, configurável por município de tal forma que os medicamentos e as informações pertinentes, assim como a disponibilidade deles (estoque) possa ser consultada tanto pela população quanto por sistemas de informação em saúde._

## Solução [WIP]

A ideia seria ter uma plataforma web onde cada ponto de distribuição (seja farmácia ou hospital etc) teria informações
como endereço, nome, horário de funcionamento, e os remédios disponíveis em seu estoque e mostrando as restrições para o usuário como documentos que seriam necessários para buscar a medicação referida (identidade, receita médica etc…).

O gerenciamento dos produtos seria em cargo de um administrador cadastrado na nossa aplicação.
Feito o cadastro, o ponto deve cadastrar seus remédios disponíveis, isso via API fornecida por nós ou manualmente caso se encontre necessário e também sendo possível realizar uma integração com o sistema interno da farmácia.

### Possíveis funcionalidades

- Pesquisar remédio por cidade
- Pesquisar remédio por estado
- Pesquisar remédio por localização atual (tendo um range de área pré-definido
- Cliente pode pedir sugestão a um admin para adicionar, editar ou remover um medicamento

### Perguntas

- O que seriam casos de saúde específicos, seriam casos onde, por exemplo uma pessoa com pressão alta consegue remédios grátis em farmácias e postos de saúde? - **Lista de exigências em geral para adquirir o remédio.**

- Daria para pesquisar somente o nome do remédio ou o ponto e ver onde teria o remédio e os disponíveis no estabelecimento de saúde - **Buscar por ambos e usar outros parametros de busca (como lista de exigencias)**

- A questão de escabilidade seria em relação as cidades e estados aderirem o sistema ou sobre perfomance, resiliência da aplicação em si ou ambos?

- Como seria o cadastro para realizar a autenticação? - **Só dos administradores ou Responsável Técnico com nosso sistema**

- Ver se o sistema interno dos pontos são iguais ou padronizados. Visto isso, não seria preciso ter uma lista de remédios pré-cadastrada, e sim utilizaria apenas uma integração com o sistema interno - **Nosso sistema API vai ser possível de integração com outros sistemas cliente**

- A integração com nosso sistema seria obrigatória ou só opcional?
