To run the script, use `./server.py` and it will start listening for any credentials. If the target gets trapped and enters the credentials, it will be shown on the same terminal.

The above message indicates that the phishing web application is listening on port 8000; moreover, 
the `0.0.0.0` implies that it is bound to all interfaces. To confirm what the user will see, 
use Firefox on the AttackBox and browse to `http://CONNECTION_IP:8000` or `http://127.0.0.1:8000` ; 
either of these addresses will show you what the user will see. With this set, it is time to email this link to test our users’ vigilance.
