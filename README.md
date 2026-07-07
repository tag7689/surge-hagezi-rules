Surge Hagezi Pro++ Sync

This repository automatically fetches the Wildcard version of the [Hagezi Pro++ DNS Blocklist](https://github.com/hagezi/dns-blocklists#proplus) daily and converts it into a highly efficient RULE-SET format tailored for Surge Mac / iOS.

⚙️ Automation Mechanism

Powered by GitHub Actions, the conversion runs automatically every day at 20:00 UTC. Zero server maintenance required.

Directly extracts HaGeZi's highly efficient wildcard onlydomains list.

Utilizes Surge's native RULE-SET syntax (prefixing domains with DOMAIN-SUFFIX), which inherently supports subdomain matching. It maintains lightning-fast matching speeds even with over a hundred thousand rules.

📜 License & Credits

The automation script (GitHub Actions YAML) in this repository is licensed under the MIT License.

The original DNS blocklist data is created and maintained by [HaGeZi](https://github.com/hagezi/dns-blocklists), licensed under CC BY-SA 4.0. All credits for the domain categorization and compilation go to the original author.
