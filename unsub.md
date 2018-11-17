# UnSubscribe User ( unsubscribe)

از این سرویس برای لغو عضویت کاربر و خروج از سرویس استفاده میشود.

دقت کنید این سرویس، فعلا تنها برای سرویس های پیاده سازی شده در پلتفرم پردیس فعال است. البته برای پلتفرم های دیگر سرویس پاسخ مناسبی تولید خواهد کرد

دقت کنید پارامتر توکن باید از طریق هدر ارسال شود.


**URL** : `/unsubscribe`


**Method** : `POST`


**Headers** : 

        `token` : "abcdefghijklmnopqrstuvwxyz"


## Success Response

درصورت موفقیت آمیز بودن فرایند پاسخ زیر تولید میشود

** Code ** : `200 OK`


```json
{
    "status": true,
    "message" : "Subscription Removed"
}
```

و در غیر اینصورت پاسخی مشابه زیر همراه با متن خطا دریافت خواهید کرد


```json
{
    "status": true,
    "message" : "Invalid Token"
}
```

## ERROR Response

درحالتی که درخواست غیرمجاز باشد و پارامترهای ارسالی به وب سرویس نیاز به بررسی داشته باشند، متن پیام خطا برگردانده میشود

** Code ** : `200 OK`

`Invalid Request`
