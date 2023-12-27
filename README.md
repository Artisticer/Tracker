# Tracker
Tracker
import requests

api_url = 'https://api.coinbase.com/v2/prices/spot?currency=USD'
response = requests.get(api_url)

if response.status_code == 200:
    data = response.json()
    bitcoin_price = data['data']['amount']
    print(f"Current Bitcoin Price: ${bitcoin_price}")
