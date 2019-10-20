# Authorization

Provide requires an API token to authorize the vast majority of platform requests. An API token is an encoded JWT and contains an identifier referencing the authorized entity as the subject (`sub`) in the claims. The encoded JWT token may also include an expiration (`exp`) and arbitrary data (`data`), among other standard JWT claims, and is signed using the `RS256` algorithm. The authorized entity (i.e., the `User` or `Application`) may use the signed `Token` to access one or more platform resources. Unless otherwise noted, all API requests must include a header such as: `Authorization: bearer <JWT>`.

The bearer `Authorization` header is scoped to an authorized platform `User` or an `Application` as described above.

> The encoded JWT is signed using the `RS256` (RSA Signature with SHA-256) algorithm. The following public key can be used to verify the signature:

```shell
-----BEGIN PUBLIC KEY-----
MIICIjANBgkqhkiG9w0BAQEFAAOCAg8AMIICCgKCAgEA0yqdJMBej1X8WwMMkMZw
DV6zZzup4RHLcln0xfGSm6dMPBDM1G96fuHhOwH5+uU5MQHJP7RqW71Bu5dLIG8Z
RX+XyUtb0sxCV/7X27Nm/bKpDysaSWQ36reAmw5wVaB1SoFeN519FY5rhoCWmH3W
auBAHTzpjg57p7uR0XynYXf8NSGXlysWHppkppqwrPH64G6UZaB7SMl1PFfkJeqZ
zJpzBGYWsixdF1EjXn+Yz0mhUZO2OSPWifOuN7cpn3BuNqegg4iVdz5HDoQhJW7N
uRhf3buKd/mjat8XA3e2Rkrr2h835GloScJkj7I4BZUNkzKQuEK6C9xW/zJtbPqQ
RYEq84A1hMfSZ3G5HFe2JkqiyvXkFwS3qMc5Pur8tZSzBj6AYMoJJso/aOdphpR8
6MaaWXWTwvwfpZbMRqehOcsmQcNLF2gLJPuHzR5WtVCnWrDgvjsWyeDD1WISKusi
aOeHxZjS3Bjl4Imq48l1wi2eI/11F/Xg70F4FJaMYLVHJA2nsmBuuQ9UDYHHq876
clKvIvgIItzJcv9lnmjl1Jks1DwCUF3qF2ugYcs9A3EoEcNzhMgZNJ2j5OUzfx1E
bzVKkqoC9MQpZWXgqV0KQqKK4I3rMY+1hLqk4S4eF9ZAVlT33qfMzlf0qWTOcP1Z
i2dsm0fy4NxWxknlEn5/LhMCAwEAAQ==
-----END PUBLIC KEY-----
```
