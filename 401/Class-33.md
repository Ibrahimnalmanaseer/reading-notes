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


it’s just like a normal function. Its name should always start with use so that you can tell at a glance that the rules of Hooks apply to it.


The purpose of our useFriendStatus Hook is to subscribe us to a friend’s status. This is why it takes friendID as an argument, and returns whether this friend is online



## Using a Custom Hook




