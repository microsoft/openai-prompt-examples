
# Information extraction from claim phone conversations

This example extracts claim-relevant information from a phone conversation that has been transcribed with e.g., [Azure Speech API](https://learn.microsoft.com/en-us/azure/cognitive-services/speech-service/speech-to-text).

## Prompt settings

| Setting | Value |
|---|---|
| Engine | `text-davinci-002` |
| Temperature | `0.7` |

## Prompt text

```
You must extract the following information from the phone conversation below:

1. Call reason (key: reason)
2. Cause of the incident (key: cause)
3. Names of all drivers as an array (key: driver_names)
4. Insurance number (key: insurance_number)
5. Accident location (key: location)
6. Car damages as an array (key: damages)
7. A short, yet detailed summary (key: summary)

Make sure fields 1 to 6 are answered very short, e.g. for location just say the location name.

Please answer in JSON machine-readable format, using the keys from above.
Format the ouput as JSON object called "results". Pretty print the JSON and make sure that is properly closed at the end.

Phone conversation:
Hi I just had a car accident and wanted to report it. OK, I hope you're alright, what happened? I was driving on the I-18 and I hit another car. Are you OK? Yeah, I'm just a little shaken up. That's understandable. Can you give me your full name? Sure, it's Sarah standl. Do you know what caused the accident? I think I might have hit a pothole. OK, where did the accident take place? On the I-18 freeway. Was anyone else injured? I don't think so. But I'm not sure. OK, well we'll need to do an investigation. Can you give me the other drivers information? Sure, his name is John Radley. And your insurance number. OK. Give me a minute. OK, it's 546452. OK, what type of damages has the car? Headlights are broken and the airbags went off. Are you going to be able to drive it? I don't know. I'm going to have to have it towed. Well, we'll need to get it inspected. I'll go ahead and start the claim and we'll get everything sorted out. Thank you!
```