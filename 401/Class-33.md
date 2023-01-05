# Next- Forms and Conditional Rendering 


## Building Your Own Hooks

Building your own Hooks lets you extract component logic into reusable functions.

## Extracting a Custom Hook

A custom Hook is a JavaScript function whose name starts with ”use” and that may call other Hooks. For example, `useFriendStatus` below is our first custom Hook:

```
import { useState, useEffect } from 'react';

function useFriendStatus(friendID) {
  const [isOnline, setIsOnline] = useState(null);

  useEffect(() => {
    function handleStatusChange(status) {
      setIsOnline(status.isOnline);
    }

    ChatAPI.subscribeToFriendStatus(friendID, handleStatusChange);
    return () => {
      ChatAPI.unsubscribeFromFriendStatus(friendID, handleStatusChange);
    };
  });

  return isOnline;
}

```



