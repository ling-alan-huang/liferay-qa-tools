# Liferay QA Tools

## Some Features

### コード自動補完ファイル（サブライム用）

1. Place `qa-tools.gradle` in somewhere, for example: `/home/alan/liferay_code/master/liferay-portal/modules/qa-tools.gradle`

2. Open `qa-tools.gradle`

3. Replace Potal directory: `String portalDir = "/home/alan/liferay_code/master/liferay-portal"`

4. Replace macro directory: `String macroDir = portalDir + "/portal-web/test/functional/com/liferay/portalweb/macros"`

5. Replace function directory: `String functionsDir = portalDir + "/portal-web/test/functional/com/liferay/portalweb/functions"`

6. Replace Sublime directory: `String userDir = "/home/alan/.config/sublime-text-3/Packages/User/"`

7. Run `../gradlew -b /home/alan/liferay_code/master/liferay-portal/modules/qa-tools.gradle buildCompletionsFile`

```
alan@alan-5540:~/liferay_code/master/liferay-portal/modules[master]$ ../gradlew -b /home/alan/liferay_code/master/liferay-portal/modules/qa-tools.gradle buildCompletionsFile
Picked up JAVA_TOOL_OPTIONS: -Duser.language=en
Java HotSpot(TM) 64-Bit Server VM warning: ignoring option MaxPermSize=256m; support was removed in 8.0
Configuration on demand is an incubating feature.

> Configure project :
Updated '/home/alan/.config/sublime-text-3/Packages/User/poshi.sublime-completions'
Updated '/home/alan/.config/sublime-text-3/Packages/User/JavaScript.sublime-settings'
Updated '/home/alan/.config/sublime-text-3/Packages/User/Default.sublime-theme'

> Task :buildSettingFile UP-TO-DATE
> Task :buildThemeFile UP-TO-DATE
> Task :buildCompletionsFile UP-TO-DATE


BUILD SUCCESSFUL in 3s
alan@alan-5540:~/liferay_code/master/liferay-portal/modules[master]$ 
```