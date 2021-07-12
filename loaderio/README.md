# loader.io exclusion

The 7g firewall blocks the loader.io verification bot because it matches the word `loader`.
This rule matches the name of the verification file as a `.txt` or `.html` file or a directory name.

## 7g Error

```
[date] [":bad_bot_5:"] 1.2.3.4 example.com "GET /loaderio-<32-digit-code>/ HTTP/1.1" 403 0.000 "-" "loaderio;verification-bot"
```

# Credit

- Noam Kfir <noam@boundless.zone>
