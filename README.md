# Firebase onAuthStateChanged Memory Leak
This repository demonstrates a common error in Firebase Authentication: forgetting to unsubscribe from the `onAuthStateChanged` listener.  This can lead to memory leaks and unexpected behavior. 

The `authBug.js` file contains the faulty code, missing the crucial `unsubscribe()` call.  The corrected code is in `authBugSolution.js`.  Always remember to unsubscribe when you're done with the listener to prevent resource exhaustion.