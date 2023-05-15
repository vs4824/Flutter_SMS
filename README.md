# Flutter SMS

Flutter Plugin for sending SMS and MMS on Android and iOS. If you send to more than one person it will send as MMS. On the iOS if the number is an iPhone and iMessage is enabled it will send as an iMessage.

## How To Use

You can send multiple ways:

1. Message and No People

2. People and No Message

3. Message and People

This will populate the correct fields.

## Example

Make sure to Install and Import the Package.

   ```import 'package:flutter_sms/flutter_sms.dart';```

Create a function for sending messages.

   ```
   void _sendSMS(String message, List<String> recipents) async {
 String _result = await sendSMS(message: message, recipients: recipents)
        .catchError((onError) {
      print(onError);
    });
print(_result);
}
   ```

You can quickly send the message with this function.

   ```
   String message = "This is a test message!";
List<String> recipents = ["1234567890", "5556787676"];

_sendSMS(message, recipents);
   ```
