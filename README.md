# Bot de Análise de Negociação

O **Bot de Análise de Negociação** é um chatbot do Telegram para análises baseadas em dados do mercado de criptomoedas, particularmente da bolsa Binance. Ele fornece indicadores técnicos padrão, sentimento social e atividades de desenvolvedores. Índices de mercado, classificações e métricas estatísticas baseadas em transações on-chain em diferentes redes blockchain também são relatados.

## Executar em máquina local

```
pip install -r requirements.txt
```

```
# Para Windows
set TELEGRAM_TOKEN=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX 
set SECRET_KEY=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX 
set API_KEY=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
definir DB_NAME=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
definir DB_USERNAME=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
definir DB_HOST=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
definir DB_PASSWORD=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
definir ADMIN_ID=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
definir ADMIN_USERNAME=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
python bot.py
```

```
# Para Linux
export TELEGRAM_TOKEN=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX 
export SECRET_KEY=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX 
export API_KEY=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
export DB_NAME=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
export DB_USERNAME=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
export DB_HOST=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
export DB_PASSWORD=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
export ADMIN_ID=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
export ADMIN_USERNAME=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
python bot.py
```

## Implantação na plataforma Heroku

```
heroku create trading-analysis-bot --buildpack heroku/python
heroku buildpacks:add --index 2 https://github.com/numrut/heroku-buildpack-python-talib
heroku config:set TELEGRAM_TOKEN=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
heroku config:set SECRET_KEY=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
heroku config:set API_KEY=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
heroku config:set DB_NAME=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
heroku config:set DB_USERNAME=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
heroku config:set DB_HOST=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
heroku config:set DB_PASSWORD=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
heroku config:definir ADMIN_ID=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
heroku config:definir ADMIN_USERNAME=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
git push heroku master
heroku ps:scale bot=1 

