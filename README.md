# Surge Hagezi Pro++ Sync

This repository automatically fetches the Wildcard version of the [Hagezi Pro++ DNS Blocklist](https://github.com/hagezi/dns-blocklists#proplus) daily and converts it into a highly efficient `RULE-SET` format tailored for Surge Mac / iOS.

**To block ads using the Rule module:**

```ini
[Rule]
# Hagezi Pro++
RULE-SET,https://raw.githubusercontent.com/YourUsername/YourRepo/main/hagezi_pro_plus.list,REJECT

# Hagezi TIF (Automatically split into ~40MB parts to bypass GitHub limits)
RULE-SET,https://raw.githubusercontent.com/YourUsername/YourRepo/main/hagezi_tif_part_aa.list,REJECT
RULE-SET,https://raw.githubusercontent.com/YourUsername/YourRepo/main/hagezi_tif_part_ab.list,REJECT
# Add part_ac, part_ad... if the list grows larger
```


### ⚙️ Automation Mechanism

* Powered by GitHub Actions, the conversion runs automatically every day at 20:00 UTC. Zero server maintenance required.

* Directly extracts HaGeZi's highly efficient `wildcard onlydomains` list:
  * [HaGeZi Normal(Recommend)](https://raw.githubusercontent.com/tag7689/surge-hagezi-rules/main/hagezi_pro_normal.list)
  * [HaGeZi Pro++](https://raw.githubusercontent.com/tag7689/surge-hagezi-rules/main/hagezi_pro_plus.list)
  * [HaGeZi TIF](https://raw.githubusercontent.com/tag7689/surge-hagezi-rules/main/hagezi_tif.list)

* Utilizes Surge's GUI-friendly `RULE-SET` syntax (`DOMAIN-SUFFIX,`). It maintains lightning-fast matching speeds even with over a hundred thousand rules.

* Large blocklists (like TIF) are automatically split into 40MB chunks to comply with GitHub's 50MB file size warning threshold.

### 📜 License & Credits

* The automation script (GitHub Actions `YAML`) in this repository is licensed under the MIT License.

* The original DNS blocklist data is created and maintained by [HaGeZi](https://github.com/hagezi/dns-blocklists), licensed under CC BY-SA 4.0. All credits for the domain categorization and compilation go to the original author.
