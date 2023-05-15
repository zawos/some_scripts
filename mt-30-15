
import requests
import time
url = 'https://promotion.waimai.meituan.com/lottery/limitcouponcomponent/fetchcoupon'
cookies = 'abcd'
data = {
    'couponReferId':'F6CFF2A35BD94F49BDEE0CC6F7CF9FE4',#更新id
    'actualLng':'113.333694',
    'actualLat' : '22.401359',
    'geoType' : '2',
    'gdPageId': '306477',
    'pageId' : '306004',
    'version' : '1',
    'utmSource':'',
    'utmCampaign':'',
    'instanceId' :'16620226080900.11717750606071209',
    'componentId' : '16620226080900.11717750606071209'
    }
headers = {
    'Connection':'keep-alive',
    'Content-Length':'2360',
    'Accept':'application/json, text/plain, */*',
    'mtgsig':'{"a1":"1.0","a2":1684137484188,"a3":"3858z8605u455vwx19yy0346zyx310538119wu60x2y97958442w029z","a4":"47fec0b239749f0ab2c0fe470a9f74392e5f945924c0e060","a5":"wjzLzgUzMESQJHZ5wkPLbyuY2jNzWKYc/j/eTRi2yAu6yx2PzbbhWJNuULBktKWJajxwtPEE14x5CxoGSRn6fFJpzHV=","a6":"h1.2YpUBnl0CySEyhaWidBVHVdHnBtPt44T0nM67A3y3nuupncfd9vgXdaBNSji0KQ7Hbkw1A24R63p8TAzVUalD3wV5PQEB7WELfnIxRVYdSA+IvKwvVqBdX2E3S0/SjDFM2Amdr0uJOU5q4vExPQmgqjeQLm1A2KpUJ0ypD1dKZMI1u6Yp9aqr4OPTJqXyRD6M5LMQaJsZMCrWH6nLy3ZvAjAGVJWDrQxojFqkbG+hwbiI4jG9jVf+lFbGBOkOfumGzPYBB4br70iN90G+xbtsfYu+Q8K1mXbqvLdw4zeWTRrc7yg3hubNfC6f5ayDw2luvsARlCWIvJFCwKa7BQxgNEvShDpkTBz8a87NM9uAVyqNtuN+zE1Ga676uILZWM5GW7oWzoBhJTdKVYMcHV0S8hlW4X+w3UUM7EcODsD5ogc=","a7":"","x0":4,"d1":"b8a5d83be74c104555ecf1bdc1d5dd29"}',

    'User-Agent':'Mozilla/5.0 (Linux; U; Android 11; zh-cn; Redmi K30i 5G Build/RKQ1.200826.002) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/100.0.4896.127 Mobile Safari/537.36 XiaoMi/MiuiBrowser/17.6.40423 swan-mibrowser',
    'Content-Type':'application/json',
    'Origin':'https://market.waimai.meituan.com',
    'Referer':'https://market.waimai.meituan.com/',
    'Accept-Encoding':'gzip, deflate, br',
    'Accept-Language':'zh-CN,zh;q=0.9,en-US;q=0.8,en;q=0.7',
    'Cookie':cookies,
    }
json_data = {
    "cType":"mti",
    "fpPlatform":3,
    "wxOpenId":"",
    "appVersion":"",
    "mtFingerprint":"H5dfp_1.8.2_tttt_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"}
msg = ''
while '成功' not in msg:
    response = requests.post(url,headers = headers,params=data,json = json_data)
    msg = response.text
    print('msg：',msg)
    if '已领取' in msg or '来晚了' in msg:
        print('留点机会给年轻人吧！msg：',msg)
        break
    time.sleep(0.002)
else:
    print('领取成功，msg为：',msg)
    
