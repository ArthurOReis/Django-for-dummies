# Configurações, Git e GitHub
***
## Idioma e Timezone

#### Quando um projeto Django é criado, por padrão, ele é setado com a língua inglesa e uma Timezone UTC. Para poder acesar e manipular essas informações, na pasta 'setup', e em 'settings.py', aparecerá essas informações na linha 106 e 108.

![Diretório Django](./imgs/img.png)

![Código com timezone e lingua](./imgs/img_1.png)

#### Com as variáveis localizadas, altera-se os seus valores, ficando:

![Código com timezone e lingua alteradas](./imgs/img_2.png)

### Como o site fica após as alterações:

![Site Django em portugês](./imgs/img_3.png)
***

## Variáveis de ambiente

#### Todo projeto Django possui uma 'SECRET_KEY', que como o nome sugere, é um elemento secreto, onde a sua principal função é dar funcionamento ao site. Entretanto, se ao commitar e 'pushar' o projeto, pode ocorrer o risco de alguém remover a chave secreta, impedindo o seu funcionamento:

![Site Django não funcionando](./imgs/img_4.png)

#### Por padrão, as SECRET_KEYS estão na linha 23 dentro de 'settings.py', sendo atribuidas a um valor criptografado:

![SECRET_KEY](./imgs/img_5.png)

#### Uma das maneiras de lidar com esse problema, é instalando a biblioteca python-dotenv:

~~~terminal
pip install python-dotenv
~~~

#### LEMBRANDO: para se certificar de que a biblioteca está instalada e faz parte dos requisitos do seu projeto, no terminal, escreva:
~~~terminal
pip freeze > requirements.txt
~~~

#### Isso vai fazer com que seja criado um arquivo de texto mostrando todos os requisitos do seu web aplicativo:

![requisitos](./imgs/img_6.png)

#### Com a instalação do Python-Dotenv, o próximo passo é tirar o valor da SECRET_KEY, criar um arquivo no diretório global (fora da pasta Setup) com o nome '.env', e criar uma variável com o mesmo nome e valor original, porém sem as aspas:

![copiar código](./imgs/img_7.png)
![colar código](./imgs/img_8.png)

#### Feito isso, no settings.py, precisa-se importar 'load_dotenv' de dotenv, chama-se função do mesmo nome, e por fim, obtenha o valor da SECRET_KEY por uma função e converta em String:

![chamando SECRET_KEY](./imgs/img_9.png)
***
### Git e Github

#### Tendo o projeto ou uma das etapas do projeto concluída, deverá exportar todo o trabalho no GitHub, entretanto é fortemente recomendado usar gitignore para não lidar com problemas envolvendo segurança, upload desnecessário e entre outros... 
#### Dito isso, é preciso criar um arquivo no diretório global com o nome '.gitignore', em seguida, visite o site [gititgnore.io](https://www.toptal.com/developers/gitignore/) e pesquise por Django no input do site, em seguida dê *CTRL A* e copia todo o código selecionado. Por fim, insira todo o código no arquivo criado e o projeto estará pronto para ser enviado:

![criando .gitignore](./imgs/img_10.png)
![acessando gitignore.io](./imgs/img_11.png)
![copiando gitignore](./imgs/img_12.png)
![codificando gitignore](./imgs/img_13.png)
***
## [Resolução da parte 1](https://github.com/ArthurOReis/Django-parte_1)