<h1> Infraestrutura como Código - Script de Provisionamento de um Servidor Web (Apache) <h1/>

<h2>
1- Criar um novo diretório para o script  <br/>
mkdir scripts2 <br/>
2- Criar o script na pasta <br/>
nano script-iac2.sh <br/>
3- Após criar o script, precisa dar permissão para executar (arquivo vai mudar de cor ;D). <br/>
chmod +x script-iac2.sh <br/>
4- Depois criar um snapshot da máquina e executar <br/>
./script-iac2.sh <br/><br/>
<h2/>

---------------------------
#!/bin/bash <br/>

echo "=== Atualizando o servidor ===" <br/>
apt-get update <br/>
apt-get upgrade -y <br/>
apt-get install apache2 -y <br/>
apt-get install unzip -y <br/><br/>


echo " === Baixando | Copiando arquivos da Aplicação ===" <br/>
cd /tmp <br/>
wget https://github.com/denilsonbonatti/linux-site-dio/archive/refs/heads/main.zip <br/>
unzip main.zip <br/>
cd linux-site-dio-main <br/>
cp -R * /var/www/html/ <br/><br/>
----------------------------

<h2>
5- testar a página localmente, abri o navegador e por o ip da VM <br/>
6- "subir" o arquivo para o GitHub <br/><br/>

=== Esse arquivo será o README do repositório no GitHub ===
<h2/>
