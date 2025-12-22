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

### Atividades de transação

```
/w USDT mint
```

```
*Atividades de transação*
12/10/2019: :dollar:  2.500.000 #USDT (2.494.282 USD) cunhados no Tesouro da Tether
12/10/2019: :dollar:  5.000.000 #USDT (5.012.230 USD) cunhados na Tether Treasury
11/10/2019: :dollar: :dollar:  15.000.000 #USDT (15.077.725 USD) cunhados na Tether Treasury
10/10/2019: :dollar: :dollar: :dollar:  20.000.000 #USDT (20.002.176 USD) cunhados no Tesouro da Tether
07/10/2019: :dollar: :dollar:  12 387 600 #USDT (12 392 934 USD) cunhados na Tether Treasury
07/10/2019: :dollar: :dollar:  20 000 000 #USDT (19 952 765 USD) cunhados na Tether Treasury
04/10/2019: :dollar: :dollar:  12.600.000 #USDT (12.725.111 USD) cunhados no Tesouro da Tether
04/10/2019: :dollar:  5.000.000 USDT (5.035.628 USD) cunhados no Tesouro da Tether
30/09/2019: :dollar: :dollar:  20.000.000 #USDT (19.996.690 USD) cunhados na Tether Treasury
```

```
/w BTC Binance
```

```
*Atividades de transação*
16/10/2019: :rotating_light: :rotating_light:  3.359 #BTC (26.705.730 USD) transferidos da #Binance para carteira desconhecida
16/10/2019: :rotating_light: :rotating_light:  3.000 #BTC (23.834.707 USD) transferidos de carteira desconhecida para #Binance
14/10/2019: :rotating_light: :rotating_light:  3.000 #BTC (24.890.913 USD) transferidos de #Binance para #Gemini
11/10/2019: :rotating_light: :rotating_light:  2.721 #BTC (22.854.703 USD) transferidos da #Binance para carteira desconhecida
11/10/2019: :rotating_light: :rotating_light:  2.721 #BTC (22.648.785 USD) transferidos de carteira desconhecida para #Binance
11/10/2019: :rotating_light:  1.300 #BTC (10.937.468 USD) transferidos de carteira desconhecida para #Binance
10/10/2019: 643 #BTC (5.526.899 USD) transferidos da #Binance para carteira desconhecida
08/10/2019: 602 #BTC (4.919.049 USD) transferidos da #Binance para carteira desconhecida
08/10/2019: 1.111 #BTC (9.122.044 USD) transferidos da #Binance para carteira desconhecida
07/10/2019: 659 #BTC (5.413.301 USD) transferidos da #Coinbase para a #Binance
07/10/2019: 706 #BTC (5.772.057 USD) transferidos da #Binance para carteira desconhecida
```

### Atividades de liquidação

```
/r XBTUSD
```

```

*Atividades de liquidação*
16/11/2019 14:14:04: Liquidação de posição longa em XBTUSD: Venda de 177.058 a 8462
16/11/2019 14:13:34: Liquidação de posição longa em XBTUSD: Venda de 40.576 a 8469
16/11/2019 14:01:44: Posição curta liquidada em XBTUSD: Compra de 403.625 a 8514
16/11/2019 14:01:32: Posição curta liquidada em XBTUSD: Compra de 3.536 a 8507
16/11/2019 14:01:27: Posição curta liquidada em XBTUSD: Compra de 1 a 8500,5
16/11/2019 11:05:44: Posição longa liquidada em XBTUSD: Venda de 3.322 a 8453,5
16/11/2019 10:50:14: Posição longa liquidada em XBTUSD: Venda de 72 a 8460,5
16/11/2019 10:48:24: Posição longa liquidada em XBTUSD: Venda de 398.077 a 8468,5
16/11/2019 10:46:54: Posição longa liquidada em XBTUSD: Venda de 13.586 a 8481,5
16/11/2019 09:29:14: Posição curta liquidada em XBTUSD: Compra de 396.629 a 8527
16/11/2019 09:28:55: Posição curta liquidada em XBTUSD: Compra de 289.471 a 8519
16/11/2019 09:28:50: Posição curta liquidada em XBTUSD: Compra de 755.983 a 8511
16/11/2019 09:28:44: Posição curta liquidada em XBTUSD: Compra de 10 a 8500,5
16/11/2019 07:05:04: Posição curta liquidada em XBTUSD: Compra de 134.522 + 248.222 a 8488,5, 8496
16/11/2019 07:04:44: Posição curta liquidada em XBTUSD: Compra de 230 a 8478
16/11/2019 02:22:34: Posição longa liquidada em XBTUSD: Venda de 132.408 a 8430,5
```
### Fluxo de notícias

```
/n
```

```
*Notícias*
- [Messari Insight] O mercado mostra indiferença em relação aos ativos listados como prováveis títulos pelo Crypto Ratings Council 
- O Telegram vai adiar o lançamento da blockchain TON devido à pressão da SEC
- O Telegram pode estar sob investigação da FinCEN, a Libra Association finaliza os parceiros iniciais
- A Nasdaq lista um índice alimentado por IA dos 100 melhores desempenhos do mercado de criptomoedas
- A eToro lança uma carteira de criptomoedas ponderada por menções no Twitter
- CoinShares lança em conjunto um token de ouro “DGLD”, construído na rede bitcoin #BTC
- Layer1 busca US$ 50 milhões para operar instalações de mineração de Bitcoin movidas a energia eólica nos EUA #BTC
- Recusa do ETF de Bitcoin, tributação de airdrops de criptomoedas, o futuro da Libra e muito mais
- Grayscale obtém aprovação para o primeiro fundo de índice de moeda digital público #ETH #XRP #LTC #BTC
- [Análise] Composição DeFi entre fragmentos - Vitalik Buterin #ETH
- Booking Holdings torna-se a mais recente desistência da Libra
- Semana DeFi de 7 de outubro - The Defiant
- Telegram afirma estar em negociações com a SEC sobre a TON “há 18 meses” #GRAM
- SEC, FinCEN e CFTC emitem declaração conjunta sobre ativos digitais
- Coinbase planeia expansão na Europa após obter licença de moeda eletrónica na Irlanda
- Zcash desenvolverá token envolvido para Ethereum #ZEC #ETH
- A evolução dos mercados de capitais criptográficos
- Incentivando a participação na testnet #ATOM #DOT #ETH #TON #ERD #SOL
- Stablecoins lastreadas por moedas nacionais #USDT
- Como as criptomoedas podem se encaixar no seu portfólio #BTC #ETH
- Mercados de taxas de criptomoedas
- Libra, a iTunes App Store para desenvolvedores de criptomoedas
- Políticas monetárias de criptomoedas # KMD #VEN #XZC #WAVES #GXS #XMR #REP #ATOM #WTC #ARDR #MANA #TRX #AION #ONT #XRP #XTZ #EOS #BCD #LOOM #BCN #ZEC #STEEM #DCR #MKR #BAT #BTG #DOGE #BNB #VEIL #NANO #NEO
Fonte: https://messari.io
```

