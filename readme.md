# (google-translator) Google Translator API for FREE

Translate with google for FREE without *API key* 

## Installation

npm install google-translator

## Usage

```javascript
var translator = require('google-translator');

/*
Translate 'Hello'
from	:	English
to		:	French
*/

translator('en' ,'fr' ,'Hello' ,response => {
	console.log(response);
});
```

You may also pass `undefined` as the origin language to have Google Translate auto-detect the input. For example:

```javascript
translator(undefined, 'en', 'ありがとう ございます', response => {
    // Process the response here
});
```

This will autodetect the language as Japanese and translate it from Japanese into English.

output :

```
{
    "text":"Bonjour",
    "isCorrect":true,
    "source":{
        "synonyms":[
            [
                "howdy",
                "hullo",
                "hi",
                "how-do-you-do"
            ]
        ],
        "pronunciation":[
            "heˈlō,həˈlō"
        ],
        "definitions":[
            {
                "type":"noun",
                "definitions":[
                    {
                        "definition":"an utterance of “hello”; a greeting.",
                        "example":"she was getting polite nods and hellos from people"
                    }
                ]
            },
            {
                "type":"exclamation",
                "definitions":[
                    {
                        "definition":"used as a greeting or to begin a telephone conversation.",
                        "example":"hello there, Katie!"
                    }
                ]
            },
            {
                "type":"verb",
                "definitions":[
                    {
                        "definition":"say or shout “hello”; greet someone.",
                        "example":"‘Hi Kirsten,’ he helloed , obviously calling me Kirsten on purpose."
                    }
                ]
            }
        ],
        "examples":[
            "But - hello - they're only 15, and they're only playing at being grown up.",
            "You are supposed to be able to keep up with my voice, hello !",
            "I said hello to him",
            "She must have been really stupid to have mimicked me… I mean, hello !",
            "So Bob, if you are out there, drop in and say hello !",
            "I mean - hello - this is just kind of a witty, fun movie.",
            "I mean, not that we have that all the time, coz hello !",
            "Umm… hello , the world just ended, everyone seems bizarrely unaffected, like the predicted deep freeze has already reached their brains.",
            "I have wanted to re-watch it like a DVD or something, but I couldn't because, hello !",
            "I yelled hello upstairs as I began to head up to see if I could help Mrs. Bishop out.",
            "It was a pleasant surprise when Sheila Sheridan came over to say hello .",
            "I haven't seen her in over a year, and yesterday she just strolls casually up to me and says hello !",
            "A man standing in line at the check-out counter of a grocery store was surprised when an attractive woman behind him said hello .",
            "I was stunned and I said I'm surprised anyone says hello to me ever in the mall or in the store after reading that.",
            "They sit in classrooms and cannot hear the teachers so, hello , it is no surprise that we are unable to get good outcomes from our education system.",
            "Quentin is surprised to see Maggie, and says hello .",
            "Ships' horns toot, children wave and call hello , and every morning you're awakened by the haunting call of the muezzin from some distant village mosque.",
            "Logan didn't say hello , but I hadn't expected a greeting.",
            "hello! did you even get what the play was about?",
            "We didn't get the chance to get together this visit, but we had nice phone conversation and a waved hello .",
            "But we had a surprise in store for Caroline when we said hello after the show.",
            "She whispered hello , then began to make her way to her room, where she hoped to take a nap.",
            "hello, what's this?",
            "Okay, so maybe costs rose by more than 1% in that period, and maybe sales dropped earlier in the year, but hello !",
            "My second thought is, hello , it's still snowing!",
            "It is extraordinary how much can be achieved when you put enthusiasm into a routine task, a special project or a simple hello or conversation.",
            "Like we have time for a life - hello !",
            "I thought it summed up what I wanted to say and it also is a way to say hello !",
            "Tlingit people do not use such greetings as hello , good-bye, good afternoon, or good evening.",
            "hello there, Katie!"
        ]
    },
    "target":{
        "synonyms":[
            "Bonjour!",
            "Salut!",
            "Tiens!",
            "Allô!"
        ]
    },
    "translations":[
        {
            "type":"interjection",
            "translations":[
                [
                    "Bonjour!",
                    [
                        "Hello!",
                        "Hi!",
                        "Good morning!",
                        "Good afternoon!",
                        "How do you do?",
                        "Hallo!"
                    ]
                ],
                [
                    "Salut!",
                    [
                        "Hi!",
                        "Hello!",
                        "Salute!",
                        "All the best!",
                        "Hallo!",
                        "Hullo!"
                    ]
                ],
                [
                    "Tiens!",
                    [
                        "Hallo!",
                        "Hello!",
                        "Hullo!",
                        "Why!"
                    ]
                ],
                [
                    "Allô!",
                    [
                        "Hello!",
                        "Hullo!",
                        "Hallo!"
                    ]
                ]
            ]
        }
    ]
}
```

Wrong sentences
```javascript
var translator = require('google-translator');

translator('en' ,'fr' ,'helloe' ,response =>{		
	if(response.isCorrect==false){
		console.log('did you mean : %s ?',response.text);
	}
});
```
output :
```
Did You Mean : hello ?
```

List of all available languages

```javascript
var translator = require('google-translator');

console.log(translator.languages);
```
output :

```
{
	af: 'Afrikaans',
	sq: 'Albanian',
	ar: 'Arabic',
	az: 'Azerbaijani',
	eu: 'Basque',
	bn: 'Bengali',
	be: 'Belarusian',
	bg: 'Bulgarian',
	ca: 'Catalan',
	'zh-cn': 'Chinese Simplified',
	'zh-tw': 'Chinese Traditional',
	hr: 'Croatian',
	cs: 'Czech',
	da: 'Danish',
	nl: 'Dutch',
	en: 'English',
	eo: 'Esperanto',
	et: 'Estonian',
	tl: 'Filipino',
	fi: 'Finnish',
	fr: 'French',
	gl: 'Galician',
	ka: 'Georgian',
	de: 'German',
	el: 'Greek',
	gu: 'Gujarati',
	ht: 'Haitian Creole',
	iw: 'Hebrew',
	hi: 'Hindi',
	hu: 'Hungarian',
	is: 'Icelandic',
	id: 'Indonesian',
	ga: 'Irish',
	it: 'Italian',
	ja: 'Japanese',
	kn: 'Kannada',
	ko: 'Korean',
	la: 'Latin',
	lv: 'Latvian',
	lt: 'Lithuanian',
	mk: 'Macedonian',
	ms: 'Malay',
	mt: 'Maltese',
	no: 'Norwegian',
	fa: 'Persian',
	pl: 'Polish',
	pt: 'Portuguese',
	ro: 'Romanian',
	ru: 'Russian',
	sr: 'Serbian',
	sk: 'Slovak',
	sl: 'Slovenian',
	es: 'Spanish',
	sw: 'Swahili',
	sv: 'Swedish',
	ta: 'Tamil',
	te: 'Telugu',
	th: 'Thai',
	tr: 'Turkish',
	uk: 'Ukrainian',
	ur: 'Urdu',
	vi: 'Vietnamese',
	cy: 'Welsh',
	yi: 'Yiddish'
}
```
