# Amelia API exclusion

The 7g firewall blocks the Contact Form 7 DB export command.
This rule picks those requests by filtering `cfdb-export` actions and unblocking them.

## 7g Error

```
[date] [":bad_request_6:"] 1.2.3.4 example.com "GET /wp-admin/admin-ajax.php?action=cfdb-export&form=<url-encoded-form-name>&enc=CSVUTF8&regionaldelimiter=true&filter=submit_time[in]<comma-separated-list-of-unicode-submit-times> HTTP/1.1" 403 0.000 "https://example.com/wp-admin/admin.php?page=CF7DBPluginSubmissions&form_name=<url-encoded-form-name>" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4472.77 Safari/537.36"
```

# Credit

- Noam Kfir <noam@boundless.zone>
