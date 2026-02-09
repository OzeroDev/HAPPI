Install required libraries with:
```pip install pygame opencv-python flask-cors```

Run endpoint: 
```ngrok http --url=brief-uniformly-drum.ngrok-free.app 50299```

Installing ngrok (windows):
choco install ngrok

Adding auth for domain tunneling:
ngrok config add-authtoken <token>

Delete contents of 'ngrok config edit' to allow different computer to tunnel