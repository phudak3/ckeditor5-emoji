# CKEditor 5 Emoji plugin

[![npm](https://img.shields.io/npm/v/@phudak/ckeditor5-emoji)](https://www.npmjs.com/package/@phudak/ckeditor5-emoji)
[![npm](https://img.shields.io/npm/dw/@phudak/ckeditor5-emoji)](https://www.npmjs.com/package/@phudak/ckeditor5-emoji)
[![npm bundle size](https://img.shields.io/bundlephobia/min/@phudak/ckeditor5-emoji)](https://www.npmjs.com/package/@phudak/ckeditor5-emoji)
[![NPM](https://img.shields.io/npm/l/@phudak/ckeditor5-emoji)](https://www.npmjs.com/package/@phudak/ckeditor5-emoji)


Emoji plugin using a modified version of the ckeditor5 SpecialCharacters plugin.

![Preview Image](preview.png "Preview Image")

## Setup

1. Installation

To install it, run:

```javascript
npm i --save @phudak/ckeditor5-emoji
```

2. Importing modules

Import the Emoji plugin with all optional categories. If you want to exclude some category, don't import it.

```javascript
import {
    Emoji, EmojiActivity, EmojiFlags, EmojiFood, EmojiNature, EmojiObjects, EmojiPeople,
    EmojiPlaces, EmojiSymbols
} from '@phudak/ckeditor5-emoji/src';
```

3. Add imported modules to plugins 

Add the Emoji plugin and optional categories to CKEditor plugins.

Add plugin to build:

```javascript
InlineEditor
    .create( document.querySelector( '#editor' ), {
        plugins: [
            ...,
            Emoji,
            EmojiPeople,
            EmojiNature,
            EmojiPlaces,
            EmojiFood,
            EmojiActivity,
            EmojiObjects,
            EmojiSymbols,
            EmojiFlags,
        ],
    } )
    .then( editor => {
        window.editor = editor;
    } )
    .catch( err => {
        console.error( err.stack );
    } );
```

**or** add plugin to custom editor builder:

```javascript
InlineEditor.builtinPlugins = [
    ...
    Emoji,
    EmojiPeople,
    EmojiNature,
    EmojiPlaces,
    EmojiFood,
    EmojiActivity,
    EmojiObjects,
    EmojiSymbols,
    EmojiFlags,
]
```

4. Add the Emoji plugin to toolbar

Add plugin to build:

```javascript
InlineEditor
    .create( document.querySelector( '#editor' ), {
        plugins: [...],
        toolbar: [ ... , 'emoji' ],
    } )
    .then( editor => {
        window.editor = editor;
    } )
    .catch( err => {
        console.error( err.stack );
    } );
```

**or** add plugin to custom editor builder:

```javascript
InlineEditor.defaultConfig = {
    toolbar: {
        items: [
            ...,
	    'emoji',
	    '|',
	    'undo',
	    'redo'
	]
    },
};
```

5. Enjoy

### Integration examples

You can check my Emoji plugin integration into custom CKEditor builds here:

- [@phudak/ckeditor5-build-inline-simple](https://www.npmjs.com/package/@phudak/ckeditor5-build-inline-simple)
- [@phudak/ckeditor5-build-inline-basic](https://www.npmjs.com/package/@phudak/ckeditor5-build-inline-basic)
- [@phudak/ckeditor5-build-inline-full](https://www.npmjs.com/package/@phudak/ckeditor5-build-inline-full)

## Emoji Set

Emoji are divided into categories:

- All
- Activity
- Food
- Flags
- Nature
- Objects
- People
- Places
- Symbols

You can choose specific categories or import all of them.




