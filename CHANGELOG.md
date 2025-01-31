
### 2.0.0

* Rewrote `DOMIterator` iframe related code. Added code sorting a custom array of elements by the DOM order -  can affect `markRanges()` method.
* Rewrote `unwrapMatches()` method for performance reason.
* Rewrote `getTextNodesAcross()` method (previously named as 'getTextNodesAcrossElements') to change the logic which determines does the two text nodes are separated by block element.
* Rewrote `markRanges` related code (to simplify the code).
* Changes in `mark()` and `markRegExp()` methods: the `filter` callback parameters that count mark elements has been changed to count matches. It can affect the old code that uses `acrossElements` option.
* Simplified `getSeparatedKeywords()` method.
* Got rid of empty sibling text nodes that are created when `Text.splitText()` method splits a text node at the start or/and at the end.
* Changes in RegExpCreator class:
  1. removed unnecessary escaping of characters in a RegExp character set
  2. added ability to using string instead of array in 'ignorePunctuation' option and accuracy object
  3. added code which remove duplicate from array of characters or synonyms

### 1.1.1

* Fixed bug that affect wrapping separate groups across elements with combination of `acrossElements`, `cacheTextNodes`, and `separateGroups` options
* Implemented missing `offset` property in filter callback info object with combination of `acrossElements` and `separateGroups` options
* Corrected some mistakes in TypeScript declaration files

### 1.1.0

* Added ability to extend the default boundary elements with custom elements (`blockElementsBoundary` option)

### 1.0.3

* Added TypeScript types declaration files.
* Rewrote `setupIgnoreJoinersRegExp()` method to get rid of a capturing group in `createSynonymsRegExp()` method (it breaks group/term relation when using synonyms with combinePatterns option).
* Rewrote `createDiacriticsRegExp()` method to reduce the size.
* Optimized cache object code.
* Corrected `Elements boundaries` doc.

### 1.0.2

* Initial release
