# angular-cordova-cardio
Angular wrapping for cordova cardIO plugin (http://plugins.cordova.io/#/package/com.keepe.cardio)

 - ``` $ cordova plugin add https://github.com/vkeepe/card.io.git ``` - To install cordova module
 - See more information about how to configure cordova plugin in config xml for Android
 
Module provide next functionallity

- ``` $cordovaNgCardIOProvider (Provider for configure)```
- ```$cordovaNgCardIO (Service)```

``` 
$cordovaNgCardIOProvider.setScanerConfig(
  {
         "expiry": true,
         "cvv": true,
         "zip": false,
         "suppressManual": false,
         "suppressConfirm": false,
         "hideLogo": true
  }
);
```

```
$cordovaNgCardIOProvider.setCardIOResponseFields(
  [
        "card_type",
        "redacted_card_number",
        "card_number",
        "expiry_month",
        "expiry_year",
        "cvv",
        "zip"
      ]
)
```

```
$cordovaNgCardIO.canCard().then(
        function (response) {
          alert(JSON.stringify(response));
        }
      );
```


 
 
