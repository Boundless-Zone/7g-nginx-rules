# Amelia API exclusion

It looks like the 7g firewall is flagging the `ajaxurl` querystring value.
This rule excludes that parameter.

# Sample Requests

| Error | URL |
| ----- | --- |
| `:bad_querystring_12::bad_request_15:` | `GET /wp-content/plugins/Woocommerce-chita-delivery/templates/map.php?ajaxurl=https://domain/wp-admin/admin-ajax.php&gapi=google-maps-api` |

# Credit

- Noam Kfir <noam@boundless.zone>
- Adapted from the GridPane example for [whitelisting a query string for SEOPress and Google Search Console](https://gridpane.com/kb/using-the-7g-web-application-firewall/)
