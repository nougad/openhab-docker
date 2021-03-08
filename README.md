# openhab-docker
For of https://github.com/openhab/openhab-docker but without healthcheck

The HEALTHCHECK causes docker to write to disk every 30 seconds which prevents disk hibernation on NAS.

Example log in file `config.v2.json`:

    "Health": {
      "Status": "healthy",
      "FailingStreak": 0,
      "Log": [
        {
          "Start": "2019-10-04T16:42:07.855025309+02:00",
          "End": "2019-10-04T16:42:08.036342122+02:00",
          "ExitCode": 0,
          "Output": "  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current\n                                 Dload  Upload   Total   Spent    Left  Speed\n\r  0     0    0     0    0     0      0                 0 --:--:-- --:--:-- --:--:--     0\r100  1000  100  1000    0     0   488k      0 --:--:-- --:--:-- --:--:--  488k\n<!doctype html><html><head><meta charset=\"utf-8\"><meta http-equiv=\"Content-Security-Policy\" content=\"default-        src * 'self' 'unsafe-inline' 'unsafe-eval' data: gap: content: blob:\"><meta name=\"viewport\" content=\"width=device-width,initial-scale=1,maximum-scale=1,minimum-scale=1,user-scalable=no,minimal-ui,viewport-fit=cover\"><meta            name=\"theme-color\" content=\"#e64a19\"><meta name=\"format-detection\" content=\"telephone=no\"><meta name=\"msapplication-tap-highlight\" content=\"no\"><title>openHAB</title><meta name=\"apple-mobile-web-app-capable\"                 content=\"yes\"><meta name=\"apple-mobile-web-app-status-bar-style\" content=\"black-translucent\"><link rel=\"apple-touch-icon\" href=\"res/icons/apple-touch-icon.png\" crossorigin=\"use-credentials\"><link rel=\"icon\" href=\"res/      icons/favicon.png\" crossorigin=\"use-credentials\"><link rel=\"manifest\" href=\"/manifest.json\" crossorigin=\"use-credentials\"><link href=\"css/app.css\" rel=\"stylesheet\"></head><body><div id=\"app\"></div><script src=\"js/app.     js\"></script></body></html>"
        },
