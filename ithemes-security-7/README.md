# iThemes Security 7 exclusion

The 7g firewall blocks the iThemes Security 7 pages, apparently because they use the `~` (tilde) character in the file names.

A single request blocks a bunch of resource requests:
- `/wp-content/plugins/ithemes-security-pro/dist/dashboard/dashboard~settings~settings~settings~dashboard~settings~settings~widget~settings~dashboard~c059c84f.min.css?ver=057df020ff5d410071e5`
- `/wp-content/plugins/ithemes-security-pro/dist/vendors/backup/dashboard~admin-notices-api~api~dashboard~settings~settings~settings~dashboard~api~se~d4341348.min.js?ver=ee293bcc2174cfbd7fd9`
- `/wp-content/plugins/ithemes-security-pro/dist/vendors/dashboard/dashboard~settings~settings~settings~settings~settings.min.js?ver=7aa0462511eed8b3e824`
- `/wp-content/plugins/ithemes-security-pro/dist/vendors/dashboard/dashboard~settings~settings~settings~dashboard~settings~settings~widget~settings~d~6fb56b45.min.js?ver=f09f771ec18375bae209`
- `/wp-content/plugins/ithemes-security-pro/dist/backup/dashboard~dashboard~settings~settings~settings~settings~dashboard~settings~settings~widget~se~157f4e98.min.js?ver=ba09f621164711e1849f`
- `/wp-content/plugins/ithemes-security-pro/dist/vendors/dashboard/dashboard~settings~settings~settings~settings~settings~settings.min.js?ver=39b647a29810d652f9a6`
- `/wp-content/plugins/ithemes-security-pro/dist/dashboard/dashboard~settings~settings~settings~dashboard~settings~settings~widget~settings~dashboard~c059c84f.min.js?ver=ab9bab4dbd38fdb8a248`
- `/wp-content/plugins/ithemes-security-pro/dist/user-groups/settings~dashboard.min.js?ver=5187c6b78319d626a264`
- `/wp-content/plugins/ithemes-security-pro/dist/dashboard/dashboard~settings~settings~settings~dashboard~settings~settings~widget~settings~dashboard~c059c84f.min.css?ver=057df020ff5d410071e5`
- `/wp-content/plugins/ithemes-security-pro/dist/vendors/backup/dashboard~admin-notices-api~api~dashboard~settings~settings~settings~dashboard~api~se~d4341348.min.js?ver=ee293bcc2174cfbd7fd9`
- `/wp-content/plugins/ithemes-security-pro/dist/vendors/dashboard/dashboard~settings~settings~settings~settings~settings.min.js?ver=7aa0462511eed8b3e824`
- `/wp-content/plugins/ithemes-security-pro/dist/vendors/dashboard/dashboard~settings~settings~settings~settings~settings~settings.min.js?ver=39b647a29810d652f9a6`
- `/wp-content/plugins/ithemes-security-pro/dist/vendors/dashboard/dashboard~settings~settings~settings~dashboard~settings~settings~widget~settings~d~6fb56b45.min.js?ver=f09f771ec18375bae209`
- `/wp-content/plugins/ithemes-security-pro/dist/dashboard/dashboard~settings~settings~settings~dashboard~settings~settings~widget~settings~dashboard~c059c84f.min.js?ver=ab9bab4dbd38fdb8a248`
- `/wp-content/plugins/ithemes-security-pro/dist/backup/dashboard~dashboard~settings~settings~settings~settings~dashboard~settings~settings~widget~se~157f4e98.min.js?ver=ba09f621164711e1849f`
- `/wp-content/plugins/ithemes-security-pro/dist/user-groups/settings~dashboard.min.js?ver=5187c6b78319d626a264`

## 7g Error

```
[date] [":bad_request_6:"] 1.2.3.4 example.com "GET /wp-content/plugins/ithemes-security-pro/dist/vendors/backup/dashboard~admin-notices-api~api~dashboard~settings~settings~settings~dashboard~api~se~d4341348.min.js?ver=ee293bcc2174cfbd7fd9 HTTP/2.0" 403 0.000 "https://<site>/wp-admin/admin.php?page=itsec-dashboard" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4472.114 Safari/537.36"
```

# Credit

- Noam Kfir <noam@boundless.zone>
