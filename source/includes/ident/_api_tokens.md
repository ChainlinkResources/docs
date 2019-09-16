# API Tokens

## List API Tokens

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiaWF0IjoxNTY4NTI3NDk2LCJqdGkiOiIxMzIxYTNjNi0yZTk5LTQ0OGYtYjcwNy1hZWMwMDY2MzkwZDkiLCJzdWIiOiJhcHBsaWNhdGlvbjpkYzQxNTJmNy00NTZmLTQxZWQtOTZiNC1lNTJiOGZhYTA1ZmQifQ.olwBIJweWDGmzcQZhWfzyx8oUm-0ewGihk-nuRcG4aMxNtMACNkclPpnveTqyi7J5t2JZgaopwfvznCj4JvLM823Vo2JGlP7uxSgdpywVKAIg3l8vFHGpsDEaLXUPBEdXfyp6DvtbTPhd2NYSYNPjkgavJ1ECGs0E4OTIqOeTylrU73ZiNs6dDOhT3ZRAz8zn1mNB4f3CzjQ6lcEs6w0KremPUw5xf0VZo1-aJ_HzYYWzCk-jodV6jojnFH0hEKVKx02Ephy7PGf703G01jycuTsTvOVmAaa-plAO7RZUFaqzYOrbRE2hR3Ih3KnvQdUBabeObYGfvmpcHFCXrsCM3Qf931sXrVdhkCrgveIU7ilqord1mefmYB-_8tpL7tT3Aeo0dKVCWxsQdzsCSd4BBQmvWCt0nzVsLMEJhR6MKdedmrS8YnfXqaa3a1uMPWP1nks7zrOL464eC7tD3u7Og119kFNohtRSLfqCy_9OKbSOosdEszuVOxBqcqzwtkdvaGYohx13HxLdiRoelObUFEPokkv1LkTEEG_zmoYTbqQOG-pUeAoheReZFUlTUTc3uSPa9vho0BjFHO_sUK9jDwqHWXpdkRiDDAzF2laCINx5MLoA5pnco_J7NlFP7mXd0FldM5CSBEO8aymlJ-0v-jaZ_wuDAl5fp84qPGWM8A' \
    https://ident.provide.services/api/v1/tokens
HTTP/2 200
```

> Response JSON:

```json
[
  {
        "id": "234da41d-0970-4561-bdf9-797ef6807fb5",
        "created_at": "2018-10-08T23:34:18.843828Z",
        "issued_at": "2018-10-08T23:34:18.842733Z",
        "expires_at": null,
        "token": "eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiaWF0IjoxNTY4NTI3NDk2LCJqdGkiOiIxMzIxYTNjNi0yZTk5LTQ0OGYtYjcwNy1hZWMwMDY2MzkwZDkiLCJzdWIiOiJhcHBsaWNhdGlvbjpkYzQxNTJmNy00NTZmLTQxZWQtOTZiNC1lNTJiOGZhYTA1ZmQifQ.olwBIJweWDGmzcQZhWfzyx8oUm-0ewGihk-nuRcG4aMxNtMACNkclPpnveTqyi7J5t2JZgaopwfvznCj4JvLM823Vo2JGlP7uxSgdpywVKAIg3l8vFHGpsDEaLXUPBEdXfyp6DvtbTPhd2NYSYNPjkgavJ1ECGs0E4OTIqOeTylrU73ZiNs6dDOhT3ZRAz8zn1mNB4f3CzjQ6lcEs6w0KremPUw5xf0VZo1-aJ_HzYYWzCk-jodV6jojnFH0hEKVKx02Ephy7PGf703G01jycuTsTvOVmAaa-plAO7RZUFaqzYOrbRE2hR3Ih3KnvQdUBabeObYGfvmpcHFCXrsCM3Qf931sXrVdhkCrgveIU7ilqord1mefmYB-_8tpL7tT3Aeo0dKVCWxsQdzsCSd4BBQmvWCt0nzVsLMEJhR6MKdedmrS8YnfXqaa3a1uMPWP1nks7zrOL464eC7tD3u7Og119kFNohtRSLfqCy_9OKbSOosdEszuVOxBqcqzwtkdvaGYohx13HxLdiRoelObUFEPokkv1LkTEEG_zmoYTbqQOG-pUeAoheReZFUlTUTc3uSPa9vho0BjFHO_sUK9jDwqHWXpdkRiDDAzF2laCINx5MLoA5pnco_J7NlFP7mXd0FldM5CSBEO8aymlJ-0v-jaZ_wuDAl5fp84qPGWM8A",
        "data": null
    },
    {
        "id": "84557020-0180-4e87-ae01-ffa05a587df4",
        "created_at": "2018-10-08T23:58:28.631901Z",
        "issued_at": "2018-10-08T23:58:28.630644Z",
        "expires_at": null,
        "token": "eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiaWF0IjoxNTY4NjE4OTQzLCJqdGkiOiI5NDRjOGMxNC00N2E4LTRhNGEtYWU0MS1kYWQxZmZjNzNlN2IiLCJzdWIiOiJhcHBsaWNhdGlvbjpkYzQxNTJmNy00NTZmLTQxZWQtOTZiNC1lNTJiOGZhYTA1ZmQifQ.gFJhOWJn6KLNOyugFkKCY9OM3MuUrDLetYw_zMmsyQilyrWcIB_pEhccUP14K6GKMMd74AwUUTbTxSxg_QZJnJYOFnQAuvO8vxoRW1izALqaqxhViZlZN09qseeQ0i0eb7rThyWSzQwXgKwRdqpQwGIVsfnXW-_xbPPdATJaKD4bAVo97AhCIzZblfctjZMsgzFNEV2fbHSQMCqeWAvm1b_cNn7N9yJJX8QMdniPHoa9TgF80nDNOmvx9blldn8niPwhifhBOL6sq5DhFY6v2n28OktOSqqclG6OjYag2zPsM7m3PMO1z2Rwv8JfkS4tMqHuKeyQNLaTX2XLAtfsxzEAH4ywhnKq6Pwad2YqDQmWprTs-R9A_ukdHcRoPv0-qjJWWQTH6cCK1x9x3C7bZHZ_Sxc2Z2bLnnrGelKtk6I8Zvrq4djsA0yyjTwW0VjnH7UHFj1z1t4B3UvVfLOl-7d3amueoiiyFmq-38fHgBRQcnRl-LQRUYefX66Qh9yzmtCZH0u4Tk77ryYqmjp7tPuRB7w5vwQ9bndc-yLuEU67eKTuAFsODRPTcoHSh3aNKL3ZsuLn_Y4y1LXjI2KX1PHq-wjYZvVgAtK1Diy0M0tkgT0gLbh8gcRtdsw0GBpunbQK4JjJs3RK6xo73Sot9InE7Ic-hZiqnaMJoMD3qj8",
        "data": null
    }
]
```

This endpoint enumerates previously authorized Tokens for the authorized User or Application.


## Create API Token

```shell
curl -i -XPOST \
    -H 'content-type: application/json' \
    -H 'Authorization: bearer eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiaWF0IjoxNTY4NjE4OTQzLCJqdGkiOiI5NDRjOGMxNC00N2E4LTRhNGEtYWU0MS1kYWQxZmZjNzNlN2IiLCJzdWIiOiJhcHBsaWNhdGlvbjpkYzQxNTJmNy00NTZmLTQxZWQtOTZiNC1lNTJiOGZhYTA1ZmQifQ.gFJhOWJn6KLNOyugFkKCY9OM3MuUrDLetYw_zMmsyQilyrWcIB_pEhccUP14K6GKMMd74AwUUTbTxSxg_QZJnJYOFnQAuvO8vxoRW1izALqaqxhViZlZN09qseeQ0i0eb7rThyWSzQwXgKwRdqpQwGIVsfnXW-_xbPPdATJaKD4bAVo97AhCIzZblfctjZMsgzFNEV2fbHSQMCqeWAvm1b_cNn7N9yJJX8QMdniPHoa9TgF80nDNOmvx9blldn8niPwhifhBOL6sq5DhFY6v2n28OktOSqqclG6OjYag2zPsM7m3PMO1z2Rwv8JfkS4tMqHuKeyQNLaTX2XLAtfsxzEAH4ywhnKq6Pwad2YqDQmWprTs-R9A_ukdHcRoPv0-qjJWWQTH6cCK1x9x3C7bZHZ_Sxc2Z2bLnnrGelKtk6I8Zvrq4djsA0yyjTwW0VjnH7UHFj1z1t4B3UvVfLOl-7d3amueoiiyFmq-38fHgBRQcnRl-LQRUYefX66Qh9yzmtCZH0u4Tk77ryYqmjp7tPuRB7w5vwQ9bndc-yLuEU67eKTuAFsODRPTcoHSh3aNKL3ZsuLn_Y4y1LXjI2KX1PHq-wjYZvVgAtK1Diy0M0tkgT0gLbh8gcRtdsw0GBpunbQK4JjJs3RK6xo73Sot9InE7Ic-hZiqnaMJoMD3qj8' \
    https://ident.provide.services/api/v1/tokens \
    -d '{"name": "PurposeToken"}'
HTTP/2 201
```

> Response JSON:

```json
[
  {
    "id": "ed3d83ec-8b4f-4538-a240-bf759a2545ff",
    "created_at": "2018-10-09T02:47:25.981937848Z",
    "issued_at": "2018-10-09T02:47:25.980910555Z",
    "expires_at": null,
    "token": "eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiaWF0IjoxNTY4NjE4OTgzLCJqdGkiOiIyOGY4OGFmNS04ZjVlLTQ0YjQtOTQwNS1hOGJhZjVhYmM1OGUiLCJzdWIiOiJhcHBsaWNhdGlvbjpkYzQxNTJmNy00NTZmLTQxZWQtOTZiNC1lNTJiOGZhYTA1ZmQifQ.Yztl5-4NumplTSzhzRyAsb2bQb0FqHntQXMjUClsAFfhXUQ_WuQlFkVOl8ZTuu5usYiNwy11OAN4ie6Ht3lN8bUHs5B2k1FuKrSGZRdz-IhWfFLKbW9E7yobdkt7ESToJBC2Qg71_9ZlzEd7VdxzrAJQ_BHF8NP90JWZDSeJGVqGPRjZk_DTmnLlm_eDbp96ZvuiKzEgrn-V8dxem96jMxAJSufGdxYSn_tSzDpKihfy0l4wChJ8ZfA5D-eOliZjgU-cXGsNlizTdHWqeXWtGMuraRvjupHHwx7UMPgLLZKle7FjU8s45o4N7QgX14bCehRSU5XcD7RlTQLtaXtpTT6ME5eMIxVt7pKHk0EWj1JTLCN6cGpjZc_RQkjePwkpnTmRwk1q0R66nccUikaqCdgk8YdXcQiNcrNLUQJs21HQyD-sIdiF1tzMeb6NlMWchyzSNqJ0EYhOZ8tYpQtOPQyc9Tqbp75jPFShOgr6dhj-2Ee6hsPAYSb_NAl4uyGk-b5PhDpzqbkGm5TX8VaA_DvJF80mPkM-21h0CKg9cEx32Q0ynTBWU3AfSZzB0_w-OJ4rphHw7i-gXjbnQgeLvjwBp_8s01ykuqKDbw0Y4V-xaiTeI2lwJrvJKIlJLsg6otXY8YNy4uFOA8tGT1Z0A1Wiq8Km4mIzlUO8lz-vCHY",
    "data": null
}
]
```

This endpoint authorizes a `Token` on behalf of a `User` or `Application`.


## Delete API Token

```shell
curl -i -XDELETE \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://ident.provide.services/api/v1/tokens/84557020-0180-4e87-ae01-ffa05a587df4
HTTP/2 204
```

This endpoint destroys a previously authorized `Token` on behalf of the authorized `User` or `Application`.

### URL Parameters

Parameter | Description
--------- | -----------
id | id of the `Token`
