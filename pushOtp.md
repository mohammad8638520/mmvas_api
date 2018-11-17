# Login ( PushOtp)

برای درخواست کد یک بار مصرف از این سرویس استفاده کنید. دقت کنید برای بار دوم پس از  پنج دقیقه  میتوانید درخواست کد یکبارمصرف را  تکرار کنید


**URL** : `/otp/request/`

**Method** : `POST`

**Params** : `mobile`
        mobile number : 09xxxxxxxxx

## Response

```json
{
    "status": true / false,
    "message": "otp sent" / "error message"
}
```


