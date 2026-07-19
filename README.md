<h1 align="center">TXDrive</h1>

<hr>

> ## Cloudflare ❤️ Workers Üzerinde Çalışan Bir Google Drive İndeksi.

<p align="center"><img src="images/ss.png"></p>

Çoklu disk, arama, sayfalama ve harici oynatıcı çağırma özelliklerinin yanı sıra DPlayer oynatma desteği sunar.

### Client ID, Client Secret ve Refresh Token Oluşturmak İçin Manuel Yöntem

- https://console.developers.google.com/apis/credentials adresini açın.
- Bir proje oluşturduktan sonra veya zaten bir projeniz varsa.
- "Kimlik bilgisi oluştur" (Create credentials) seçeneğine tıklayın.
- "OAuth istemci kimliği" (OAuth client ID) seçeneğini belirleyin.
- "Web uygulaması" (Web application) seçeneğini seçin.
- Bir isim verin (kendiniz için referans olabilecek herhangi bir isim).
- "Yetkilendirilmiş JavaScript kaynakları" (Authorized JavaScript origins) bölümüne https://developers.google.com adresini ekleyin.
- "Yetkilendirilmiş yönlendirme URI'leri" (Authorized redirect URIs) bölümüne https://developers.google.com/oauthplayground adresini ekleyin.
- Kaydedin ve İstemci Kimliğinizi (Client ID) ve İstemci Sırrınızı (Client Secret) bir kenara not edin.
- https://developers.google.com/oauthplayground adresini açın.
- Sağ üst köşedeki Ayarlar Simgesine ![](https://developers.google.com/oauthplayground/assets/images/settings.png) tıklayın.
- "Kendi OAuth kimlik bilgilerinizi kullanın" (Use your own OAuth credentials) seçeneğine tıklayın.
- OAuth Client ID ve OAuth Client secret bilgilerini girin.
- Şimdi aynı sayfanın sol tarafındaki Adım 1'e ("Select & authorize APIs") geri dönün.
- "Drive API v3"ü bulun.
- İlk seçeneği, yani https://www.googleapis.com/auth/drive seçeneğini seçin.
- "Authorize API" butonuna tıklayın ve Google hesabınızı kullanarak gerekli izinleri verin.
- Kimlik doğrulama tamamlandığında sayfa otomatik olarak Adım 2 olan "Exchange authorization code for tokens" kısmına geçecektir.
- "Exchange authorization code for tokens" butonuna tıklayın. Eğer Adım 3'e geçerse, manuel olarak Adım 2'ye geri tıklayın.
- "Auto-refresh the token before it expires" (Süresi dolmadan önce belirteci otomatik yenile) seçeneğini işaretleyin.

### Ekstra Seçenekler

```js
const uiConfig = {
  .......
  "avatar": "https://i.ibb.co/jW0TDZH/image.png",  // Navigasyon çubuğundaki avatar görselini değiştirir
  "disable_navicon": true // Navigasyon çubuğundaki gereksiz yönlendirme menüsünü devre dışı bırakır
  .......
};
```
