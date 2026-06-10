# DispatchSDK (Android)

Dispatch CDS orders SDK for Android — embeddable vehicle-orders feature
(Jetpack Compose, minSdk 24). Distributed as a binary AAR via Maven Central.

SDK заказов техники Dispatch CDS для Android. Бинарная дистрибуция через
Maven Central, исходный код — в приватном репозитории Dispatch CDS.

## Installation

```kotlin
dependencies {
    implementation("io.github.dispatchcds:dispatch-sdk:0.1.0")
}
```

## Quick start

Из любого Android-хоста (Compose не обязателен):

```kotlin
import org.dispatchcds.sdk.ui.DispatchSdkActivity

DispatchSdkActivity.launch(
    context = activity,
    token = parkApiToken,
    baseUrl = "https://YOUR-PARK-API-HOST/api",
)
```

Из Compose-хоста — экран целиком:

```kotlin
import org.dispatchcds.sdk.config.DispatchSdkConfig
import org.dispatchcds.sdk.ui.DispatchOrdersScreen

DispatchOrdersScreen(
    DispatchSdkConfig(
        baseUrl = "https://YOUR-PARK-API-HOST/api",
        tokenProvider = { parkApiToken },
        onClose = { /* пользователь закрыл виджет */ },
    )
)
```

## Доступ

Использование SDK требует договора с Dispatch CDS и токена Park API.
Контакт: dispatch@bi.group. Лицензия: см. LICENSE.
