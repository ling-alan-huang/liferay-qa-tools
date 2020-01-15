# Liferay QA Tools

## Some Features

Download `lfieray-qa-tools`.

<s>### コード自動補完ファイル（サブライム用）</s>

### 生成代码自动完成文件（Sublime使用）

> Backup and remove all files in `/home/alan/.config/sublime-text-3/Packages/User/`

1. Open `qa-tools.gradle`

3. Replace Potal directory: `String portalDir = "/home/alan/liferay_code/master/liferay-portal"`

4. Replace Sublime User directory: `String sublimeUserDir = "/home/alan/.config/sublime-text-3/Packages/User/"`

5. In `lfieray-qa-tools`, run `./gradlew -b qa-tools.gradle buildCompletionsFile`

-------------------

*Console:*

```
alan@alan-5540:~/liferay_code/liferay-qa-tools[master]$ ./gradlew -b qa-tools.gradle buildCompletionsFile
Picked up JAVA_TOOL_OPTIONS: -Duser.language=en
Java HotSpot(TM) 64-Bit Server VM warning: ignoring option MaxPermSize=256m; support was removed in 8.0

> Task :buildSettingFile
Updated '/home/alan/.config/sublime-text-3/Packages/User/JavaScript.sublime-settings'

> Task :buildThemeFile
Updated '/home/alan/.config/sublime-text-3/Packages/User/Default.sublime-theme'

> Task :buildCompletionsFile
Updated '/home/alan/.config/sublime-text-3/Packages/User/poshi.sublime-completions'

BUILD SUCCESSFUL in 1s
3 actionable tasks: 3 executed
alan@alan-5540:~/liferay_code/liferay-qa-tools[master]$
```

<s>### PATH 依頼検索</s>

### PATH的调用关系查找

For example:

`Button#SAVE` is what you are looking for.

In `lfieray-qa-tools`, run `./gradlew -b qa-tools.gradle searchDependencies -Pdependency='Button#SAVE'`

-------------------

*Console:*

```
alan@alan-5540:~/liferay_code/liferay-qa-tools[master]$ ./gradlew -b qa-tools.gradle searchDependencies -Pdependency='Button#SAVE'
Picked up JAVA_TOOL_OPTIONS: -Duser.language=en
Java HotSpot(TM) 64-Bit Server VM warning: ignoring option MaxPermSize=256m; support was removed in 8.0

> Task :searchDependencies
Updated '/home/alan/liferay_code/liferay-qa-tools/Button#SAVE.log'

BUILD SUCCESSFUL in 22s
1 actionable task: 1 executed
alan@alan-5540:~/liferay_code/liferay-qa-tools[master]$
```
-------------------

Open output file `Button#SAVE.log`