
# Verification ( ChargeOtp)

از این سرویس برای تایید کد یکبارمصرف و دریافت توکن اختصاصی سرویس ارزش افزوده، استفاده میشود.

رمز یکبار مصرف از طریق پیامک برای شماره وارد شده ارسال خواهد شد.

**URL** : `/otp/charge`


**Method** : `POST`


**Params** : 
        
        `mobile`
        
                mobile number : 09xxxxxxxxx
        
        `pin`
        
                otp pin : 1762


## Success Response

در صورتی که کد یکبارمصرف ورود، به درستی وارد شده باشد، پاسخی به شکل عبارت زیر دریافت خواهید کرد
و باید مقدار برگشتی توکن را در اپلیکیشن یا دیتابیس خود برای این کاربر ذخیره کنید
برای چک کردن وضعیت عضویت کاربر در زمان های دیگر به این توکن نیاز خواهید داشت


** Code ** : `200 OK`


```json
{
    "status": true,
    "token": "abcdefghijklmnop-ABCDEFGHIJKLM-123456789",
    "message": ""
}
```

در صورتی که کد وارد شده نادرست باشد، پیامی مشابه زیر دریافت میکنید


```json
{
    "status": false,
    "token": null,
    "message": "کد وارد شده نادرست است"
}
```

## ERROR Response

درحالتی که درخواست غیرمجاز باشد و پارامترهای ارسالی به وب سرویس نیاز به بررسی داشته باشند، متن پیام خطا برگردانده میشود

** Code ** : `200 OK`

`Invalid Request`



*[Check Subscription](checkSub.md) `GET /subcription/check`