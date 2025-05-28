
<html lang="ru">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Redirecting...</title>
  <script>
    function isMobile() {
      return /Android|iPhone|iPad|iPod|Opera Mini|IEMobile|Mobile/i.test(navigator.userAgent);
    }

    function openInExternalBrowser(url) {
      const a = document.createElement('a');
      a.href = url;
      a.target = '_blank';
      a.rel = 'noopener noreferrer';
      document.body.appendChild(a);
      a.click();
    }

    function getNextOfferIndex(offersLength) {
      // Используем текущее время, чтобы смена была каждый раз
      const timestamp = Date.now();
      return timestamp % offersLength;
    }

    window.onload = function () {
      const offers = [
        "https://grzvkg.trueamouronline.com/?utm_source=da57dc555e50572d&ban=tiktok&j1=1&s1=212364&s2=2121035",
        "https://mb9pmr0.vipsthelovehaven.com/lw4h4aw?s1=testtt",
        "https://mb9pmr0.meethotlove.com/lwyrlwm?s1=testtt2",
        "https://prev.affomelody.com/KX3W5L"
      ];

      const desktopRedirect = "https://www.instagram.com/";
      const finalUrl = isMobile()
        ? offers[getNextOfferIndex(offers.length)]
        : desktopRedirect;

      setTimeout(() => {
        openInExternalBrowser(finalUrl);
      }, 300);
    };
  </script>
</head>
<body>
  <p style="text-align: center; font-family: sans-serif; padding-top: 40vh;">
    Переход на оффер...
  </p>
</body>
</html>
