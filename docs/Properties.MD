# Свойства  Adeptik.AspNet.Angular для MSBuild

## Пути

Имя свойства | Описание | Значение по умолчанию
------------ | -------- | ---------------------
`VSWebRootDir` | Папка web-содержимого, используемая Visual Studio при запуске web-приложения. Не содержит завершающий слэш. | $(MSBuildProjectDirectory)\wwwroot
`WebRootPublishRelativePath` | Папка, в которую помещаются файлы фронтэнда при публикации, относительно корня папки публикации. Не содержит завершающий слэш. | wwwroot
`NgProjectDirPath` | Путь к папке исходных файлов фронтэнда относительно корня проекта. Не содержит завершающий слэш. | Angular
`NgProjectDir` | Абсолютный путь к папке исходных файлов фронтэнда. Не содержит завершающий слэш. | $(MSBuildProjectDirectory)\\$(NgProjectDirPath)
`NgOutDir` | Путь к папке, в которую помещается сборка фронтэнда, относительно корня проекта. Не содержит завершающий слэш. | bin\\$(Configuration)\angular
`NgTargetDir` | Абсолютный путь к папке, в которую помещается сборка Angular. Не содержит завершающий слэш. | $(MSBuildProjectDirectory)\\$(NgOutDir)
`NgIntermediateDir` | Папка для промежуточного хранения файлов. Не содержит завершающий слэш. | $(MSBuildProjectDirectory)\obj\\$(Configuration)\angular

## Параметры сборки Angular CLI

Имя свойства | Описание | Значение по умолчанию
------------ | -------- | ---------------------
`NgBuildTarget` | Тип построения. Принимает значения: development, production. | development
`NgBuildEnvironment` | Имя среды. | dev
`NgBuildSourcemaps` | Признак того, что необходимо сгенерировать map-файлы. | True
`NgBuildVendorChunk` | Признак того, что для своих библиотек необходимо использовать отдельный bundle. | True
`NgBuildAOT` | Признак использования компиляции "Ahead of time". | False
`NgBuildBaseHref` | Базовый url. | /
`NgBuildDeployUrl` | Url развертывания. | `<пусто>`
`NgBuildVebose` | Вывод дополнительной информации в консоль. | False
`NgBuildExtractCSS` | Извлечение глобальных стилей в файлы css вместо js. | False
`NgBuildOutputHashing` | Режим хэширования имен выходных файлов. Принимает значения: `none`\|`all`\|`media`\|`bundles`. | media

Если сборка происходит для конфигурации с именем `Release`, то свойства принимают значения по умолчанию, указанные в таблице:

Имя свойства | Значение по умолчанию
------------ | ---------------------
`NgBuildTarget` | production
`NgBuildEnvironment` | prod
`NgBuildSourcemaps` | False
`NgBuildAOT` | True
`NgBuildExtractCSS` | True
`NgBuildOutputHashing` | all