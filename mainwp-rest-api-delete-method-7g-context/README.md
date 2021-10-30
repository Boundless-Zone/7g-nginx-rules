# Exclusion for MainWP DELETE method

This rule adds an exclusion for `DELETE` requests sent to the MainWP REST API.
7g blocks all `DELETE` methods and this rule excludes the method when the request is made to the `/wp-json/mainwp/` path.

# Credit

- Noam Kfir <noam@boundless.zone>
