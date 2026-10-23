# Relatório — Elas Empreendem

## Viabilidade

- Grupo: Dupla 09
- Integrantes: Ana Fabia da Silva. A pasta registra só esse nome. A constitution fala em dois integrantes, e o repositório só tem a conta Fabiasilva19 além do instrutor.
- Repositório: https://github.com/Fabiasilva19/projeto_elasEmpreendem
- Constitution: https://github.com/Fabiasilva19/projeto_elasEmpreendem/blob/2a2f41063ba5278974e703e03d67089261623fb1/Constitution
- Stack: não declarada
- Veredito: Viável com recorte

O problema cabe na disciplina se o produto for um anúncio revisável: a profissional publica um serviço, com categoria, cidade e descrição, e outra pessoa encontra esse anúncio. Dois logins, pagamento, chat, mapa e checagem de antecedentes não cabem nesta etapa.

## SWOT

### Forças

Usuária e resultado estão no README em um parágrafo só. A constitution está no repositório, no commit citado no formulário, e separa sugestão de código do que mexe em requisito, banco e segurança. A regra de dado pessoal cabe num produto com login de usuárias.

### Fraquezas

Não há stack, modelo, formato da resposta nem critério de pronto verificável. “Testada por pessoas reais” não diz quem testa, em qual fluxo nem o que conta como falha.

### Oportunidades

Spec com um anúncio de exemplo e três saídas testáveis: categoria, cidade e descrição. O agente redige a descrição a partir desses campos e não inventa preço, horário nem contato. Pagamento, chat e o login do cliente ficam para depois.

### Ameaças

Anúncio de babá com endereço ou dado de criança tratado como texto livre. Dado pessoal de usuária em prompt. Marketplace com pagamento antes de existir um anúncio que se publica e se encontra. Regra de merge que exige uma segunda pessoa que não está no repositório.

## Stack técnica

**Parecer: Não declarada.** O README e a constitution não nomeiam linguagem, framework, banco nem modelo.

Para a primeira spec, uma aplicação web em uma linguagem basta: o formulário do anúncio, a lista por categoria e cidade, e uma chamada de modelo com saída em JSON para a descrição. SQLite guarda o anúncio. A chave fica em variável de ambiente no servidor. Pagamento, chat e aplicativo nativo não entram agora. TypeScript num único projeto, ou Python com uma página simples, servem. O que não serve é abrir os dois antes de um anúncio passar nos três campos.

## Recomendação

**Especifiquem um anúncio de serviço, com categoria, cidade e descrição revisável, e deixem pagamento, chat e o login do cliente para depois.**

Elas Empreendem está alinhado com a disciplina se o produto for a publicação de um serviço, não um marketplace completo. A profissional informa categoria, cidade e um texto curto. O agente devolve a descrição e mostra o que veio do texto dela. Se faltar cidade ou categoria, o sistema pede o campo, em vez de completar com conhecimento geral. Preço, telefone, endereço e dado de criança não entram no prompt nem no repositório. O critério de pronto desta etapa é objetivo: o anúncio aparece na lista daquela categoria e daquela cidade, e a descrição não contém dado que não estava no formulário. A constitution precisa nomear o segundo integrante e incluí-lo no repositório, ou passar a valer para uma pessoa só. O arquivo Constitution no commit 2a2f410 já é a evidência da semana 2. O que falta no mesmo repositório é a spec desse anúncio.
