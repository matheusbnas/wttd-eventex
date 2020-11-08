README.md
#Eventex

Sistema de Eventos emcomendado pela Morena.

Build Status Code Health

Como desenvolver?
Clone o repositório.
Crie um virtualenv com o Python 3.5
Ative o virtualenv
Instale as dependências
Configure a instância com o .env
Execute os testes.
git clone git@github.com:ritomar/wttd-eventex.git wttd
cd wttd
python -m venv .wttd
source .wttd/bin/activate
pip install -r requirements-dev.txt
cp contrib/env-sample .env
python manage.py test
Como fazer o deploy?
Crie uma instância no heroku.
Envie as configurações para o heroku.
Defina uma SECRET_KEY segura para a instância.
Defina DEBUG=False
Configura o serviço de e-mail.
Envie o código para o heroku.
heroku create minhainstancia
heroku config:push
heroku config:set SECRET_KEY=`python contrib/secret_gen.py`
heroku config:set DEBUG=False
# configure o e-mail
git push heroku master --force
