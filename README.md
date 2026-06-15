# country-dial-codes-emoji-svg

A converged JSON dataset of country dial codes, Unicode emojis, and premium SVG flag URLs.

---

## 🚀 Why This Dataset Exists

When building premium user interfaces—such as international phone number pickers or country selectors—developers often face a trade-off between visual aesthetics and reliability. Relying solely on hosted image URLs can break your UI if a user has a poor network connection or strict data limits. 

This dataset solves that problem by merging high-resolution imagery with native text-based fallbacks.

### Key Features
* **Network-Resilient UI:** Use high-quality **SVG images** on stable connections, and seamlessly fall back to lightweight native **Unicode Emojis** when offline or conserving data.
* **Geopolitical Name Matching:** Discrepancies in country naming conventions across datasets (e.g., *Eswatini* vs. *Swaziland* or *Macau* vs. *Macao*) have been normalized using **ISO 3166-1 Alpha-2** codes as the gold-standard identifier.
* **Built-in Search Optimization:** Includes an `alternateName` field to capture naming variations, ensuring a smooth user search experience.

---

## 📦 Data Schema

The entire dataset is structured as a clean, production-ready JSON array. Missing fields are explicitly set to `null` instead of empty strings to integrate perfectly with standard JSON serializers (like Dart's `json_decode` or JavaScript's `JSON.parse`).

```json
[
  {
    "name": "India",
    "alternateName": null,
    "isdCode": "+91",
    "isoCode": "IN",
    "flagEmoji": "🇮🇳",
    "flagImage": "[https://cdn.kcak11.com/CountryFlags/countries/in.svg](https://cdn.kcak11.com/CountryFlags/countries/in.svg)"
  },
  {
    "name": "Swaziland",
    "alternateName": "Eswatini",
    "isdCode": "+268",
    "isoCode": "SZ",
    "flagEmoji": "🇸🇿",
    "flagImage": "[https://cdn.kcak11.com/CountryFlags/countries/sz.svg](https://cdn.kcak11.com/CountryFlags/countries/sz.svg)"
  }
]
```

---

## 🙏 Credits & Upstream Sources

This converged dataset is a derivative work built by merging, cleaning, and verifying data from two excellent open-source repositories. If you find this project useful, please consider visiting and starring the original upstream sources:

* **Dial Codes & Emojis Base:** Sourced from the [diogocapela / country-dial-codes.json](https://gist.github.com/diogocapela/1638d3967bef3a2c5ec24bfe07ce2d8f#file-country-dial-codes-json) GitHub Gist.
* **High-Res SVG Flag Assets:** Sourced from the [kcak11 / countries.json](https://gist.github.com/kcak11/4a2f22fb8422342b3b3daa7a1965f4e4#file-countries-json) GitHub Gist.

---

## 📄 License

This dataset is open-source and available under the **MIT License**. Feel free to use, modify, and distribute it in both personal and commercial applications.
