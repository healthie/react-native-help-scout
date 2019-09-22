# React Native Help Scout

Help Scout's Beacon for React Native.

## Installation

```sh
yarn add react-native-help-scout
```

## iOS

Please visit https://developer.helpscout.com/beacon-2/ios/#additional-setup and complete the steps

## Usage

```javascript
import { Beacon } from 'react-native-help-scout'

// Initialize Beacon
Beacon.init('beacon-id')

// Open Beacon
Beacon.open()

// Set user information in Beacon
Beacon.identify({
	email: 'joshuaheywood@live.com',
	name: 'Joshua Heywood',
	company: 'Megatronic',
	jobTitle: 'Marketing Manager',
})

// Unset user information in Beacon
Beacon.logout()

// Navigate to a specific screen
Beacon.navigate('/ask/message/')

// Open with search
Beacon.search('hipaa')

// Open article
Beacon.openArticle('DOCS_ARTICLE_ID')

// Dismissing the Beacon
Beacon.dismiss(() => console.log('Beacon dismissed'))

// Event handlers
const openHandler = () => console.log('Beacon opened')
Beacon.on('open', openHandler)
Beacon.off('open', openHandler)
Beacon.off('open')
Beacon.once('open', () => console.log('This will only get called the first time the open event is triggered'))

const closeHandler = () => console.log('Beacon closed')
Beacon.on('close', closeHandler)
Beacon.off('close', closeHandler)
Beacon.off('close')
Beacon.once('close', () => console.log('This will only get called the first time the close event is triggered'))
```