
# Check Subscription ( subscription/Check)

از این سرویس برای بررسی وضعیت عضویت کاربر در سرویس استفاده میشود.

دقت کنید پارامتر های شماره موبایل و توکن باید از طریق هدر ارسال شوند.


**URL** : `/subscription/check`


**Method** : `GET`


**Headers** : 
        
        `mobile` : "091xxxxxxx"
        `token` : "abcdefghijklmnopqrstuvwxyz"


## Success Response

درصورتی که عضویت کاربر در سرویس ، فعال باشد پاسخ زیر را دریافت می کنید :

** Code ** : `200 OK`


```json
{
    "active": true,
}
```
و در غیر اینصورت پاسخ این سرویس به صورت زیر خواهد بود :


```json
{
    "active": false
}
```

## ERROR Response

درحالتی که درخواست غیرمجاز باشد و پارامترهای ارسالی به وب سرویس نیاز به بررسی داشته باشند، متن پیام خطا برگردانده میشود

** Code ** : `200 OK`

`Invalid Request`



*[Unsubscribe](unsub.md) `POST /unsubscribe`
