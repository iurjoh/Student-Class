# Student class

Classe Python com testes de propriedades, mudanças de estado, datas e respostas HTTP simuladas.

[English](README.md)

## Registro do processo

Código revisado em 01/10/2026. O repositório registra um exercício, não um produto publicado. Não foram encontrados planejamento datado, pesquisa com usuários ou wireframes nos arquivos revisados. A arquitetura abaixo descreve o código existente, sem inventar um diário de desenvolvimento.

## Ideia, arquitetura e design

`student.py` define Student com nome/sobrenome, data inicial de hoje, término 365 dias depois e indicador de lista de travessuras. Propriedades geram nome completo e email demonstrativo. Métodos ativam o indicador, estendem o término e buscam uma agenda por requests. `test_students.py` contém hooks de preparação/limpeza e seis métodos de teste. Não há banco ou interface.

## Execução e testes

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install requests
python3 -m unittest -v test_students
```

Não há requirements no diretório raiz revisado; student.py importa `requests`. Testes cobrem nome completo, email, indicador, extensão de prazo, sucesso e falha HTTP. Os dois testes HTTP simulam `student.requests.get`, sem precisar de serviço real. Não executados nesta atualização; nenhum resultado ou cobertura é afirmado.

## Privacidade, limites e próximos testes

A URL de agenda inclui nome/sobrenome em `company.com`; é demonstrativa, não integração verificada. Não a consulte com dados pessoais reais. A requisição não tem timeout ou tratamento de exceções. Revise timeout, falhas de rede, codificação de nomes, limites de datas e extensões inválidas antes de reutilizar. Emails gerados são exemplos, não contatos verificados. Não é um produto publicado de gestão estudantil.

## Capturas

Não há interface de aplicação para capturar. Nenhuma imagem foi adicionada. Se evidência de terminal for útil, salve captura datada do comando e resultado real em `docs/assets/`, sem caminhos ou dados privados. Não invente dashboard ou resultado de testes.

## Créditos e licença

Baseado no [template Gitpod completo do Code Institute](https://github.com/Code-Institute-Org/gitpod-full-template). Direitos de curso/template de terceiros preservados, sem licença nova. O README original está no [apêndice histórico em inglês](README.md#original-template-readme-historical), não como recomendação atual de configuração.
