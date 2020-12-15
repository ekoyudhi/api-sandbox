---
title: Autentikasi
position_number: 2
parameters:
  - name:
    content:
content_markdown: |-
  Anda membutuhkan autentikasi untuk memanggil API. Anda dapat men-generate ```API Key``` dan ```API Secret Key``` pada dasbor anda.

  Tambahkan ```API Key``` dan ```API Secret Key``` pada pada saat mengakses endpoint autentikasi untuk mendapatkan ```Token```. 
  
  ```Token``` akan dipakai pada setiap request ke endpoint URL (akses menggunakan ```Bearer Token```)

left_code_blocks:
  - code_block: |2-
      curl -u "YOUR_API_KEY:YOUR_API_SECRET_KEY" https://api.twitter.com/oauth2/token
    title: cURL
    language: bash
right_code_blocks:
  - code_block: |2-
      {
        "token_type": "bearer",
        "access_token": "AAAAAAAAAAAAAAAAAAAAAFQpwwAAAAAAJVx3Dsboo1opmVc1WMyw0qfj7fU%3DQN5MNkSM40tQnBa258xxYMdc8QfgRqkrqZHuru55AI3u12TGUP"
      }
    title: Response Success
    language: javascript
  - code_block: |2-
       {
          "errors": [
            {
                "code": 99,
                "message": "Unable to verify your credentials",
                "label": "authenticity_token_error"
            }
          ]
        }
    title: Response Error
    language: javascript
---