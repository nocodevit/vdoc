---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
nav_order: 2
permalink: /format/
---

# Message Format
{: .no_toc}

## Table of contents
{: .no_toc .text-delta}

1. TOC
{:toc}


## Request

| Parameter   | Is Required | Descriptions/ Remarks |
|:------------|:------------|:----------------------|
| version     | Yes         | 2.0                   |
| access_code | Yes         | Used to verfiy the identity of the api caller. Format is `p` followed by 6 digits, such as `p00001` . please contact support@linksfield.net to apply for access_code|
| timestamp   | Yes         | UTC timestamp of the request. Timetout = 5 minutes |
| sign        | Yes         | Signature of the message |

```json
//sample code 
    {
        "version": "2.0",
        "access_code" : "P000009",
        "timestamp": "1493893791",
        "page_no" : 1,
        "page_size" : 3,
        "month" : "201808",
        "sign" : "sF4hFI390weingeseionglts="
    }

```

## Response

| Parameter   | Is Required | Descriptions/ Remarks |
|:------------|:------------|:----------------------|
| code        | Yes         | `0000` means success  |
| data        | Yes         | Response data         |
| sign        | Yes         | Signature of data     |
| message     | Yes         | Response message      |


```json
//sample code 
    {
        "code": "0000",
        "data" : 
        {
            "device_flow": [
            {
                "device_id" : "88888888888888",
                "flow"      : 30.00
            },
            {
                "device_id" : "88888888888889",
                "flow"      : 54.30
            }
            ],
            "devide_flow_list_num": 2,
            "page" : {
                "cur_page_no" : 1,
                "page_size"   : 3,
                "total_count" : 2,
                "total_pages" : 1
            },
            "sign" : "3sesierngnaooadioancc="
        },
        "message" : "成功"
    }

```
