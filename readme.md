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
            "he?l?,h??l?"
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
			...
		]
    },
    "target":{
        "synonyms":[
            "Bonjour!",
			...
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
