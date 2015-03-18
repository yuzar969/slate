---
title: API Reference

language_tabs:

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='http://github.com/tripit/slate'>Documentation Powered by Slate</a>


search: false
---

# Introduction

Welcome to the Trees.ID API! You can use our API to access Trees.ID API endpoints, which can get information on various lots, blocks, projects, programs, and trees in our database.

We have language bindings in Http, Php, and Javascript! You can view code e.gs in the dark area to the right, and you can switch the programming language of the e.gs with the tabs in the top right.


# Trees.ID

> To use API, use this url or code:

```HTTP
http://api.trees.id/?

followed by the parameters and their condition.
```



> Make sure to include parameter.

Trees.ID API can free access with this base url

`http://api.trees.id/?`

<aside class="notice">
You must include parameter on base url.
</aside>

# Lots

## Get All Lots With Filter (Archive)


> The code beside returns JSONP structured like this:

```json
{
    "success": 1,
    "message": "Record(s) Found",
    "totalCount": 67101,
    "totalPage": 67101,
    "perPage": "1",
    "data": [
        {
            "id_lot": 1,
            "nama_lot": "Mekarjaya 25",
            "url_lot": "mekarjaya-25",
            "img_lot": "http:\/\/api.trees.id\/images\/lots\/00\/000\/000\/001\/Mekarjaya-25.jpg",
            "kordinat": [
                {
                    "lat": "-7.11286",
                    "lng": "107.69382"
                },
                {
                    "lat": "-7.11339",
                    "lng": "107.6935"
                },
                {
                    "lat": "-7.11387",
                    "lng": "107.69373"
                },
                {
                    "lat": "-7.11348",
                    "lng": "107.69271"
                },
                {
                    "lat": "-7.11324",
                    "lng": "107.69285"
                },
                {
                    "lat": "-7.11292",
                    "lng": "107.69283"
                }
            ],
            "kordinat_center": {
                "lat": -7.1132933333333,
                "lng": 107.69324
            },
            "img_petani": null
        }
    ]
}
```

This endpoint retrieves all lots and condition/filter.

### HTTP Request

`GET http://api.trees.id/?object=lot`

### URL Parameters

Parameter | Type (Value) | Default | Description
--------- | ------------ | ------- | -----------
object | string | null | Main condition request.
search | string | null | If not null, the result will filter with this parameter.
program_id | int | null | If not null, the result will filter with this parameter.
project_id | int | null | If not null, the result will filter with this parameter.
block_id | int | null | If not null, the result will filter with this parameter.
relawan_id | int | null | If not null, the result will filter with this parameter.
verifikator_id | int | null | If not null, the result will filter with this parameter.
petani_id | int | null | If not null, the result will filter with this parameter.
status | int (0-12) | null | If not null, the result will filter with this parameter.
content | string | data | If not null, the result will filter with this parameter.
per_page | int | 6 | Total result per request.

<aside class="success">
e.g : http://api.trees.id/?object=lot&search=mekar
</aside>

## Get a Specific Lot (Single)


> The code beside returns JSONP structured like this:

```json
{
    "success": 1,
    "message": "Record(s) Found",
    "totalCount": 1,
    "totalPage": 1,
    "perPage": 1,
    "data": [
        {
            "id_lot": 2,
            "nama_lot": "Mekarjaya 26",
            "url_lot": "mekarjaya-26",
            "img_lot": "http:\/\/api.trees.id\/images\/lots\/00\/000\/000\/002\/Mekarjaya-26.jpg",
            "content_lot": "Auto Generated Lot",
            "id_block": 6,
            "nama_block": "Mekarjaya, Lemahsugih",
            "url_block": "mekarjaya-lemahsugih",
            "img_block": "http:\/\/api.trees.id\/images\/blocks\/00\/000\/000\/006\/desa-padarek.png",
            "id_project": null,
            "nama_project": null,
            "url_project": null,
            "img_project": null,
            "id_program": 2,
            "nama_program": "Nusantara Recovery",
            "url_program": "nusantara-recovery",
            "img_program": "http:\/\/api.trees.id\/images\/programs\/00\/000\/000\/002\/banneindonesia-recovery3.jpg",
            "id_petani": 297,
            "nama_petani": "Amud",
            "img_petani": null,
            "id_relawan": 2,
            "nama_relawan": "KSBL ",
            "img_relawan": "http:\/\/api.trees.id\/images\/users\/00\/000\/000\/002\/ksbl.jpg",
            "id_pemilik": 297,
            "nama_pemilik": "Amud",
            "img_pemilik": null,
            "id_verifikator": null,
            "nama_verifikator": null,
            "img_verificator": null,
            "id_verifikator2": null,
            "nama_verifikator2": null,
            "img_verificator2": null,
            "jumlah_pohon_rencana": 1885,
            "total_pohon": null,
            "status": 0,
            "status_name": "Draft",
            "jenis_tanaman": "Jabon",
            "tanggal_tanam": "00-01",
            "luas_lahan": "0.94250",
            "luas_lahan_realisasi": "0.973",
            "kordinat": [
                {
                    "lat": "-7.11607",
                    "lng": "107.68924"
                },
                {
                    "lat": "-7.11677",
                    "lng": "107.68939"
                },
                {
                    "lat": "-7.11709",
                    "lng": "107.68858"
                },
                {
                    "lat": "-7.11651",
                    "lng": "107.68833"
                },
                {
                    "lat": "-7.1161",
                    "lng": "107.68843"
                }
            ],
            "kordinat_center": {
                "lat": -7.116508,
                "lng": 107.688794
            },
            "status_verifikasi_pohon": null,
            "polygon_from_tree": null
        }
    ]
}
```

This endpoint retrieves a specific lot.


### HTTP Request

`GET http://api.trees.id/?object=lot&id=<ID>`

### URL Parameters

Parameter | Type (Value) | Default | Description
--------- | ------------ | ------- | -----------
object | string | null | Main condition request.
id | string | null | The ID of the lot to retrieve.
content | string (data,map) | data | If not null, the result will filter with this parameter.

<aside class="success">
e.g : http://api.trees.id/?object=lot&id=6630
</aside>
<aside class="success">
e.g Map : http://api.trees.id/?object=lot&id=6630&content=map
</aside>

## Get a Statistik Lot


> The code beside returns JSONP structured like this:

```json
{
    "success": 1,
    "message": "Record(s) Found",
    "total_pohon": 256543166,
    "total_lot": 51925,
    "total_relawan": 562,
    "total_desa": 1480,
    "total_petani": 33235,
    "total_verifikator": 16
}
```

This endpoint retrieves a statistik lot.


### HTTP Request

`GET http://api.trees.id/statistik`


# Blocks

## Get All Blocks With Filter (Archive)


> The code beside returns JSONP structured like this:

```json
{
    "success": 1,
    "message": "Record(s) Found",
    "totalCount": 1649,
    "totalPage": 1649,
    "perPage": "1",
    "data": [
        {
            "id_block": 3,
            "nama_block": "CIKAWAO",
            "url_block": "cikawao",
            "kordinat": [
                {
                    "lat": "-7.133366",
                    "lng": "107.735847"
                }
            ],
            "kordinat_center": {
                "lat": "-7.133366",
                "lng": "107.735847"
            },
            "img_block": "http:\/\/api.trees.id\/images\/blocks\/00\/000\/000\/003\/31.png"
        }
    ]
}
```

This endpoint retrieves all blocks and condition/filter.

### HTTP Request

`GET http://api.trees.id/?object=block`

### URL Parameters

Parameter | Type (Value) | Default | Description
--------- | ------------ | ------- | -----------
object | string | null | Main condition request.
search | string | null | If not null, the result will filter with this parameter.
program_id | int | null | If not null, the result will filter with this parameter.
project_id | int | null | If not null, the result will filter with this parameter.
provinsi_id | int | null | If not null, the result will filter with this parameter.
kecamatan_id | int | null | If not null, the result will filter with this parameter.
content | string (data,name) | data | If not null, the result will filter with this parameter.
per_page | int | 6 | Total result per request.

<aside class="success">
e.g : http://api.trees.id/?object=block&search=cik
</aside>
<aside class="success">
e.g Name : http://api.trees.id/?object=block&search=cik&content=name
</aside>


## Get a Specific Block (Single)


> The code beside returns JSONP structured like this:

```json
{
    "success": 1,
    "message": "Record(s) Found",
    "totalCount": 1,
    "totalPage": 1,
    "perPage": 1,
    "data": [
        {
            "id_block": 51,
            "nama_block": "Cikemulan ",
            "url_block": "cikemulan",
            "img_block": null,
            "district": null,
            "regency": null,
            "province": null,
            "totalPage": 1,
            "perPage": 6,
            "list_lot": [
                {
                    "id_lot": 1088,
                    "nama_lot": "Cikemulan 1",
                    "url_lot": "cikemulan-1",
                    "img_lot": null
                }
            ]
        }
    ]
}
```

This endpoint retrieves a specific block.


### HTTP Request

`GET http://api.trees.id/?object=block&id=<ID>`

### URL Parameters

Parameter | Type (Value) | Default | Description
--------- | ------------ | ------- | -----------
object | string | null | Main condition request.
id | string | null | The ID of the block to retrieve.
content | string (data,map) | data | If not null, the result will filter with this parameter.
per_page | int | 6 | Total result lot per request.

<aside class="success">
e.g : http://api.trees.id/?object=block&id=3
</aside>
<aside class="success">
e.g Map : http://api.trees.id/?object=block&id=3&content=map
</aside>

## Get All Districts With Filter (Archive)

This endpoint retrieves all districts and condition/filter.

### HTTP Request

`GET http://api.trees.id/?object=kecamatan&content=name`

### URL Parameters

Parameter | Type (Value) | Default | Description
--------- | ------------ | ------- | -----------
object | string | null | Main condition request.
search | string | null | If not null, the result will filter with this parameter.
provinsi_id | int | null | If not null, the result will filter with this parameter.
content | string (name) | data | Must set as name.


# Projects

## Get All Projects With Filter (Archive)


> The code beside returns JSONP structured like this:

```json
{
    "success": 1,
    "message": "Record(s) Found",
    "totalCount": 8,
    "totalPage": 8,
    "perPage": "1",
    "data": [
        {
            "id_project": 1,
            "nama_project": "Patra Kartika Sobatbumi",
            "url_project": "bakti-sosial-tni-ad-pkbl-pertamina",
            "img_project": "http:\/\/api.trees.id\/images\/projects\/00\/000\/000\/001\/logo1d.png",
            "total_pohon": 20028356,
            "total_relawan": 322,
            "total_desa": 485,
            "total_petani": 6122,
            "total_lot": 7325
        }
    ],
    "agregat_tree": 106060340,
    "agregat_lot": 35211,
    "agregat_relawan": 477,
    "agregat_desa": 1232,
    "agregat_petani": 23785,
    "agregat_verifikator": 12
}
```

This endpoint retrieves all projects and condition/filter.

### HTTP Request

`GET http://api.trees.id/?object=project`

### URL Parameters

Parameter | Type (Value) | Default | Description
--------- | -----------  | ------- | -----------
object | string | null | Main condition request.
search | string | null | If not null, the result will filter with this parameter.
program_id | int | null | If not null, the result will filter with this parameter.
content | string (data,name) | data | If not null, the result will filter with this parameter.
per_page | int | 6 | Total result per request.

<aside class="success">
e.g : http://api.trees.id/?object=project&search=c
</aside>

## Get a Specific Project (Single)


> The code beside returns JSONP structured like this:

```json
{
    "success": 1,
    "message": "Record(s) Found",
    "totalCount": 1,
    "totalPage": 1,
    "perPage": 1,
    "data": [
        {
            "id_project": 4,
            "nama_project": "CSR Pertamina 17 juta pohon 2013",
            "url_project": "csr-pertamina-2013-2",
            "img_project": "http:\/\/api.trees.id\/images\/projects\/00\/000\/000\/004\/csrpertamina21.jpg",
            "total_pohon": 16917083,
            "total_relawan": 27,
            "total_desa": 100,
            "total_petani": 2980,
            "total_lot": 3936,
            "totalPage": 656,
            "perPage": 6,
            "list_lot": [
                {
                    "id_lot": 1670,
                    "nama_lot": "Bendosari-4",
                    "url_lot": "bendosari-4",
                    "img_lot": "http:\/\/api.trees.id\/images\/lots\/00\/000\/001\/670\/Bendosari-44.jpg",
                    "img_petani": null
                },
                {
                    "id_lot": 1932,
                    "nama_lot": "Balokang",
                    "url_lot": "balokang",
                    "img_lot": "http:\/\/api.trees.id\/images\/lots\/00\/000\/001\/932\/balokang.jpg",
                    "img_petani": "http:\/\/api.trees.id\/images\/users\/00\/000\/004\/348\/IMG-20121231-01516.jpg"
                },
                {
                    "id_lot": 1972,
                    "nama_lot": "PASIRLENGUT23",
                    "url_lot": "pasirlengut23",
                    "img_lot": "http:\/\/api.trees.id\/images\/lots\/00\/000\/001\/972\/1.jpg",
                    "img_petani": "http:\/\/api.trees.id\/images\/users\/00\/000\/002\/429\/juju-karma1.jpg"
                },
                {
                    "id_lot": 1973,
                    "nama_lot": "CIBINONG7",
                    "url_lot": "cibinong7",
                    "img_lot": "http:\/\/api.trees.id\/images\/lots\/00\/000\/001\/973\/2.jpg",
                    "img_petani": "http:\/\/api.trees.id\/images\/users\/00\/000\/002\/430\/FP12.jpg"
                },
                {
                    "id_lot": 1975,
                    "nama_lot": "PASIRDATAR1",
                    "url_lot": "pasirdatar1",
                    "img_lot": "http:\/\/api.trees.id\/images\/lots\/00\/000\/001\/975\/7.jpg",
                    "img_petani": "http:\/\/api.trees.id\/images\/users\/00\/000\/002\/432\/asep-yudha-72x72.jpg"
                },
                {
                    "id_lot": 1976,
                    "nama_lot": "MARIUK\/PASIR MATUH",
                    "url_lot": "mariukpasir-matuh",
                    "img_lot": "http:\/\/api.trees.id\/images\/lots\/00\/000\/001\/976\/8.jpg",
                    "img_petani": "http:\/\/api.trees.id\/images\/users\/00\/000\/002\/433\/yayat.jpg"
                }
            ]
        }
    ]
}
```

This endpoint retrieves a specific project.


### HTTP Request

`GET http://api.trees.id/?object=project&id=<ID>`

### URL Parameters

Parameter | Type (Value) | Default | Description
--------- | ------------ | ------- | -----------
object | string | null | Main condition request.
id | string | null | The ID of the project to retrieve.
content | string (data,map) | data | If not null, the result will filter with this parameter.
per_page | int | 6 | Total result lot per request.

<aside class="success">
e.g : http://api.trees.id/?object=project&id=1
</aside>
<aside class="success">
e.g Map : http://api.trees.id/?object=project&id=1&content=map
</aside>

# Programs

## Get All Programs With Filter (Archive)


> The code beside returns JSONP structured like this:

```json
{
    "success": 1,
    "message": "Record(s) Found",
    "totalCount": 2,
    "totalPage": 1,
    "perPage": 6,
    "data": [
        {
            "id_program": 1,
            "nama_program": "Persembahan relawan GMP untuk pertamina",
            "url_program": "pertamina",
            "img_program": "http:\/\/api.trees.id\/images\/programs\/00\/000\/000\/001\/featured-project2.jpg"
        },
        {
            "id_program": 2,
            "nama_program": "Nusantara Recovery",
            "url_program": "nusantara-recovery",
            "img_program": "http:\/\/api.trees.id\/images\/programs\/00\/000\/000\/002\/banneindonesia-recovery3.jpg"
        }
    ]
}
```

This endpoint retrieves all programs and condition/filter.

### HTTP Request

`GET http://api.trees.id/?object=program`

### URL Parameters

Parameter | Type (Value) | Default | Description
--------- | -----------  | ------- | -----------
object | string | null | Main condition request.
search | string | null | If not null, the result will filter with this parameter.
content | string (data,name) | data | If not null, the result will filter with this parameter.
per_page | int | 6 | Total result per request.

<aside class="success">
e.g : http://api.trees.id/?object=program&search=c
</aside>

## Get a Specific Program (Single)


> The code beside returns JSONP structured like this:

```json
{
    "success": 1,
    "message": "Record(s) Found",
    "totalCount": 1,
    "totalPage": 1,
    "perPage": 1,
    "data": [
        {
            "id_program": 2,
            "nama_program": "Nusantara Recovery",
            "url_program": "nusantara-recovery",
            "img_program": "http:\/\/api.trees.id\/images\/programs\/00\/000\/000\/002\/banneindonesia-recovery3.jpg",
            "total_pohon": 144800508,
            "total_relawan": 130,
            "total_desa": 375,
            "total_petani": 7748,
            "total_lot": 17437,
            "totalPage": 8719,
            "perPage": "2",
            "list_lot": [
                {
                    "id_lot": 1,
                    "nama_lot": "Mekarjaya 25",
                    "url_lot": "mekarjaya-25",
                    "img_lot": "http:\/\/api.trees.id\/images\/lots\/00\/000\/000\/001\/Mekarjaya-25.jpg"
                },
                {
                    "id_lot": 2,
                    "nama_lot": "Mekarjaya 26",
                    "url_lot": "mekarjaya-26",
                    "img_lot": "http:\/\/api.trees.id\/images\/lots\/00\/000\/000\/002\/Mekarjaya-26.jpg"
                }
            ]
        }
    ]
}
```

This endpoint retrieves a specific program.


### HTTP Request

`GET http://api.trees.id/?object=program&id=<ID>`

### URL Parameters

Parameter | Type (Value) | Default | Description
--------- | ------------ | ------- | -----------
object | string | null | Main condition request.
id | string | null | The ID of the program to retrieve.
content | string (data,map) | data | If not null, the result will filter with this parameter.
per_page | int | 6 | Total result lot per request.

<aside class="success">
e.g : http://api.trees.id/?object=program&id=1
</aside>
<aside class="success">
e.g Map : http://api.trees.id/?object=program&id=1&content=map
</aside>


# Users

## Get All Users With Filter (Archive)


> The code beside returns JSONP structured like this:

```json
{
    "success": 1,
    "message": "Record(s) Found",
    "totalCount": 761,
    "totalPage": 254,
    "perPage": "3",
    "data": [
        {
            "id_user": 2,
            "nama_user": "KSBL ",
            "img_user": "http:\/\/api.trees.id\/images\/users\/00\/000\/000\/002\/ksbl.jpg"
        },
        {
            "id_user": 3,
            "nama_user": "cvtuturubus",
            "img_user": null
        },
        {
            "id_user": 4,
            "nama_user": "dedi_suryadi",
            "img_user": null
        }
    ]
}
```

This endpoint retrieves all users and condition/filter.

### HTTP Request

`GET http://api.trees.id/?object=user`

### URL Parameters

Parameter | Type (Value) | Default | Description
--------- | ------------ | ------- | -----------
object | string | null | Main condition request.
search | string | null | If not null, the result will filter with this parameter.
role | (petani, relawan, verifikator, pemiliklahan, investor) | null | List Role.
content | (data, name) | data | If not null, the result will filter with this parameter.
per_page | int | 6 | Total result per request.

<aside class="success">
e.g : http://api.trees.id/?object=user&role=relawan
</aside>

## Get a Specific User (Single)


> The code beside returns JSONP structured like this:

```json
{
    "success": 1,
    "message": "Record(s) Found",
    "totalCount": 1,
    "totalPage": 1,
    "perPage": 1,
    "data": [
        {
            "id_user": 2,
            "nama_user": "KSBL ",
            "img_user": "http:\/\/api.trees.id\/images\/users\/00\/000\/000\/002\/ksbl.jpg",
            "total_pohon": 706105,
            "total_petani": 225,
            "total_lot": 233,
            "totalPage": 78,
            "perPage": "3",
            "list_lot": [
                {
                    "id_lot": 1,
                    "nama_lot": "Mekarjaya 25",
                    "url_lot": "mekarjaya-25",
                    "img_lot": "http:\/\/api.trees.id\/images\/lots\/00\/000\/000\/001\/Mekarjaya-25.jpg"
                },
                {
                    "id_lot": 2,
                    "nama_lot": "Mekarjaya 26",
                    "url_lot": "mekarjaya-26",
                    "img_lot": "http:\/\/api.trees.id\/images\/lots\/00\/000\/000\/002\/Mekarjaya-26.jpg"
                },
                {
                    "id_lot": 3,
                    "nama_lot": "Mekarjaya 27",
                    "url_lot": "mekarjaya-27",
                    "img_lot": "http:\/\/api.trees.id\/images\/lots\/00\/000\/000\/003\/Mekarjaya-27.jpg"
                }
            ]
        }
    ]
}
```

This endpoint retrieves a specific user.


### HTTP Request

`GET http://api.trees.id/?object=user&id=<ID>`

### URL Parameters

Parameter | Type/Value | Default | Description
--------- | ---- | ------- | -----------
object | string | null | Main condition request.
id | string | null | The ID of the user to retrieve.
content | string (data,name) | data | If not null, the result will filter with this parameter.
per_page | int | 6 | Total result lot per request.

<aside class="success">
e.g : http://api.trees.id/?object=user&id=2
</aside>
<aside class="success">
e.g Name : http://api.trees.id/?object=id&id=2&content=name
</aside>

# Trees

## Get All trees With Filter (Archive)


> The code beside returns JSONP structured like this:

```json
{
    "success": 1,
    "message": "Record(s) Found",
    "totalCount": 3069,
    "totalPage": 1535,
    "perPage": "2",
    "data": [
        {
            "id_tree": 1,
            "nama_tree": "PohonImut",
            "nama_lot": "Go Hitzz",
            "nama_donatur": "Mutia",
            "hp_donatur": "087885118929",
            "email_donatur": null,
            "twitter_donatur": null,
            "tree_offset": 1,
            "code": null,
            "img_tree": "http:\/\/api.trees.id\/tree\/14661\/25654\/000001.jpg"
        },
        {
            "id_tree": 2,
            "nama_tree": "SENGON",
            "nama_lot": "Go Hitzz",
            "nama_donatur": "Rony",
            "hp_donatur": "0",
            "email_donatur": null,
            "twitter_donatur": null,
            "tree_offset": 2,
            "code": null,
            "img_tree": "http:\/\/api.trees.id\/tree\/14661\/25654\/000002.jpg"
        }
    ]
}
```

This endpoint retrieves all trees and condition/filter.

### HTTP Request

`GET http://api.trees.id/?object=trees`

### URL Parameters

Parameter | Type (Value) | Default | Description
--------- | ------------ | ------- | -----------
object | string | null | Main condition request.
lot_id | int | null | If not null, the result will filter with this parameter.
donatur_email | string | null | If not null, the result will filter with this parameter.
per_page | int | 6 | Total result per request.

<aside class="success">
e.g : http://api.trees.id/?object=user&role=relawan
</aside>

## Get a Specific Tree (Single By Tree Code)


> The code beside returns JSONP structured like this:

```json
{
    "success": 1,
    "message": "Record(s) Found",
    "totalCount": 1,
    "totalPage": 1,
    "perPage": 6,
    "data": [
        {
            "id_code": 2,
            "code_lot": 56991,
            "status_used": 1,
            "used_at": "2014-12-17",
            "id_tree": 3123,
            "nama_lot": "Sarakan Sari-38",
            "nama_tree": "test",
            "nama_donatur": "test",
            "hp_donatur": "0893219391",
            "email_donatur": "test@gmail.com",
            "twitter_donatur": null,
            "tree_offset": 3,
            "tree_offset_now": null,
            "code": "E8432RXD1U",
            "img_tree": "http:\/\/twitgreen.local\/tree\/25900\/56991\/000008.jpg"
        }
    ]
}
```

This endpoint retrieves a specific tree by tree_code.


### HTTP Request

`http://api.trees.id/?object=tree&tree_code=<code>`

### URL Parameters

Parameter | Type (Value) | Default | Description
--------- | ------------ | ------- | -----------
object | string | null | Main condition request.
tree_code | string | null | The code for reedim tree.

<aside class="success">
e.g : http://api.trees.id/?object=tree&tree_code=E8432RXD1U
</aside>


## Get a Specific Tree (Single By ID)

> The code beside returns JSONP structured like this:

```json
{
    "success": 1,
    "message": "Record(s) Found",
    "totalCount": 1,
    "totalPage": 1,
    "perPage": 6,
    "data": [
        {
            "id_tree": 3131,
            "nama_tree": "Ega Oktiviani",
            "nama_lot": "Cipanjalu2",
            "nama_donatur": "DNR",
            "hp_donatur": "0085795111943",
            "email_donatur": null,
            "twitter_donatur": null,
            "tree_offset": 184,
            "code": null,
            "img_tree": "http:\/\/api.trees.id\/tree\/48592\/52718\/000184.jpg"
        }
    ]
}
```

This endpoint retrieves a specific tree by ID.


### HTTP Request

`http://api.trees.id/?object=tree&single_id=<ID>`

### URL Parameters

Parameter | Type (Value) | Default | Description
--------- | ------------ | ------- | -----------
object | string | null | Main condition request.
id | string | null | The ID of the tree to retrieve.

<aside class="success">
e.g : http://api.trees.id/?object=tree&tree_code=E8432RXD1U
</aside>

## Naming Tree (POST)

> The code beside returns JSON structured like this:

```json
{
    "status":"success",
    "link_pohon":"http:\/\/domain.com\/tree-view-new\/10\/9",
    "image_path":"http:\/\/domain.com\/tree\/3602\/4012\/000009.jpg",
    "title":"Dummy",
    "name":"dummy-1"
}
```

This endpoint use for naming tree on lot.


### Shell Request

`curl --data '{"title": "<name tree>","name_donation": "<author>","no_hp_donation": "<no>","email": "<email>","lot_id": "<ID Lot>","app_key": "<app_key>","app_id": "<app_id>"}' http://api.trees.id/api/tree`

### Shell Parameters

Parameter | Type (Value) | Status | Description
--------- | ------------ | ------- | -----------
title | string | required | Name of tree.
name_donation | string | required | Name author.
no_hp_donation | string | required | Number Telp author.
email | string | required | Email of author.
lot_id | int | required | ID Lot for tree.
app_key | string | required | APP Key.
app_id | int | required | APP ID.


## Redeem Tree (POST)

> The code beside returns message succes or error.


This endpoint use for redeem tree on lot.


### URL Request Post

`POST http://api.trees.id/redeem-tree`

<aside class="notice">
Sent post data to url above.
</aside>

### Post Data Parameter

Name | Type (Value) | Status | Description
--------- | ------------ | ------- | -----------
Tree[title] | string | required | Name of tree.
Tree[code] | string | required | Code Tree.
Tree[name_donation] | string | required | Name author.
Tree[no_hp_donation] | string | required | Number Telp author.
Tree[email] | string | required | Email of author.
