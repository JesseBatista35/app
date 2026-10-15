plugins {
    id 'com.android.application'
    id 'org.jetbrains.kotlin.android'
    id 'kotlin-kapt'
    id 'kotlin-parcelize'
    id 'dagger.hilt.android.plugin'
    id 'androidx.navigation.safeargs.kotlin'
    id 'com.google.devtools.ksp'
    id 'com.google.gms.google-services'
    id 'org.jetbrains.kotlin.plugin.compose'
}

android {
    compileSdk 36

    defaultConfig {
        applicationId "br.gov.caixa.habitacao"
        minSdk 24
        targetSdk 36
        versionCode project.versionCode as Integer
        versionName "${versionApp}"
        project.archivesBaseName = "habitacao-${versionApp}"
        testInstrumentationRunner "androidx.test.runner.AndroidJUnitRunner"
        android.defaultConfig.manifestPlaceholders = ['appAuthRedirectScheme': 'br.gov.caixa.habitacao']
    }

    buildTypes {
        debug {
            debuggable true
            buildConfigField "String", "SSO_URL", "\"https://logindes.caixa.gov.br/auth/realms/internet/\""
            buildConfigField "String", "APP_CENTER_SECRET", "\"cd12c78d-562e-441f-a0da-d91f9852f66b\""

            buildConfigField "String", "GOOGLE_DB_SECRET_KEY", "\"PbLruAxMfCvR8GRABwreNg==\""
            buildConfigField "String", "MOBILE_SDK_APP_ID", "\"1:30447847847:android:d2b36f3edfe57088b20e82\""
            buildConfigField "String", "FIREBASE_URL", "\"https://habitacaocaixades.firebaseio.com\""
            buildConfigField "String", "PROJECT_NUMBER", "\"30447847847\""
            buildConfigField "String", "STORAGE_BUCKET", "\"habitacaocaixades.appspot.com\""
            buildConfigField "String", "PROJECT_ID", "\"habitacaocaixades\""
            buildConfigField("String", "SIGAM_ENVIRONMENT", "\"TQS\"")

            def unicoKey = System.getenv("UNICO_BIOMETRIC_SDK_KEY") ?: ""
            buildConfigField("String", "XID_UNICO_BIOMETRIC_SDK_KEY", "\"${unicoKey}\"")
        }

        release {
            debuggable false
            minifyEnabled true
            proguardFiles getDefaultProguardFile('proguard-android-optimize.txt'), 'proguard-rules.pro'
            buildConfigField "String", "SSO_URL", "\"https://login.caixa.gov.br/auth/realms/internet/\""
            buildConfigField "String", "APP_CENTER_SECRET", "\"8212fd47-b90c-4153-b155-2e38e075aa19\""

            buildConfigField "String", "GOOGLE_DB_SECRET_KEY", "\"PbLruAxMfCvR8GRABwreNg==\""
            buildConfigField "String", "MOBILE_SDK_APP_ID", "\"1:978309264263:android:fb2ea54ff4fdfdc1b95922\""
            buildConfigField "String", "FIREBASE_URL", "\"https://habitacaocaixades.firebaseio.com\""
            buildConfigField "String", "PROJECT_NUMBER", "\"978309264263\""
            buildConfigField "String", "STORAGE_BUCKET", "\"app-habitacao-interno.appspot.com\""
            buildConfigField "String", "PROJECT_ID", "\"app-habitacao-interno\""
            buildConfigField("String", "SIGAM_ENVIRONMENT", "\"PRODUCTION\"")

            def unicoKey = System.getenv("UNICO_BIOMETRIC_SDK_KEY") ?: ""
            buildConfigField("String", "XID_UNICO_BIOMETRIC_SDK_KEY", "\"${unicoKey}\"")
        }

        dev {
            initWith debug
            minifyEnabled true
            proguardFiles getDefaultProguardFile('proguard-android-optimize.txt'), 'proguard-rules.pro'
        }

        hmp {
            initWith debug
            debuggable false
        }

        piloto {
            initWith release
            buildConfigField("String", "SIGAM_ENVIRONMENT", "\"PILOT\"")
        }

        producao {
            initWith release
        }

        buildTypes.each {
            //Configs para o MFP

            it.buildConfigField "String", "SECURITY_ADAPTER", "\"SecurityAdapterCaixa\""
            it.buildConfigField "String", "CAIXA_TOKEN", "\"caixa.token\""

            //Configs gerais do SSO
            it.buildConfigField "String", "CLIENT_ID", "\"cli-mob-hab\""
            it.buildConfigField "String", "REDIRECT_URI", "\"br.gov.caixa.habitacao:/oauth2Callback\""

            it.buildConfigField "String", "SSO_ISSUER", "\".well-known/openid-configuration\""
            it.buildConfigField "String", "SSO_END_SESSION", "\"/protocol/openid-connect/logout\""
            it.buildConfigField "String", "SSO_SCOPE", "\"openid offline_access agente_moradia acessoIrrestrito\""
            it.buildConfigField "String", "SSO_APP_NAME", "\"br.gov.caixa.habitacao\""
        }
    }

    compileOptions {
        sourceCompatibility JavaVersion.VERSION_17
        targetCompatibility JavaVersion.VERSION_17
    }

    kotlinOptions {
        jvmTarget = '17'
    }

    buildFeatures {
        dataBinding true
        viewBinding true
        compose true
    }

    namespace 'br.gov.caixa.habitacao'
}

dependencies {
    implementation 'androidx.exifinterface:exifinterface:1.3.7'
    implementation "androidx.hilt:hilt-navigation-compose:1.2.0"

    // Persistent Mobile Foundation
    implementation 'com.persistent:base:10.0.0@aar'
    implementation 'com.persistent:liveupdate:10.0.0@aar'
    implementation 'com.persistent:push:10.0.0@aar'

    // Jetpack Compose
    implementation 'androidx.compose.ui:ui'
    implementation 'androidx.compose.ui:ui-tooling-preview'
    implementation 'androidx.compose.material3:material3:1.3.1'
    implementation 'androidx.compose.runtime:runtime'
    implementation 'androidx.activity:activity-compose:1.8.0'
    implementation 'io.coil-kt:coil-compose:2.4.0'

    implementation 'androidx.constraintlayout:constraintlayout-compose:1.1.0'
    debugImplementation 'androidx.compose.ui:ui-tooling'

    // Jetpack Navigation
    def nav_version = '2.5.3'
    implementation "androidx.navigation:navigation-fragment-ktx:$nav_version"
    implementation "androidx.navigation:navigation-ui-ktx:$nav_version"
    implementation "androidx.navigation:navigation-compose:$nav_version"

    // Kotlin
    implementation 'androidx.core:core-ktx:1.7.0'
    implementation 'androidx.appcompat:appcompat:1.4.2'
    implementation 'androidx.activity:activity-ktx:1.5.1'
    implementation 'org.jetbrains.kotlin:kotlin-reflect:1.7.10'

    // Gson
    implementation 'com.google.code.gson:gson:2.10.1'

    // Material Design 3
    implementation 'com.google.android.material:material:1.6.1'

    // Layout
    implementation 'androidx.constraintlayout:constraintlayout:2.1.4'
    implementation ('androidx.legacy:legacy-support-v4:1.0.0') {
        exclude group: 'androidx.media', module: 'media'
    }

    // Hilt Dependency Injection
    implementation "com.google.dagger:hilt-android:$hilt_version"
    kapt "com.google.dagger:hilt-android-compiler:$hilt_version"

    // Room Database
    implementation "androidx.room:room-runtime:2.6.1"
    ksp "androidx.room:room-compiler:2.6.1"
    implementation "androidx.room:room-rxjava3:2.4.3"
    implementation "net.zetetic:sqlcipher-android:4.6.1@aar"

    // JavaRX
    implementation 'io.reactivex.rxjava3:rxandroid:3.0.0'
    // Because RxAndroid releases are few and far between, it is recommended you also
    // explicitly depend on RxJava's latest version for bug fixes and new features.
    // (see https://github.com/ReactiveX/RxJava/releases for latest 3.x.x version)
    implementation 'io.reactivex.rxjava3:rxjava:3.1.5'

    // SplashScreen
    implementation 'androidx.core:core-splashscreen:1.0.0'

    // App Center
    def appCenterSdkVersion = '5.0.0'
    implementation "com.microsoft.appcenter:appcenter-analytics:${appCenterSdkVersion}"
    implementation "com.microsoft.appcenter:appcenter-crashes:${appCenterSdkVersion}"

    // Design System
    implementation "la.foton.componentes:sidsc-designsystem:0.0.21@aar"

    // Retrofit
    implementation 'com.squareup.retrofit2:retrofit:2.9.0'
    implementation 'com.squareup.retrofit2:converter-gson:2.9.0'
    implementation 'com.squareup.retrofit2:converter-scalars:2.9.0'
    implementation 'com.squareup.okhttp3:logging-interceptor:5.0.0-alpha.12'

    implementation 'com.google.android.play:review-ktx:2.0.1'

    // Tests
    testImplementation 'junit:junit:4.13.2'
    androidTestImplementation 'androidx.test.ext:junit:1.1.3'
    androidTestImplementation 'androidx.test.espresso:espresso-core:3.4.0'

    // SIGAM
    implementation ('br.gov.caixa.sigam:sigam:2.7.0.3@aar') {
        exclude group: 'androidx.work', module: 'work-runtime'
    }

    // Firebase
    implementation platform('com.google.firebase:firebase-bom:33.7.0')
    implementation 'com.google.firebase:firebase-appcheck'
    implementation 'com.google.firebase:firebase-appcheck-debug'
    implementation 'com.google.firebase:firebase-appcheck-playintegrity'
    implementation 'com.google.firebase:firebase-messaging'
    implementation 'com.google.firebase:firebase-core:21.1.1'

    implementation 'com.google.firebase:firebase-analytics-ktx'
    implementation 'com.google.android.play:integrity:1.2.0'

    // Autenticação com App Auth
    implementation 'net.openid:appauth:0.11.1'

    implementation('com.auth0.android:jwtdecode:2.0.2') {
        exclude group: 'com.android.support', module: 'appcompat-v7'
    }
    implementation 'androidx.security:security-crypto-ktx:1.1.0-alpha06'

    // Biometria
    implementation "androidx.biometric:biometric-ktx:1.2.0-alpha05"

    // DialMyApp
    implementation 'org.mbte:dialmyapp:2.4.2.010@aar'

    implementation 'com.googlecode.libphonenumber:libphonenumber:8.13.43'
    implementation 'com.google.guava:guava:33.2.1-android'
    implementation 'androidx.legacy:legacy-support-v4:1.0.0'
    implementation 'org.greenrobot:eventbus:3.3.1'
    implementation 'org.apache.cordova:framework:11.0.0'
    implementation 'androidx.webkit:webkit:1.11.0'
    implementation 'androidx.work:work-runtime:2.8.1'
    implementation 'com.google.guava:listenablefuture:9999.0-empty-to-avoid-conflict-with-guava'
    implementation 'androidx.appcompat:appcompat:1.6.1'
    implementation 'com.android.installreferrer:installreferrer:2.2'
    implementation 'com.google.android.gms:play-services-maps:17.0.0'
    implementation 'com.google.android.gms:play-services-location:17.0.0'

    // XID - Novo onboarding CAIXA
    implementation ('br.gov.caixa.siipc.xid:onboarding-sdk-android:2.4.2') {
        exclude group: 'androidx.work', module: 'work-runtime'
    }
    implementation('com.whatsapp.otp:whatsapp-otp-android-sdk:0.1.0')
    implementation('com.google.android.gms:play-services-location:21.0.1')
    implementation('androidx.datastore:datastore-preferences:1.1.7')
    implementation('com.google.crypto.tink:tink-android:1.13.0')
}

configurations.configureEach {
    resolutionStrategy {
        // A biblioteca appauth usa browser na versão 1.3.0 a qual não trata PendingIntents adequadamente
        force 'androidx.browser:browser:1.8.0'
    }
}
