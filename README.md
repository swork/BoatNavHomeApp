# BoatNavHomeApp
 Landing/start page for boat nav tablet, as PWA
 
 PWA means automatic "caching" of components I write. But what I want is automatic caching of external components too.
 
 Initial cheat: expose both native (out in the world) and offline (local) links for all resources (tide tables, Coast Pilot links etc.). Upcoming if I ever get to it, generic storage interface for offline docs like these with an update link.

# Problems

Oh peepee. It works on desktop, works on phone (can turn off network and load offline links) but doesn't work on Samsung tablet's Chrome ("You're not connected to the Internet" - duh fucker, this was the whole point). Seems likely I need to write the whole thing from low levels. -- Or install with Firefox, which DOES maintain app operation when offline. Okay, good enough.

# Directions

Subsequent to the initial cheat I'd like at-sea access to content schema changes. I think it's okay to specify on/off-line explicitly, if that becomes necessary (else discovering youre offline when you think you've been online probably involves a timeout, annoying).

Hard to know whether I need file system access (store PDFs as files and link to them with file:://whatever.pdf URLs) or blob store (shelve PDF content in LocalStorage and .innerHTML=blob, if that works).
