
# NGINX Proxy Automation 🔥

<div class="Disclaimer">
<div class="DisclaimerHead">
Disclaimer 1:
</div>
<div class="DisclaimerBody">
I've forked this code from: <a target="_blank" href="https://docs.docker.com/">gh:evertramos/nginx-proxy-automation</a> not to gain the credits but too ensure that it stay's available in a matter that I assume it to be, as I plan to base some of my projects on it!
</div>
</div>

<p align="center">
   <a target="_blank" href="https://docs.docker.com/"><img src="https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white" /></a>
   <a target="_blank" href="https://docs.nginx.com/"><img src="https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white" /></a> 
</p>
<p align="center">
   <a target="_blank" href="https://letsencrypt.org/docs/"><img src="https://img.shields.io/badge/Secured_by-Let's_Encrypt-blue.svg?logo=let%E2%80%99s-encrypt" /></a>
</p>

<p align="center">
   <img src="https://github.com/evertramos/images/raw/master/webproxy.jpg" />
</p>

## How to start 🔰
[![shell script](https://img.shields.io/badge/Shell_Script-121011?style=for-the-badge&logo=gnu-bash&logoColor=white)](https://github.com/evertramos)


1. Clone this repository using the option **_--recurse-submodules_** ⚠️

```bash
git clone --recurse-submodules https://github.com/evertramos/nginx-proxy-automation.git proxy 
```

We use submodule for [basescript](https://github.com/evertramos/basescript)

2. 🚀 Run the script 'fresh_start.sh' from the _./proxy/bin_ folder
   
```bash
cd proxy/bin && ./fresh-start.sh --yes -e your_email@domain --skip-docker-image-check
```

Update the email above with your real e-mail address

3. 🧪 Test the proxy

```bash
docker run -dit -e VIRTUAL_HOST=your.domain.com --network=proxy --name test-web httpd:alpine
```
or simply run:
```bash
./test.sh your.domain.com
```

Use your own domain name when testing this proxy and make sure your DNS is correctly configured.




<style>
.Disclaimer{
    outline: .1em solid yellow;
    background: lightgoldenrodyellow;
    color: black;
}
.DisclaimerHead{
  text-align: center;
     background: khaki;
     color: goldenrod;
}

.DisclaimerHead::before , .DisclaimerHead::after {
       
     content:':bangbang:'
     
}

.DisclaimerHead{
    
}

.warning{
    color:red;    
     font-weight:bolder;
}
.underline{
    text-decoration: underline;
}

</style>
