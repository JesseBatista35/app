Skip to main content
Azure DevOps
projetos
/
Caixa
/
Repos
/
Files
/

SIAME-android
Search


Caixa

Overview

Boards

Repos
Files
Commits
Pushes
Branches
Tags
Pull requests

Pipelines

Test Plans

Artifacts
Project settings
SIAME-android

app
gradle
tutoriais
.gitignore
build.gradle
CHANGELOG.md
gradle.properties
gradlew
gradlew.bat
hs_err_pid1712.log
README.md
replay_pid1712.log
settings.gradle

feature/item_STRY00127759-replace-sso-with-xid

/
build.gradle
build.gradle

Edit

Contents
History
Compare
Blame

12345678910111213141516
buildscript {
    ext.hilt_version = '2.54'
    dependencies {
        classpath("androidx.navigation:navigation-safe-args-gradle-plugin:2.5.0")
        classpath "com.google.dagger:hilt-android-gradle-plugin:$hilt_version"
    }
}

plugins {
    id 'com.android.application' version '8.8.2' apply false
    id 'com.android.library' version '8.8.2' apply false
    id 'org.jetbrains.kotlin.android' version '2.1.10' apply false
    id 'com.google.devtools.ksp' version '2.1.10-1.0.31' apply false
    id 'com.google.gms.google-services' version '4.4.0' apply false
    id 'org.jetbrains.kotlin.plugin.compose' version '2.1.10' apply false
}
Finished loading items

Showing 32 items.

Searching...

Showing 10 filtered items.

Showing 32 items.

Searching...

Showing 4 filtered items.

Showing 4 filtered items.

Collapsed

Expanded

Searching...

Showing 4 filtered items.

Showing 4 filtered items.

Collapsed

Row 6. Clickable



buildscript {
    ext.hilt_version = '2.54'
    dependencies {
        classpath("androidx.navigation:navigation-safe-args-gradle-plugin:2.5.0")
        classpath "com.google.dagger:hilt-android-gradle-plugin:$hilt_version"
    }
}

plugins {
    id 'com.android.application' version '8.8.2' apply false
    id 'com.android.library' version '8.8.2' apply false
    id 'org.jetbrains.kotlin.android' version '2.1.10' apply false
    id 'com.google.devtools.ksp' version '2.1.10-1.0.31' apply false
    id 'com.google.gms.google-services' version '4.4.0' apply false
    id 'org.jetbrains.kotlin.plugin.compose' version '2.1.10' apply false
}


atuamente ta assim
