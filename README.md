# Reproducer for Safari bug concerning video element with object-fit: cover

This repository illustrates a bug in Safari on iOS 17.5.1 where setting `object-fit: cover` style on a video element is not applied, depending on the value of some padding on the enclosing element.

For instance, if the padding on the element is set to `15px`, the `object-fit: cover` is not applied. Resetting the `object-fit: cover` on the element, after briefly setting it to some other value (like `contain`), resolves the state.

Apparently the behavior is in some way related to value of the padding. Setting it to some slightly different value like `16px` also does not trigger the issue.
