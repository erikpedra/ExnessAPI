# Sosial Media
Telegram : https://t.me/minsanztuy        
Website    : https://autotradevip.com/en/  
Olmyptrade : https://youtu.be/zTZT7zDlmtU  
Binomo     : https://youtu.be/ww9rVMX5TK4  
IQ Option  : https://youtu.be/4i3YUEDRGWY  
Quotex     : https://www.youtube.com/channel/UCCqnm8XHUoc0Ude78RJwmoA  
Expert Option     : https://www.youtube.com/channel/UCCqnm8XHUoc0Ude78RJwmoA
# exnessapi
Exness API  


### Import
```python
from exnessapi import Exness
```

### Login 
if connect sucess return True,None  
if connect fail return False,reason  
```python
from exnessapi import Exness
account=Exness(host="my.exness-trader.market",login="1234567890")
check_connect,message=account.connect()
print(check_connect,message)
```

### Get Balance
change_balance
Exness only have real mode account,or you can control by account_id

```python
from exnessapi import Exness
account=Exness(host="my.exness-trader.market",login="1234567890")
check_connect,message=account.connect()
balance=account.get_balance()
print(balance)
account.close()
```

### Get Candle
```python
from exnessapi import Exness
account=Exness(host="my.exness-trader.market",login="1234567890")
check,message=account.connect()
if check:
    asset="EURUSDm"
    limit=100 #how much candle you can to get is last to pass.
    timeframe=5 #5minute
    candle=account.get_candle(asset,timeframe,limit)
    for c in candle:
        print(c)
    account.close()
```

### get_server_time
```python
from exnessapi import Exness
account=Exness(host="my.exness-trader.market",login="1234567890")
check_connect,message=account.connect()
serverMT =account.server()
print(serverMT)
account.close()
```

### Get Symbol
```python
from exnessapi import Exness
account=Exness(host="my.exness-trader.market",login="1234567890")
check_connect,message=account.connect()
symbol =api.get_symbol()
for c in symbol:
    print(c)
account.close()
```
