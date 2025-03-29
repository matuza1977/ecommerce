# Projeto E-commerce 
Um projeto extremamente simples de e-commerce (ainda incompleto) feito com 
Django 2.2.4 e Python 3.7.3.

### Conteúdo educacional
Este conteúdo foi criado no [Curso de Python 3 - Do Básico Ao Avançado (Completo)](https://www.udemy.com/course/python-3-do-zero-ao-avancado/) sem a intenção de 
ser utilizado em produção, mas como recurso educacional ensinado no meu curso.

Isso não impede que você baixe, altere, use e/ou distribua o seu conteúdo conforme preferir.

### Este projeto NÃO inclui
Abaixo uma lista de recursos que não adicionei ainda e que você pode me ajudar a adicionar.

- Combinações de variações de produto (tem apenas uma variação)
- Cupons de desconto no carrinho de compras
- Cálculo de frete
- Métodos de pagamento (MercadoPago, PayPal, PagSeguro, enfim...)

### TODOs
Abaixo uma lista do que adicionei ou ainda pretendo adicionar.

- [x] Model produtos
- [x] Model variações
- [x] Listagem e detalhes de produtos e variações
- [x] Carrinho de compras baseado em session
- [x] Remover produtos do carrinho
- [x] Model perfil (criar e atualizar)
- [x] Login e Logout do cliente
- [x] Registrar pedido do cliente
- [x] Página de pagamento

### Tutorial para iniciantes
Abaixo uma lista de comandos para clonar e configurar este projeto na sua 
máquina local:

- Instalar git (Windows, Linux e Mac) e depois:

```
git clone https://github.com/luizomf/django-simple-ecommerce.git
```

- Para **Windows**:

```
cd django-simple-ecommerce
python -m venv venv
venv\Scripts\activate.bat
python -m pip install --upgrade pip setuptools wheel --user
python -m pip install django django-debug-toolbar django-crispy-forms pillow
pip install bootstrap4 crispy-bootstrap4 #adicionar "  'bootstrap4', 'crispy_bootstrap4',  " no arquivo settings.py
python manage.py migrate


python manage.py migrate
```

- Para **Linux**:

```
cd django-simple-ecommerce
python3.7 -m venv venv
. venv/bin/activate
pip install django django-debug-toolbar django-crispy-forms pillow
pip install bootstrap4 crispy-bootstrap4 #adicionar "  'bootstrap4', 'crispy_bootstrap4',  " no arquivo settings.py
python manage.py migrate


python manage.py migrate
```

- Para **Mac**

```
cd django-simple-ecommerce
python -m venv .venv
source .venv/bin/activate
pip install django django-debug-toolbar django-crispy-forms pillow
pip install bootstrap4 crispy-bootstrap4 #adicionar "  'bootstrap4', 'crispy_bootstrap4',  " no arquivo settings.py
python manage.py migrate
```

Pronto!

https://stackoverflow.com/questions/75495403/django-returns-templatedoesnotexist-when-using-crispy-forms?newreg=258f43d5b55649de8301149a64238e01
<<<<<<< HEAD
=======

Ou Crie o Script Shell (linux) "ecommerce.sh"

#!/bin/bash

# Abort on errors
set -e

# Verifica se o Git está instalado e o instala se necessário
if ! command -v git &> /dev/null; then
    echo "Git não está instalado. Instalando..."
    sudo apt update && sudo apt install -y git
fi

# Clona o repositório do projeto
echo "Clonando o repositório..."
git clone https://github.com/luizomf/django-simple-ecommerce.git

# Entra no diretório do projeto
cd django-simple-ecommerce

# Verifica se Python 3.7 está instalado e o instala se necessário
if ! python3.7 --version &> /dev/null; then
    echo "Python 3.7 não está instalado. Instalando..."
    sudo apt update && sudo apt install -y python3.7 python3.7-venv python3-pip
fi

# Cria o ambiente virtual
echo "Criando o ambiente virtual..."
python3.7 -m venv venv

# Ativa o ambiente virtual
echo "Ativando o ambiente virtual..."
source venv/bin/activate

# Instala as dependências do Django e outras bibliotecas
echo "Instalando dependências..."
pip install --upgrade pip
pip install django django-debug-toolbar django-crispy-forms pillow

# Executa as migrações do banco de dados
echo "Executando as migrações..."
python manage.py migrate

echo "Configuração concluída! Para iniciar o servidor, use:"
echo "source venv/bin/activate"
echo "python manage.py runserver"

Para executar: 

chmod +x ecommerce.sh

./ecommerce.sh
>>>>>>> 38979c1 (script)
