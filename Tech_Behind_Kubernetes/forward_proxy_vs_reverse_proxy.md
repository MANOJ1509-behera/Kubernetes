What’s the difference between Forward Proxy and Reverse Proxy? 🤔 
```
Are you connected to your corporate internet? You’re probably using a proxy. Do you use Nginx for your website? You’re using yet another Proxy.
So what’s the difference? Let’s break it down..


⏩ FORWARD PROXY
Also called Proxy Server, is a server that sits in front of 1 or more client machines that want to access the internet. When these clients send a request to a website or web service, the request goes via the proxy.
The Proxy then sends this request to the actual web service.
The website can only see the IP of the proxy server as the request origin, it never sees the Clients' IPs.
This way, the the clients can “hide” behind the proxy and their identity is protected.
The Proxy admin can also control which traffic to allow. This way, they can better protect clients from harmful web services.

⏪ REVERSE PROXY
A server that sits in front of 1 or more Web Servers. It receives all requests from clients across the internet and forwards them to the web servers behind them.
The clients can only see the public IP of the proxy. This way, the actual web servers can “hide” behind the reverse proxy, enjoying better protection and anonymity.
Reverse proxy can also control what traffic to forward, dropping any malicious requests upfront.
```
![reverse](https://github.com/user-attachments/assets/dea081de-21ca-4cce-945c-5e2bd9cc4d67)

