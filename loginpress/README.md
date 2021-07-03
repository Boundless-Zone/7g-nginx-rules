# LoginPress exclusions

This rule adds an exclusion for the LoginPress admin customizer.

Going to LoginPress > Customizer opens a link like this: https://example.com/wp-admin/admin.php?page=loginpress.

That link redirects to a customizer page, which is blocked by 7g.

## 7g Error

```
[date] [":bad_querystring_12::bad_request_15:"] 1.2.3.4 example.com "GET /wp-admin/customize.php?url=https://example.com/wp-login.php&autofocus=loginpress_panel HTTP/1.1" 403 0.000 "https://example.com/wp-admin/admin.php?page=loginpress-addons" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/89.0.4389.90 Safari/537.36"
```

## Credit

- Noam Kfir <noam@boundless.zone>
