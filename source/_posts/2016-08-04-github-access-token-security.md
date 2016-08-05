title: Github Access Token Automatically Revoked If Exposed
date: 2016-08-04 17:06:38
categories:
- Fragments
---
By accident (dangerous action) I found out an interesting fact that ** your Github access token will be automatically revoked if it was exposed in any public repository. **

I tested it few more times and found more details:
- Access token will be immediately revoked after the push of a commit that contains the explicit text.
- Access token will be revoked whatever public repo the explicit text was in or whoever committed it (Updated: private repo won't, thanks for help from Rong and Yanzhe:)).
- The match of access token is explicit as a string starts/ends with EOF or space or brackets. For example, assume you have an access token ABC:
	* "ABC" will be detected.
	* "xABCx" will not.
	* "/ABC" will not.
	* "[ABC]" or "(ABC)" will.

This detect and revoke mechanism out of security concern is obviously great, the question is how Github does it so efficiently with the enormous amount of access tokens and commits? The best algorithm I can figure out is using alphabet tree with map reduce, hope I could get answer from someone work for Github someday.