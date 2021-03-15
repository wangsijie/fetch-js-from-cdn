# FETCH-JS-FROM-CDN

## Usage

```jsx
import React, { useRef } from 'react';
import fetchJSFromCDN from 'fetch-js-from-cdn';

export default function() {
    const jQueryRef = useRef(null);
    useEffect(() => {
        fetchJSFromCDN(
            'https://code.jquery.com/jquery-3.6.0.min.js',
            '$',
        ).then(instance => jQueryRef.current = instance);
    }, []);

    return null;
}
```