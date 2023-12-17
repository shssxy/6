#coding:utf-8   
import requests,json   
headers={'Content-Type': 'application/json'}  
webhook = 'https://oapi.dingtalk.com/robot/send?access_token=xxxxxxxxxx' 
data = {
    "msgtype": "text",
    "text": {"content": '            ' + '\n'  +  "@" + mobile + 'test' + '\n' + '            '},
    "at": {"atMobiles": "['"+ mobile + "']","isAtAll": False}
}
requests.post(webhook, data=json.dumps(data), headers=headers) 
