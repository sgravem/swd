# SWD data crunching for WSN

##Questions for Sarah
23 October 2015

1. OK to have public repository?
A. I'd rather keep the data at least within the SSWD group. I've already been asked to take things down from google drive by a collaborator. 
2. Should I rename columns, or should Sarah?
A. Go ahead and rename what you need, but change it on the metadata so we keep track
3. Should I follow the order of analyses you did?
A. No, those were suggestions for you. Do what you think is most appropriate.
4. Increase in bed depth - why so many blank cells?
A. Because 1) can't have an increase at the first time point, 2) Jennifer hasn't given me her data. Hopefully she will give it to me very soon
5. How to treat blank cells - NA?
A: Yes. All blank cells are NA
6. Please send me link to google drive
A: It should be in your shared folders. The data on Gdrive aren't necessarily the most updated bc I've been asked not to share some people's data publicly, but the methods are accurate at least for HMS and Bodega Sites. Here is the link https://drive.google.com/drive/u/0/folders/0ByqPe4LWWImCVFlSeFhubG9UNVU
7. Should locationID include distance above bolt?
A. It does. Distance above blot is the last entry in location ID
8. Do we want site as a fixed effect?

  * or latitude?  
  * eventually, site should be a random effect, nested within region (a fixed effect)
A. I have been thinking of site as fixed since we're intersted in where the strongest patterns are occurring geographically. I'm happy to substitute latitude for site or use region as the fixed effect, with site nested within region. There may be some features of site that are important though, such as wave action. We can try it both ways?
9.  For now, are we ignoring mussel length strategy? 
A. I think that Jennifer's mussel length strategy designations are wrong. I'm waiting for her reply on this. I will clean up her data after I know. For the Bodega sites I removed all entries for average length where the "5 biggest" strategy was used since it's not comparable with the "4 corners" strategy. 
10. Include sea star density as covariate (better yet, estimate of reduction in star density?)
A. Yes this would be ideal. However, I think we only have good estimates for HMS and SHB and none of the other sites. Any ideas on how to get around this problem? 
11. I think we should focus on absolute estimates, not change (for now)
A. That's fine. I was hoping the changes would show some clear and simple patterns but they don't. We can drop them for now. 

## Models

1. Bed depth ~ distance * time + random(site, transect)
2. Increase in bed depth ~ distance * time + random(site, transect)
  * Is increase relative to time 0? A. No it's relative to the previous time point, but we could add a column that is relative to time 0. Do you think this will be better than just testing bed depth? 
3. Mussel recruit density ~ distance * time + random(site, transect)
4. Increase in mussel recruit density ~ distance * time + random(site, transect)
  * relative to the first recruitment measure?  not sure why we need this A. No it's relative to the previous time point, but we could add a column that is relative to time 0. I was investigating when and where recruit pulses were happening, which could be interesting but is not a priority right now. 
5. Mussel size ~ distance * time + random(site, transect, quadrat) Q: why is quadrat included in this model but not the others? 
