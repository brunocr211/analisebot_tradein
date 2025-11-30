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
export TELEGRAM_TOKEN=XXXXXXXXXXXXXXXXXXXXXXXXXXXX 
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

## Características

### Informações fundamentais

```
/i evx
```

```
#EVX
Tipo: TOKEN
Protocolo de consenso: POW
Algoritmo criptográfico: Ethash
Site: https://www.everex.io/
Redes sociais: 
https://t.me/everexio
https://www.facebook.com/everex.io
https://twitter.com/everexio
Exploradores: 
https://etherscan.io/token/0xf3db5fa2c66b7af3eb0c0b782510816cbe4813b8
Capitalização de mercado: $10.694.046
Preço atual: $0,473188
Preço de emissão: $0,880000
Data de emissão: 11/10/2017
Oferta máxima: -
Oferta total: 25.000.000
Oferta em circulação: 22.600.000
```

### Transações de curto prazo

```
/s tnt
```

```
#TNTBTC 92.966.054,00 (94,84%)
P: 0,00000730 V: 608,23 VWAP: 0,00000654
30 minutos: Compra 12,07 Venda 6,42
15 minutos: Compra 8,37 Venda 3,97
5 minutos: Compra 4,19 Venda 2,16
#TNTETH 5.059.783,00 (5,16%)
P: 0,00026182 V: 1.194,92 VWAP: 0,00023616
30 minutos: Compra 13,32 Venda 12,58
15 minutos: Compra 8,04 Venda 2,38
5 minutos: Compra 1,76 Venda 1,99
```

### Análise técnica

```
/x btc
```
