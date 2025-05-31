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
```
```jsonc
// preview do primeiro campo
"nome": "Abiu",
"origem": "Brasil",
"estado_produtor": "MG, SP, PR, SC",
"imagem": "https://upload.wikimedia.org/wikipedia/commons/thumb/a/ac/Lucuma_salicifolia_fruto.jpg/800px-Lucuma_salicifolia_fruto.jpg",
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
#### link raw txt {endpont}
```
https://raw.githubusercontent.com/charles-cs50/brasil_rawjsondata/refs/heads/main/rjd_brasil_2025.json
```
### python client ( * lib requests )
```python
# python client
import requests
url='https://raw.githubusercontent.com/charles-cs50/brasil_rawjsondata/refs/heads/main/rjd_brasil_2025.json'
req=requests.get(url)
dic=req.json()
# preview data
print(req, end='\n\n')
print(dic)
```
