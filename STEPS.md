## Github Actions
<i>API de causa e efeito</i>. <b>Gatilho -> workflow (job [action, action])</b>

Ex: 
* Gatilho > push branch dev
* Workflow > test and deploy
    * job test
        * yarn install
        * yarn test
    * job build & deploy
        * yarn install
        * yarn build
        * deploy dev

## Steps
1. Criar .github/workflows
2. Criar workflow pull_request.yml para rodar testes ao abrir um PR.
3. Criar workflow dev.yml para rodar testes, build e deploy ao realizar um push.
    - Configurar variáveis de ambiente no Github Secrets.
4. Criar workflow main.yml, semelhante ao anterior, para deploy no ambiente de prod.