# WP Rocket exclusion

The 7g firewall blocks an svg file on the WP Rocket admin page because the file has `config` in the file name.

## 7g Error

```
[date] [":bad_request_24:"] 1.2.3.4 example.com "GET /wp-content/plugins/wp-rocket/assets/img/configuration.svg HTTP/2.0" 403 0.000 "https://<site>/wp-content/plugins/wp-rocket/assets/css/wpr-admin.css?ver=3.9.0.5" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4472.114 Safari/537.36"
```

# Credit

- Noam Kfir <noam@boundless.zone>
