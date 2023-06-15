# WooCommerce Chita exclusion

It looks like the 7g firewall is flagging the `ajaxurl` querystring value.
This rule excludes that parameter.

Chita seems to have either added or changed the way they handle some commands.
This rule also deals with the new mechanism, matching the `chita_create_shipping_label` string under `admin-ajax`.

# Sample Requests

| Error | URL |
| ----- | --- |
| `:bad_querystring_12::bad_request_15:` | `GET /wp-content/plugins/Woocommerce-chita-delivery/templates/map.php?ajaxurl=https://domain/wp-admin/admin-ajax.php&gapi=google-maps-api` |
| `:bad_request_15:` | `GET /wp-admin/admin-ajax.php?action=chita_create_shipping_label&order_url=https://chita-il.com/RunCom.Server/Request.aspx?APPNAME=run&PRGNAME=ship_print_ws&ARGUMENTS=-N12345678&order_id=12345` |

# Credit

- Noam Kfir <noam@boundless.zone>
- Adapted from the GridPane example for [whitelisting a query string for SEOPress and Google Search Console](https://gridpane.com/kb/using-the-7g-web-application-firewall/)
