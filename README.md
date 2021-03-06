# Download Legends of Runeterra Data Dragon
[![Daily Test (@v1)](https://github.com/magisteriis/download-legends-of-runeterra-data-dragon/actions/workflows/daily-test.v1.yml/badge.svg)](https://github.com/magisteriis/download-legends-of-runeterra-data-dragon/actions/workflows/daily-test.v1.yml)

![image](https://user-images.githubusercontent.com/3706841/151632989-01f5ede8-b056-4e11-a5f7-dc40c9ffe237.png)

A GitHub Action for downloading the Legends of Runeterra Data Dragon.

> Legends of Runeterra Data Dragon (not to be confused with League of Legends Data Dragon) is the name of the static data product that will host both game assets and data for community use in media or product development. Assets and data are made available over the internet in the format described below, and are updated in tandem with game releases so the community can update their products with the latest and greatest data. Legends of Runeterra static data is split into two bundles; core bundles and set bundles. - [Riot Developer Portal](https://developer.riotgames.com/docs/lor#data-dragon)

## Example
Download the latest version as `./core.zip`, `./set1.zip`, `./set2.zip`, `./set3.zip`, `./set4.zip` and  `./set5.zip`.

    - name: Download Data Dragon
      uses: magisteriis/download-legends-of-runeterra-data-dragon@v1
      
    - name: Extract Data Dragon
      run: unzip '*.zip'
      
## Inputs
### `version`
Download a specific version of the Data Dragon.

*The action will replace `.` with `_` in the URL.*

    - name: Download Data Dragon version 1.0.0
      uses: magisteriis/download-legends-of-runeterra-data-dragon@v1
      with:
        version: 1.0.0
        
### `locale`
You can specify the locale to download. The default is `en_us`. 

*The action will lowercase the locale and replace `-` with `_` in the URL.*

    - name: Download Data Dragon for en-us
      uses: magisteriis/download-legends-of-runeterra-data-dragon@v1
      with:
        locale: en-US

### `bundles`
Download specific bundles of the Data Dragon. Example values: `core`, `sets`,`sets-lite`, `set1`, `set1-lite`, `core lite set1`, `core set1 set2-lite`.

    - name: Download Data Dragon core and lite sets
      uses: magisteriis/download-legends-of-runeterra-data-dragon@v1
      with:
        bundles: core sets-lite # Download core and all lite sets.

### `directory`
You can specify the directory where the data dragon files should be downloaded.

    - name: Download Data Dragon for en-us
      uses: magisteriis/download-legends-of-runeterra-data-dragon@v1
      with:
        directory: ./data-dragon
        
### Sponsors

[![Sentry Logo](https://raw.githubusercontent.com/mikaeldui/riot-games-dotnet-client/main/sponsors/sentry.svg)](https://sentry.io/for/good/)
[![JetBrains Logo (Main) logo](https://raw.githubusercontent.com/mikaeldui/riot-games-dotnet-client/main/sponsors/jetbrains.svg)](https://jb.gg/OpenSourceSupport)
        
## Notice from Riot Games, Inc.
The GitHub Action "[Download Legends of Runeterra Data Dragon](https://github.com/marketplace/actions/download-legends-of-runeterra-data-dragon)" by [@mikaeldui](https://github.com/mikaeldui) isn't endorsed by Riot Games and doesn't reflect the views or opinions of Riot Games or anyone officially involved in producing or managing Riot Games properties. Riot Games, and all associated properties are trademarks or registered trademarks of Riot Games, Inc.
