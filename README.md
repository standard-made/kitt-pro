**<h1> kitt.pro | chat-gpt</h1>**
![Kitt.Pro](/assets/kitt_pro_readme.png "Kitt.Pro by STANDARDmade, LLC")



## <span style="color:#555555"><u> **OVERVIEW** </u></span>
[kitt.pro](https://kitt.pro) [`Flutter Productivity App`] - COMING SOON
by STANDARDmade, LLC
- Flutter & Dart
  - OpenAI Stuff
  - Chat-GPT Stuff
  - :taco: Stuff


## <span style="color:#555555"><u> **POINTS OF CONTACT** </u></span>
If any issues arise for any of the below mentioned areas, please draft a strongly worded email and never send it to: **kitt@made.llc** 



## <span style="color:#555555"><u> **CORE SOLUTIONS** </u></span>
| Stack  | Versions |
| ------------- |:-------------:|
| Flutter | ^0.13.5 |
| Firebase Core | ^2.4.1 |
| OpenAI | v1 |
| Learning Model | text-davinci-003 |



## <span style="color:#555555"><u> **CORE DEVELPOMENT** </u></span>
**kitt.pro |** by STANDARDmade, LLC + :taco::taco::taco:


``` dart
// GENERATE RESPONSE FROM OPENAI [dart]
class ChatPage extends StatefulWidget {
  const ChatPage({super.key});

  @override
  State<ChatPage> createState() => _ChatPageState();
}

Future<String> generateResponse(String prompt) async {
  const apiKey = apiSecretKey;

  var url = Uri.https("api.openai.com", "/v1/completions");
  final response = await http.post(
    url,
    headers: {
      'Content-Type': 'application/json',
      "Authorization": "Bearer $apiKey"
    },
    body: json.encode({
      "model": "text-davinci-003",
      "prompt": prompt,
      'temperature': 0,
      'max_tokens': 2000,
      'top_p': 1,
      'frequency_penalty': 0.0,
      'presence_penalty': 0.0,
    }),
  );

  // Do something with the response
  String utf8Body = utf8.decode(response.bodyBytes);

  // Decode the JSON string
  Map<String, dynamic> newresponse = jsonDecode(utf8Body);

  return newresponse['choices'][0]['text'];
}
```
:taco::taco::taco:
</details>