# Login ( PushOtp)

برای درخواست کد یک بار مصرف از این سرویس استفاده کنید. دقت کنید برای بار دوم پس از  پنج دقیقه  میتوانید درخواست کد یکبارمصرف را  تکرار کنید

رمز یکبار مصرف از طریق پیامک برای شماره وارد شده ارسال خواهد شد.
**URL** : `/otp/request/`

**Method** : `POST`

**Content-Type**: `x-www-form-urlencoded`

**Params** : `mobile`

**در بدنه رکوئست پارامتر ها به صورت فرم و مشابه فرمت زیر ارسال شوند**:

**RequestBody**: 

```
mobile=09123456789
```

**Request Headers (optional, but recommended)**:
```
    x-log-app: com.example.package
    x-log-app-version: 1.2
    x-log-os: android
    x-log-os-version: 1.4
    x-log-device: Samsung Galaxy S9
    x-log-campaign: norooz99,
    x-log-landing: internet6GB
```

**Send Everything you want to log, as a header with 'x-log-' prefix **

## Success Response

در صورتی که درخواست غیرمجاز نباشد و عملیات موفقیت آمیز به پایان برسد، پاسخی به شکل عبارت زیر دریافت خواهید کرد

** Code ** : `200 OK`

```json
{
    "status": true,
    "message": "otp sent"
}
```

در صورتی که پاسخی به شکل زیر دریافت شود، خطایی در زمان بندی استفاده از وب سرویس رخ داده است، و بهتر است برای اطلاعات بیشتر با پشتیبانی ارتباط برقرار کنید

```json
{
    "status": false,
    "message": "Too Many Tries! Try Later."
}
```

## ERROR Response

درحالتی که درخواست غیرمجاز باشد و پارامترهای ارسالی به وب سرویس نیاز به بررسی داشته باشند، متن پیام خطا برگردانده میشود
** Code ** : `200 OK`
`Invalid Request`



* [Verification](chargeOtp.md) `POST /otp/charge`
