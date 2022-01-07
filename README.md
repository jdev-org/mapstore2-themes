# mapstore2-themes

To custom, create and build mapstore2 themes from less files :

https://lesscss.org/

## Install

1. Clone project
```
git clone https://github.com/jdev-org/mapstore2-themes.git
```

2. Install `less` processor :
```
npm install -y -g less
```

## Build

1. Dupplicate `dark` theme (or other default mapstore2 available theme)
2. change or adapt variable.less file
3. build :
```
lessc <path/theme.less> <path/mytheme.css>
```

## Deploy

1. deploy mytheme.css file

Deploy `mytheme.css` file into mapstore2-georchestra webapp (e.g `/webapps/mapstore/themes/mytheme/mytheme.css`)

2. Open `localConfig.json` and insert new available theme for contextCreator config :

```
          {
            "name": "ContextCreator",
            "cfg": {
              "themes":[
                {"id":"mytheme", "type":"link", "href":"themes/mytheme/mytheme.css"}
              ]
            }
          },
```
