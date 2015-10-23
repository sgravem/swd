# SWD data crunching for WSN

##Questions for Sarah
23 October 2015

1. OK to have public repository?
2. Should I rename columns, or should Sarah?
3. Should I follow the order of analyses you did?
4. Increase in bed depth - why so many blank cells?
5. How to treat blank cells - NA?
6. Please send me link to google drive
7. Should locationID include distance above bolt?
8. Do we want site as a fixed effect?
  * or latitude?  
  * eventually, site should be a random effect, nested within region (a fixed effect)
9.  

## Models

1. Bed depth ~ distance * time + random(site, transect)
2. Increase in bed depth ~ distance * time + random(site, transect)
  * Is increase relative to time 0?
3.  Mussel recruit density ~ distance * time + random(site, transect)
4.  Increase in mussel recruit density ~ distance * time + random(site, transect)
5.  
