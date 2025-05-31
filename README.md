# brasil_rawjsondata
json para testes, com atualização mensal, sem login, sem necessidade de cadastro, direto do arquivo, foco Brasil.

## Brasil Botânica
### frutas brasil ( link raw rjd_frutas_brasil.json [* CTRL+s Salvar pelo navegador] )
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
### brasil geo ( link raw rjd_brasil_2025.json [* CTRL+s Salvar pelo navegador] )
🔗 [rjd_brasil_2025](https://raw.githubusercontent.com/charles-cs50/brasil_rawjsondata/refs/heads/main/rjd_brasil_2025.json)
```
campos: estado_nome, estado_capital, sigla_estado, fronteira_com, estado_ddd.
ordem : alfabetica.
data  : 30/05/25
```
```jsonc
// preview do primeiro campo
"estado_nome": "Acre",
"estado_capital": "Rio Branco",
"sigla_estado": "AC",
"estado_populacao": 840939,
"fronteira_com": ["Amazonas", "Rondônia", "Peru", "Bolívia"],
"estado_ddd": ["68"]
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
```html
<?php
# proto: client.php ~> local file. [run]> php client.php

# php cliente
$url = 'https://raw.githubusercontent.com/charles-cs50/brasil_rawjsondata/refs/heads/main/rjd_nomes_femininos.json';
$response = @file_get_contents($url);

if ($response !== false) {
    $data = json_decode($response, true); // Decodifica a string JSON para um array associativo

    if ($data !== null) {
        echo "<pre>"; // Tag <pre> para preservar a formatação
        echo json_encode($data, JSON_PRETTY_PRINT | JSON_UNESCAPED_UNICODE); // Codifica o array de volta para JSON formatado
        echo "</pre>";
    } else {
        echo "Erro ao decodificar a resposta JSON.";
    }
} else {
    echo "Erro ao consumir a API.";
}

?>
```
