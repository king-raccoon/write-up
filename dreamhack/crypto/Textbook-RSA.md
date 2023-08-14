<https://dreamhack.io/wargame/challenges/131>

N: 144918197968628123944881508887621016687723837701442108302516619394612525708078719299953319375167967446781372165706433948939714109407511545048581027742262538739751471796346239726842318801555786640636975633032130752723968541557035414516725166787504667513685936598043879485723829933465720891169231800160765272299
e: 65537
FLAG: 42736505956125746720831151775407113070690948888119136795093702713933511667154822404667039493117966861025151858242008275920416809520252136526333671378365024856274343050535298717089041503371179913061190671754599017776046309048685778053376242900213260066665375868114859569261313594512464834105757322316604251675

```
from Crypto.Util.number import long_to_bytes

N = 144918197968628123944881508887621016687723837701442108302516619394612525708078719299953319375167967446781372165706433948939714109407511545048581027742262538739751471796346239726842318801555786640636975633032130752723968541557035414516725166787504667513685936598043879485723829933465720891169231800160765272299
e = 65537
FLAG = 42736505956125746720831151775407113070690948888119136795093702713933511667154822404667039493117966861025151858242008275920416809520252136526333671378365024856274343050535298717089041503371179913061190671754599017776046309048685778053376242900213260066665375868114859569261313594512464834105757322316604251675
FLAG_enc = 72703496255418845402381729405721784563522667457656217580878653485292156443118611981728589672224125224875295717734320989482439656417077716501728961810633467287708985477547555360845673327965767587590905649493804902945052981649410455895232068833220581022164701360968855593703197265299594714934568308524080707151
c = (pow(2, e) * FLAG) % N
c = hex(c)[2:]
print(c)
#c = 679c774877d8c08b6cb12b921957fdecf57acfcb21e29cfa48205e654d02e2f49783361f89ba24327dc79360b8c9b6dbbb68553e72345d8f291a632565132a57076a771f364b94eb30f5b1bd94963cff3adb5e1b64c687ed818ce40b63f196974313d95052799eb654ea9490461ec80dd7ee82f787d146f2f6ecfb143d58932c
c_dec = 265303025271760754782762668660255715813910508769429152493707039977108929146371416679674
c_dec = c_dec //2
print(long_to_bytes(c_dec))
```