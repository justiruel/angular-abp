# angular-abp
## setting awal angular-abp
### yarn install
### Buka D:\PROJECT\RISET\aspnetboilerplate\GITHUB\angular-abp\nswag\service.config.nswag, isi :
```
"fromSwagger": {
        "url": "<be-dotnetcore-url>:<port>/swagger/v1/swagger.json",
        "output": null
    }
```
### Buka D:\PROJECT\RISET\aspnetboilerplate\GITHUB\angular-abp\src\assets\appconfig.json, isi :
```
"remoteServiceBaseUrl": "<be-dotnetcore-url>:<port>",
"appBaseUrl": "<local-url>:<port>",
```
### Generate Service Proxy
Buka CMD dan masuk ke folder **./nswag**. Jalankan file **refresh.bat** untuk re-generate service proxy class (digunakan untuk memanggil method-method service/api/backend).
<br/>
Saat ada penambahan service baru, kita harus mendaftarkannya di **src/shared/service-proxies/service-proxy.module.ts**. Buka dan tambahkan **ApiServiceProxies.NewServiceNameServiceProxy** pada array providers.
Langkah kedua ini hanya diperlukan saat ada service baru ditambahkan, jika hanya ada perubahan pada service yang sudah pernah didaftarkan maka tidak perlu dilakukan lagi. Jika ini tidak dilakukan saat ada service baru, maka service baru tersebut tidak akan bisa di akses dari komponen lain.
### yarn start
## Info
### mengatur menu yang tampil
D:\PROJECT\RISET\aspnetboilerplate\GITHUB\angular-abp\src\app\shared\layout\nav\app-navigation.service.ts
