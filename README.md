# Meu resumo do Curso Git flow na prática da School of Net 

O Git flow é uma extensão do git.
É possível usar os dois ao mesmo tempo.
Semântica aos branches *master* e *develop*

O master é um repositório onde é feito merge, quase nunca commits.
O develop é o repositório para o desenvolvimento, dele vem o merge para o master.

Ele trabalha com:
* FEATURES
* RELEASES 
* HOTFIXES
* BUGFIXES
* SUPPORTS

# Criando repositório com Git flow

* git flow init

# Criando features

Define uma nova funcionalidade.
Toda feature inicia e termina em develop.
Toda feature tem o prefixo padrão FEATURE/\*. Exemplo: FEATURE/loja, FEATURE/cadastro, FEATURE/login.

* git flow feature start <nome-feature>

Após o git commit
* git flow finish <nome-feature>

Após finalizar uma feature, é realizado um merge em develop e a featre é excluída.

Caso queria compartilhar a feature com outras pessoas, antes de finalizar a feature
* git flow publih <nome-feature>

# Administrando features

Para obter uma feature publicada.
* git flow feature track <nome-feature>

Listar apenas features,
* git flow feature list

Troca entre features
* git flow feature checkout <nome-feature>

Por padrão o git flow trabalha com origin.

# Criando releases

Definir uma nova versão em produção do software.
Prefixo padrão RELEASE/\*. Exemplo: REALEASE/rls1, RELEASE/v2, etc..

A releasse é mesclada no master e no develop
As releases trabalham com o padrão Semantic Versioning
vMAJOR.MINOR.PATCH.

* git flow release start <versao>: Onde versão segue o padrão Semantic Versining: 0.0.1, 0.0.2, 0.1.0, 1.0.0

