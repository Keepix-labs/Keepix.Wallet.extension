<div align="center">
<img src="public/icon-128.png" alt="logo"/>
<h1> Keepix Chrome Extension</h1>

</div>

## Pages <a name="pages"></a>

### New Tab <a name="newtab"></a>

[Override Chrome pages](https://developer.chrome.com/docs/extensions/mv3/override/)<br/>
`chrome_url_overrides` in manifest.json

```
"chrome_url_overrides": {
  "newtab": "src/pages/newtab/index.html"
}
```

### Popup <a name="popup"></a>

[Browser actions](https://developer.chrome.com/docs/extensions/reference/browserAction/)<br/>
`action` in manifest.json

```
"action": {
  "default_popup": "src/pages/popup/index.html",
  "default_icon": {
    "32": "icon-32.png"
  }
}
```

### Devtools <a name="devtools"></a>

[Devtools](https://developer.chrome.com/docs/extensions/mv3/devtools/#creating)<br/>
`devtools_page` in manifest.json

```
"devtools_page": "src/pages/devtools/index.html"
```

### Background <a name="background"></a>

[Background](https://developer.chrome.com/docs/extensions/mv3/background_pages/)<br/>
`background` in manifest.json

```
"background": {
  "service_worker": "src/pages/background/index.ts",
  "type": "module"
}
```

### ContentScript <a name="contentscript"></a>

[Content Script](https://developer.chrome.com/docs/extensions/mv3/content_scripts/)<br/>
`content_scripts[0]` in manifest.json

```
"content_scripts": [
  {
    "matches": ["http://*/*", "https://*/*", "<all_urls>"],
    "js": ["src/pages/content/index.tsx"],
    "css": ["contentStyle.css"]
  }
]
```

### Options <a name="options"></a>

[Options](https://developer.chrome.com/docs/extensions/mv3/options/)<br/>
`options_page` in manifest.json

```
"options_ui": {
  "page": "src/pages/options/index.html"
}
```

### SidePanel (Chrome 114+) <a name="sidepanel"></a>

[SidePanel](https://developer.chrome.com/docs/extensions/reference/sidePanel/)<br/>
`side_panel.default_path` in manifest.json
