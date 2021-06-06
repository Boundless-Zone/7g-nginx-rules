# WooCommerce exclusions

This rule adds an exclusion for the WooCommerce order received callback called after the PayPal order completes successfully.
The rule might also apply to other payment methods but that hasn't been checked.

The rule creates an exemption for requests that match **both** of these conditions:
- The path matches `/checkout/order-received/\d+/` (for any numeric order number).
- The querystring matches `^key=wc_order_\w+&`.

## 7g Error

```
[date] [":bad_querystring_36:"] 1.2.3.4 example.com "GET /checkout/order-received/<order-number>/?key=wc_order_<hash>&utm_nooverride=1&token=<token>&tx=<transaction-number>&st=Pending&amt=<total>&cc=USD&cm=%7B<encoded-order-info-json>7D&item_number=&sig=<signature>%3D HTTP/1.1" 403 0.000 "https://www.paypal.com/" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4472.77 Safari/537.36"
```

# Credit

- Noam Kfir <noam@boundless.zone>
