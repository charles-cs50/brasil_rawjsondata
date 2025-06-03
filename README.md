#  [![jackal-11-24-v2-32-inverted.png](https://i.postimg.cc/wBPhM5Lv/jackal-11-24-v2-32-inverted.png)]()  CODEBABEL

# brasil_rawjsondata: 0.0.1
## 📃 Descrição
```
rawjsondata/rjd: json para testes, com atualização mensal, sem login, sem necessidade de cadastro,
direto do arquivo, foco Brasil.
```
[![](https://i.postimg.cc/28XCfSZj/rjd-banner.png)]()

# 🧭 Conteúdo
#### BOTÂNICA
* [Brasil Botânica 🥇](#brbo)
* [Brasil Frutas 🥈](#brbo_frutas)
* [Brasil Frutas/Campos](#brbo_frutas_cam)
* [Brasil Frutas/Visualização](#brbo_frutas_vis)
* [Brasil Frutas/Endpoint](#brbo_frutas_end)
#### GEO
* [Brasil Geo 🥇](#brge)
* [Brasil Geo/Campos](#brge_geo_cam)
* [Brasil Geo/Visualização](#brge_geo_vis)
* [Brasil Geo/Endpoint](#brge_geo_end)
##### GEO_nomes
* [Brasil Nomes Femininos](#installation)
* [Brasil Nomes Masculinos](#installation)
##### GEO_carros
* [Brasil Carros Lançados](#installation)
* [Brasil Carros Nacionais](#installation)
#### CLIENTES
* [Clients/Clientes 🥇](#brcl)
* [Clients/Clientes Python](#brcl_py)
* [Clients/Clientes Javascript](#brcl_js)
* [Clients/Clientes PHP](#brcl_ph)

### brbo
# Brasil Botânica

## 🍓 Frutas Brasil
### brbo_frutas
🔗 [rjd_brasil_bot_frutas](https://raw.githubusercontent.com/charles-cs50/brasil_rawjsondata/refs/heads/main/rjd_brasil_bot_frutas.json)

## 📅 Campos
### brbo_frutas_cam
```
campos  : nome, origem, estado_produtor, imagem, usada_em ( em qual receita se usa: suco, bolos, enfim ), nome_cientifico.

ordem   : alfabetica
data    : 30/10/2025
imagens : nome_da_fruta.png 650x650 pixels - color 8bit ~~> fundo transparente.
OBS: link sendo atualizado e padronizado, as imagens serão todas do mesmo tamanho, formato e paleta de 8bits. 
```

## 📅 Visualização
### brbo_frutas_vis
```jsonc
// preview do primeiro campo
"nome": "Abiu",
"origem": "Brasil",
"estado_produtor": "MG, SP, PR, SC",
"imagem": "https://i.postimg.cc/BbnZrmCv/abiu.png",
"usada_em": "in natura, doces, geleias, licores",
"nome_cientifico":" Pouteria caimito (Ruiz & Pav.) Radlk. Sinônimos incluem Lucuma caimito e Achras caimito."
```
## 🔥 Endpoint
### brbo_frutas_end
```
! Em desenvolvimento... (*imagens)
```

### brge
# 🌐 Brasil Geo

## brasil_2025
### brge_geo
🔗 [rjd_brasil_geo_2025](https://raw.githubusercontent.com/charles-cs50/brasil_rawjsondata/refs/heads/main/rjd_brasil_geo_2025.json)

## 📅 Campos
### brge_geo_cam
```
campos: estado_nome, estado_capital, estado_sigla, estado_populacao, estado_area, estado_googlemaps, estado_wazemaps, estado_fronteira_com, estado_ddd, estado_naturalidade.

ordem : alfabetica  e index: 001 à 026.
data  : 30/05/25
```

## 📅 Visualização
### brge_geo_vis
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

## 🔥 Endpoint
### brge_geo_end
```
https://raw.githubusercontent.com/charles-cs50/brasil_rawjsondata/refs/heads/main/rjd_brasil_geo_2025.json
```

## 👥 Brasil Nomes Femininos
### brge_nomes_fem
🔗 [rjd_brasil_geo_nomesfem](https://raw.githubusercontent.com/charles-cs50/brasil_rawjsondata/refs/heads/main/rjd_brasil_geo_nomesfem.json)

## 📅 Campos
### brge_nomesfem_cam
```
campos: nome, origem, significado.
ordem : alfabetica.
data  : 30/05/25
```

## 📅 Visualização
### brge_nomefem_vis
```jsonc
// preview do primeiro campo
"nome": "Abigail",
"origem": "Hebraico",
"significado": "Meu pai é alegria"
```

## 🔥 Endpoint
### brge_nomefem_end
```
https://raw.githubusercontent.com/charles-cs50/brasil_rawjsondata/refs/heads/main/rjd_brasil_geo_nomesfem.json
```

## 👥 Brasil Nomes Masculinos
### brge_nomes_mas
🔗 [rjd_brasil_geo_nomesmas](https://raw.githubusercontent.com/charles-cs50/brasil_rawjsondata/refs/heads/main/rjd_brasil_geo_nomesmas.json)

## 📅 Campos
### brge_nomesmas_cam
```
campos: nome, origem, significado.
ordem : alfabetica.
data  : 30/05/25
```

## 📅 Visualização
### brge_nomesmas_vis
```jsonc
// preview do primeiro campo
"nome": "Abel",
"origem": "Hebraico (Hével)",
"significado": "Vapor, sopro"
```

## 🔥 Endpoint
### brge_nomesmas_end
```
https://raw.githubusercontent.com/charles-cs50/brasil_rawjsondata/refs/heads/main/rjd_brasil_geo_nomesmas.json
```

## 🚗 Brasil Carros Lançados
### brge_carros_lan
🔗 [rjd_barsil_geo_carroslancados]()

## 📅 Campos
### brge_carroslan_cam
```
campos: nome, ano_lancamento, fabricante, categoria, imagem.

ordem : alfabetica.
data  : 30/05/25
```

## 📅 Visualização
### brge_carroslan_vis
```jsonc
// preview do primeiro campo
"nome": "Fiat Uno",
"ano_lancamento": 1984,
"fabricante": "Fiat",
"categoria": "hatch",
"imagem": " ...link... "
```

## 🔥 Endpoint
### brge_carroslan_end
```
! em desenvolvimento... (*Imagens e json final)
```

### brcl
# 💻 Clients/Clientes

## ✅ Python client ( * lib requests )
### brcl_py
```python
# proto: client.py ~> local file. [run]> python client.py or python3 client.py

# python client - Endpoint ~> url
import requests
url='https://raw.githubusercontent.com/charles-cs50/brasil_rawjsondata/refs/heads/main/rjd_brasil_geo_2025.json'

req=requests.get(url)
dic=req.json()

# preview data
print(req, end='\n\n')
print(dic)

# Obtendo index para verificar o dicionário.
rjd_index=dic["Brasil"]["index"]
print('index: \n', rjd_index, end='\n\n')

# demais detalhes 
rjd_detalhes=dic["Brasil"]["detalhes"]
brasil_estados_quantidade=rjd_detalhes["brasil_estados"]
print(rjd_detalhes)
print('Brasil estados : ', brasil_estados_quantidade)

# pegando dados "Acre"
estado_acre=dic["Brasil"]["001"]
print('dados Acre: \n', estado_acre)
```
```python
rjd_index=dic["Brasil"]["index"]
print(rjd_index)

""" retorno terminal """
#>>> index: 
 #    {'Acre': '001', 'Alagoas': '002', 'Amapá': '003', 'Amazonas': '004', 'Bahia': '005', ... }
```
## ✅ Javascript ( fetch js )
### brcl_js
```javascript
// proto: client.js ~> local file. [run]> node client.js

// Javascript client - Endpoint ~> const url
const url='https://raw.githubusercontent.com/charles-cs50/brasil_rawjsondata/refs/heads/main/rjd_brasil_geo_2025.json'

fetch(url)
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
## ✅ PHP ( @file_get_contents() )
### brcl_ph
```php
<?php
# proto: client.php ~> local file. [run]> php client.php

# php cliente - Endpoint ~> $url
$url = 'https://raw.githubusercontent.com/charles-cs50/brasil_rawjsondata/refs/heads/main/rjd_brasil_geo_2025.json';

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
