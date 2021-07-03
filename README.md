# 7g-nginx-rules
[GridPane](https://gridpane.com/) adapted the [7G Firewall](https://perishablepress.com/7g-firewall/) built by Perishable Press for Nginx.

In the process, they modularized it and made it possible to add custom rules to quickly and selectively block or allow requests.

This repository hosts custom rules for GridPane's nginx variant of the 7g firewall.

## Instructions

For instructions on how to create and use these custom rules, see
https://gridpane.com/kb/using-the-7g-web-application-firewall/#custom-rules.

To contribute rules to the repository, follow these steps:

1. Fork this repo.
2. Create a folder for the tool. If the rule is for a WordPress plugin, use the plugin's slug for the folder name. Find a suitable descriptive slug if it's something else.
3. Add your rules to the folder.
4. Add a Markdown file named README.md to the exception folder to document the rule and for credit.
5. Send a pull request.

Check out the existing examples for the recommended file and folder structure.
