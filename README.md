# brasil_rawjsondata
json para testes, com atualização mensal, sem login, sem necessidade de cadastro, direto do arquivo, foco Brasil.

## Brasil Botânica
### brasil_frutas ( link raw rjd_frutas_brasil.json [ * CTRL+s Salvar pelo navegador ] )
🔗 [rjd_frutas_brasil](https://raw.githubusercontent.com/charles-cs50/brasil_rawjsondata/refs/heads/main/rjd_frutas_brasil.json)
```
campos  : nome, origem, estado_produtor, imagem, usada_em ( em qual receita se usa: suco, bolos, enfim ), nome_cientifico
ordem   : alfabetica
data    : 30/10/2025
imagens : nome_da_fruta.png 650x650 pixels - color 8bit ~~> fundo transparente.
OBS: link sendo atualizado e padronizado, as imagens serão todas do mesmo tamanho, formato e paleta de 8bits. 
```
```jsonc
// preview do primeiro campo
"nome": "Abiu",
"origem": "Brasil",
"estado_produtor": "MG, SP, PR, SC",
"imagem": "https://i.postimg.cc/BbnZrmCv/abiu.png",
"usada_em": "in natura, doces, geleias, licores",
"nome_cientifico":" Pouteria caimito (Ruiz & Pav.) Radlk. Sinônimos incluem Lucuma caimito e Achras caimito."
```
#### link raw txt {endpoint}
```
https://raw.githubusercontent.com/charles-cs50/brasil_rawjsondata/refs/heads/main/rjd_frutas_brasil.json
```

## Brasil Geo
### brasil_geo ( link raw rjd_brasil_2025.json [ * CTRL+s Salvar pelo navegador ] )
🔗 [rjd_brasil_2025](https://raw.githubusercontent.com/charles-cs50/brasil_rawjsondata/refs/heads/main/rjd_brasil_2025.json)
```
campos: estado_nome, estado_capital, estado_sigla, fronteira_com, estado_ddd.
ordem : alfabetica.
data  : 30/05/25
```
```jsonc
// preview do primeiro campo
"estado_nome": "Acre",
"estado_capital": "Rio Branco",
"estado_sigla": "AC",
"estado_populacao": "880.631",
"estado_area":"152.581 km²",
"estado_googlemaps":" ...link... ",
"estado_wazemaps":"...link... ",
"estado_fronteira_com": ["Amazonas", "Rondônia", "Peru", "Bolívia"],
"estado_ddd": ["68"],
"estado_naturalidade":"acriano"
```
#### link raw txt {endpoint}
```
https://raw.githubusercontent.com/charles-cs50/brasil_rawjsondata/refs/heads/main/rjd_brasil_2025.json
```
# Clients
### Python client ( * lib requests ) 🚀 testado.
```python
# proto: client.py ~> local file. [run]> python client.py or python3 client.py

# python client
import requests
url='https://raw.githubusercontent.com/charles-cs50/brasil_rawjsondata/refs/heads/main/rjd_brasil_2025.json'
req=requests.get(url)
dic=req.json()

# preview data
print(req, end='\n\n')
print(dic)

# Obtendo index para verificar o dicionário.
rjd_index=dic["Brasil"]["index"]
print('index: \n', rjd_index, end='\n\n')

# pegando dados "Acre"
estado_acre=dic["Brasil"]["001"]
print('dados Acre: \n', estado_acre)
```
```python
""" retorno do rjd_index=dic["Brasil"]["index"] """

#>>> index: 
 #    {'Acre': '001', 'Alagoas': '002', 'Amapá': '003', 'Amazonas': '004', 'Bahia': '005', ... }
```
### Javascript ( fetch js ) 🚀 testado.
```javascript
// proto: client.js ~> local file. [run]> node client.js

// Javascript client
fetch('https://raw.githubusercontent.com/charles-cs50/brasil_rawjsondata/refs/heads/main/rjd_frutas_brasil.json')
  .then(response => response.json())
  .then(data => {
    // const textarea = document.getElementById('suaTextarea'); html
    // textarea.value = JSON.stringify(data, null, 2); html
    console.log(JSON.stringify(data, null, 2)); 
  })
  .catch(error => {
    console.error('Erro ao buscar os dados:', error);
});
```
### PHP ( @file_get_contents() ) 🚀 testado.
```php
<?php
# proto: client.php ~> local file. [run]> php client.php

# php cliente
$url = 'https://raw.githubusercontent.com/charles-cs50/brasil_rawjsondata/refs/heads/main/rjd_nomes_femininos.json';
$response = @file_get_contents($url);

if ($response !== false) {
    $data = json_decode($response, true);
    if ($data !== null) {
        echo "<pre>"; 
        echo json_encode($data, JSON_PRETTY_PRINT | JSON_UNESCAPED_UNICODE); # encoding:utf-8 ~> JSON_UNESCAPED_UNICODE
        echo "</pre>";
    } else {
        echo "Erro ao decodificar a resposta JSON.";
    }
} else {
    echo "Erro ao consumir a API.";
}
?>
```
