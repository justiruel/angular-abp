# angular-abp
## setting awal angular-abp
### 1. yarn install
### 2. Buka D:\PROJECT\RISET\aspnetboilerplate\GITHUB\angular-abp\nswag\service.config.nswag, isi :
```
"fromSwagger": {
        "url": "<be-dotnetcore-url>:<port>/swagger/v1/swagger.json",
        "output": null
    }
```
### 3. Buka D:\PROJECT\RISET\aspnetboilerplate\GITHUB\angular-abp\src\assets\appconfig.json, isi :
```
"remoteServiceBaseUrl": "<be-dotnetcore-url>:<port>",
"appBaseUrl": "<local-url>:<port>",
```
### 4. Generate Service Proxy
Buka CMD dan masuk ke folder **./nswag**. Jalankan file **refresh.bat** untuk re-generate service proxy class (digunakan untuk memanggil method-method service/api/backend).
<br/>
Saat ada penambahan service baru, kita harus mendaftarkannya di **src/shared/service-proxies/service-proxy.module.ts**. Buka dan tambahkan **ApiServiceProxies.NewServiceNameServiceProxy** pada array providers.
Langkah kedua ini hanya diperlukan saat ada service baru ditambahkan, jika hanya ada perubahan pada service yang sudah pernah didaftarkan maka tidak perlu dilakukan lagi. Jika ini tidak dilakukan saat ada service baru, maka service baru tersebut tidak akan bisa di akses dari komponen lain.
### 5. yarn start
### 6. Error "abp is not defined"
solusinya :
```
- npm install --save abp-ng2-module
- npm install --save abp-web-resources
```
atau coba saat menjalankan no. 1 (yarn install), cmd run as administrator

## Info
### mengatur menu yang tampil
D:\PROJECT\RISET\aspnetboilerplate\GITHUB\angular-abp\src\app\shared\layout\nav\app-navigation.service.ts
