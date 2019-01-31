# OT

## Research Papers
- [Real Differences between OT and CRDT for Co-Editors (arXiv18 by Sun)](https://arxiv.org/pdf/1810.02137.pdf)

## Survey
- [OT FAQ maintained by Chengzheng Sun](http://www3.ntu.edu.sg/home/czsun/projects/otfaq/#_What_is_the_11)

```
This is a must-read article.
```

- [Operational transformation (wiki)](https://en.wikipedia.org/wiki/Operational_transformation)

```
It is quite comprehensive.
```

- [List of collaborative software (wiki)](https://en.wikipedia.org/wiki/List_of_collaborative_software)

- [Collaborative real-time editor](https://en.wikipedia.org/wiki/Collaborative_real-time_editor)

## OT Technique
- [Whitepage: Google Wave Operational Transformation](https://github.com/scrosby/fedone/blob/master/whitepapers/operational-transform/operational-transform.rst)

- [Real Time Collaboration Technology Roundup](https://irisate.com/collaborative-editing-solutions-round-up/)

```
It contains several video talks.
It describes OT and CRDT.

It introduces "Flip":

Ohmstudio is the first "heavy" app featuring 'Google Docs-style' synchronous collaborative editing. 
But it doesn't rely on any Operational Transform or CRDT framework to perform concurrent editing. 
Those are simply not adapted for the complexity and the performance it needs.

Instead it's powered by Flip groundbreaking algorithms. 
And we're proud to say it's confirmed to be rock solid!
```

- [Real Time Collaboration: Flip @ Youtube](https://www.youtube.com/watch?v=W0kQ1um9X6w)

```
Raphaël Dingé (CTO from Irisate and creator of Flip Concurrent Editing Libraries)
gives an overlook of Flip "compare and swap" approach to Collaborative Editing
```

- [Irisate Blog](https://irisate.com/blog/)

```
It is a blog devoted to collaborative editing systems.
```

## Collaborative Editors

### Known to be OT-based
- [SubEthaEdit 5 (Code, Write, Edit. Together.)](https://subethaedit.net/)
  - [subethaedit/SubEthaEdit @ github](https://github.com/subethaedit/SubEthaEdit)

  ```
  General purpose plain text editor for macOS. Widely known for its live collaboration feature. 

  Thanks to the Xerox Parc Jupiter Project for Transactional Transformations.
  ```

- [FirebaseExtended/firepad](https://github.com/FirebaseExtended/firepad)

```
Collaborative Text Editor Powered by Firebase
```

See [firepad/lib/text-operation.js](https://github.com/FirebaseExtended/firepad/blob/master/lib/text-operation.js)
for OT.

  - [Announcing Firepad - Our Open Source Collaborative Text Editor](https://firebase.googleblog.com/2013/04/announcing-firepad-our-open-source.html)
  ```
  Firepad provides true collaborative editing, complete with intelligent OT-based merging and conflict resolution.
  It’s full-featured and has support for both rich text and code editing.
  ```
  - [FirePad Demo](https://demo.firepad.io/#EBDXy0X62z)

- [Etherpad](http://etherpad.org/)

```
Etherpad is a highly customizable Open Source online editor 
providing collaborative editing in really real-time.
```
  - [ether/etherpad-lite @ github](https://github.com/ether/etherpad-lite)

  ```
  Etherpad: Really real-time collaborative document editing
  ```

  - [Etherpad (wiki)](https://en.wikipedia.org/wiki/Etherpad)

  ```
  Merging of changes is handled by operational transform.
  A "time slider" feature allows anyone to explore the history of the pad. 
  ```


### Known to be CRDT-based

## Collaborative Systems Development

- [Convergence](https://convergence.io/)

```
Introducing the revolutionary API for building realtime collaborative applications.
```

- [SwellRT/swellrt](https://github.com/SwellRT/swellrt)

```
The main feature of SwellRT is realtime storage based in objects.
They can be shared among participants that can mutate them in realtime. 
All changes are persisted and propagated transparently. 
Object's state is eventually consistent.
```

### Known to be OT-based
- [Google Realtime API](https://developers.google.com/realtime/overview)

```
The Realtime API is deprecated as of November 28, 2017.

The Google Realtime API provides collaboration as a service for files 
in Google Drive via the use of **operational transforms**. 

The API is a JavaScript library hosted by Google 
that provides collaborative objects, events, and methods for creating collaborative applications.
```

  - [(Issue #108 of jupyterlab/jupyterlab-google-drive) Deprecation of the Google Realtime API](https://github.com/jupyterlab/jupyterlab-google-drive/issues/108)

  ```
  It mentions many alternatives.
  ```
- [share/sharedb](https://github.com/share/sharedb)

```
ShareDB is a realtime database backend based on Operational Transformation (OT) of JSON documents. 
It is the realtime backend for the DerbyJS web application framework.
```

### Known to be CRDT-based
