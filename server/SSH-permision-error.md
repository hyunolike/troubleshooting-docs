## 문제
```
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@         WARNING: UNPROTECTED PRIVATE KEY FILE!          @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
Permissions 0644 for '/Users/username/.ssh/your-key.pem' are too open.
It is required that your private key files are NOT accessible by others.
This private key will be ignored.
```


## 해결
- `chmod 600 ~/.ssh/your-key.pem`
- ![image](https://user-images.githubusercontent.com/61215550/173764600-9b52be76-1920-4fb3-b93c-86e939197937.png)
