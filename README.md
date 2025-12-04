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
![x.png](img/x.png)

### Estatísticas de movimento do mercado

```
/m
```

```
#MERCADO
USDⓈ: 20 (+) 113 (-)
ALTS: 43 (+) 89 (-)
BNB: 63 (+) 30 (-)
BTC: 120 (+) 31 (-)
Terça-feira, 2 de julho, 13:48:21, 2019
```

### Fluxos monetários do mercado de altcoins

```
/e
```
![market.png](img/market.png)

### Fluxos de câmbio na cadeia

```
/b
```

```
*Fluxos diários de câmbio de BTC*
#Binance: $75 milhões em | $68 milhões fora
#Bitmex: $18 milhões em | $7 milhões fora
#Bitfinex: $6 milhões em | $8 milhões fora
#Bitstamp: $18 milhões em | $22 milhões fora
#Bittrex: $2 milhões em | $4 milhões fora
#Poloniex: $1 milhão em | $2 milhões fora

*Fluxos diários de câmbio ETH*
#Binance: $24 milhões em | $12 milhões fora
#Bitfinex: $2 milhões em | $1 milhão fora
#Bittrex: $240 mil em | $415 mil fora
#Kraken: $2 milhões em | $2 milhões fora
#Kucoin: $406 mil em | $235 mil fora
#Poloniex: $325 mil em | $352 mil fora

*Fluxos semanais de câmbio de BTC*
Entrada: $703,8 milhões (-42,1% em relação à semana passada)
Saída: $763,5 milhões (-27,8% em relação à semana passada)
Fluxo líquido: -US$ 59,7 milhões
Preço do #BTC: US$ 8.084,63 (-1,3% em relação à semana passada)

*Fluxos semanais de câmbio de ETH*
Entrada: US$ 119,1 milhões (-37,5% em relação à semana passada)
Saída: US$ 111,8 milhões (-48,7% em relação à semana passada)
Fluxo líquido: $7,3 milhões
Preço do #ETH: $175,74 (+0,8% em relação à semana passada)

*Fluxos semanais de stablecoins*
Entrada: $264,3 milhões (-51,1% em relação à semana passada)
Saída: $364,0 milhões (-45,7% em relação à semana passada)
Fluxo líquido: -$99,7 milhões

