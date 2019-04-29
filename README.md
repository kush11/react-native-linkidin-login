
<h3 align="center">
  🔗 React-Native LinkedIn
</h3>
<p align="center">
Simple <strong>LinkedIn</strong> login library for <strong>React-Native</strong> with <i>WebView</i> into a <i>Modal</i>
</p>
<br />


### Example

```JavaScript
// See ./example folder for details
import React from 'react'
import { StyleSheet, View } from 'react-native'

import LinkedInModal from 'react-native-linkedin'

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#fff',
    justifyContent: 'center',
    alignItems: 'center',
  },
})

export default class AppContainer extends React.Component {
  render() {
    return (
      <View style={styles.container}>
        <LinkedInModal
          clientID="[ Your client id from https://www.linkedin.com/developer/apps ]"
          clientSecret="[ Your client secret from https://www.linkedin.com/developer/apps ]"
          redirectUri="[ Your redirect uri set into https://www.linkedin.com/developer/apps ]"
          onSuccess={token => console.log(token)}
        />
      </View>
    )
  }
}
```

```javascript
const access_token // from this lib
const baseApi = 'https://api.linkedin.com/v2/me/'

const response = await fetch(
  `${baseApi}`,
  {
    method: 'GET',
    headers: {
      Authorization: 'Bearer ' + access_token
    }
  }
)
const payload = await response.json()
```