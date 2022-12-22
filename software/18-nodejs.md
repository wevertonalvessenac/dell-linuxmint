#Autor: Robson Vaamonde<br>
#Procedimentos em TI: http://procedimentosemti.com.br<br>
#Bora para Prática: http://boraparapratica.com.br<br>
#Robson Vaamonde: http://vaamonde.com.br<br>
#Facebook Procedimentos em TI: https://www.facebook.com/ProcedimentosEmTi<br>
#Facebook Bora para Prática: https://www.facebook.com/BoraParaPratica<br>
#Instagram Procedimentos em TI: https://www.instagram.com/procedimentoem<br>
#YouTUBE Bora Para Prática: https://www.youtube.com/boraparapratica<br>
#Data de criação: 22/12/2022<br>
#Data de atualização: 22/12/2022<br>
#Versão: 0.01<br>
#Testado e homologado no Linux Mint 20.1 Ulyssa, 20.2 Uma e 20.3 Una x64

Instalação do Node.JS e NPM no Linux Mint 20.1 Ulyssa, 20.2 Uma e 20.3 Una x64

Site Oficial do Node.JS: https://nodejs.org/en/

#00_ Verificando as Informações do Sistema Operacional Linux Mint<br>

	Terminal: Ctrl + Alt + T

	OBSERVAÇÃO IMPORTANTE: Linux Mint 20.3 Una é derivado do Ubuntu Desktop 20.04.4 Focal Fossa
	sudo cat /etc/os-release
	sudo cat /etc/lsb-release
	Menu
		Informações do Sistema

#01_ Atualização do Sistema Operacional Linux Mint<br>

	_ Atualização do sistema utilizando o MintUpdate;
	_ Atualização do sistema utilizando o Apt;

	Terminal: Ctrl + Alt + T
		sudo apt update
		sudo apt upgrade
		sudo apt full-upgrade
		sudo apt dist-upgrade
		sudo apt autoremove
		sudo apt autoclean

#02_ Instalando as Dependências do Node.JS no Linux Mint<br>

	_ sudo apt install git vim curl gcc g++ make build-essential

#03_ Instalando a Versão LTS do Node.JS no Linux Mint<br>

	_ sudo curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash
	_ sudo sudo apt install nodejs npm

#04_ Verificando as Versões do Node.JS e NPM no Linux Mint<br>

	_ sudo nodejs -v
	_ sudo npm -v

#05_ Criando um Projeto Simples para Testar o Node.JS no Linux Mint<br>

	_ md nodejs-hello
	_ cd nodejs-hello
	_	npm init -y
	_	npm install express --save

#06_ Editando o Projeto Simples do Node.JS o VSCode no Linux Mint<br>

	_ code .
	_ OBSERVAÇÃO IMPORTANTE: nesse exemplo vamos editar o arquivo index.js

	var express = require ('express'); 
	var app = express();
	
	app.get('/', function (req, res) {
		res.send('Robson Vaamonde #BoraParaPrática!!!');
	});

	app.listen(3000, function() {
		console.log('Aplicativo de exemplo ouvindo na porta 3000');
	});

#07_ Executando o Projeto Simples do Node.JS no Linux Mint<br>

	_ node index.js
	_ firefox http://localhost:3000/