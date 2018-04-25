# IQ Option API(Frok from [n1nj4z33/iqoptionapi](https://github.com/n1nj4z33/iqoptionapi))
fix some thing...
update:2018/4/25
sucess on python3.6.4

---

### Installation & GET new version
```
sudo pip3 install git+git://github.com/Lu-Yi-Hsun/iqoptionapi.git
```
---
### Import 
```
from iqoptionapi.stable_api import IQ_Option
```
### login
```
I_want_money=IQ_Option("email","password")
```
### buy
```
I_want_money.buy(Money,ACTIVES,ACTION)
                #Money:How many you want to buy type(number)
                #ACTIVES:sample input "EURUSD" OR "EURGBP".... you need to look constants.py file type(str)
                #ACTION:"call"/"put" type(str)
```

### get candles
!!!pay attention!!! get_candles can not get "real time data" ,it will late about 30sec
if you very care about real time you need use "get  realtime candles"
sample 

you want to get  candles 1:30:45sec now

you may get 1:30:15sec data have been late approximately 30sec


```
I_want_money.get_candles(ACTIVES,interval,count,endtime)
            #ACTIVES:sample input "EURUSD" OR "EURGBP".... you need to look constants.py file type(str)
            #interval:duration of candles
            #count:how many candles you want to get from now to past
            #endtime:get candles from past to "endtime"
```
### get  realtime candles
you will get ""latest"" DATA
```
I_want_money.get_realtime_candles("EURUSD")
```
### get all profit
```
I_want_money.get_all_profit()
#return type(dict) sample:dict["EURUSD"]=0.85 
```
### get balance
```
I_want_money.get_balance()
```

### check win
```
I_want_money.check_win()
#this function will do loop check your bet until if win/equal/loose
```
## Will Add new option........

### Change real/practice Account
```
```
### sell
```
```