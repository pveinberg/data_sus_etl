
## Fonte de dados

https://datasus.saude.gov.br/transferencia-de-arquivos/#


* podemos usar:
SIAsus  -sistema de informações ambulatoriais
SINSN
SINASC

## Projeto
wendel tem no github

### Fork do original
https://github.com/pveinberg/data_sus_etl/


## Passos

pode ser feito um loop por estado e data para pegar vários dados

RDPE2303.dbc

RD = tipo de dado
PE = Estado (pernambuco)
23 = Ano 2023
03 = Mês (março)

## Url
ftp ftp://ftp.datasus.gov.br/dissemin/publicos/SIHSUS/200801_/Dados/RDPE2303.dbc

## Consulta GPT

Levando em consideração a tabela 8.1 COMPATIBILIDADE DE TIPO DE VÍNCULO COM TIPO DE ATO no arquivo anexo

Extrair os códigos de "TIPO DE ATO" para formato dict (python)

Por exemplo:

{
    "codigo": 7,
    "descricao": "Profissional Autônomo PF",
    "tipo_de_ato": [
        ("01", "Cirurgião ou Obstetra"),
        ("02", "1.º Auxiliar Cirúrgico"),
        ("03", "2.º Auxiliar Cirúrgico"),
        ("04", "3.º Auxiliar Cirúrgico"),
        ("05", "Demais Auxiliares Cirúrgicos"),
        ("06", "Anestesia"),
        ("07", "Consulta Clínica"),
        ("27", "Neurocirurgia")
    ]
}

