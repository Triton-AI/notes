# notes
TTL's 
Spline trajectory - automatic. More explanation later.

Offline-trajectory-tools: 

Running TTL tools - there's a readme in the repo.

3 yaml files - the bounds, main regions, pit regions. They have gps coordinates or .kml files from google earth that got converted. Then convert them to enu.
Once your files are in enu format, this trajectory optimizer will work.
Note - all paths are hard-coded. Be careful where you run it from.
We have specific regions for the pit which get encoded in the ttl. When the car gets to that region, it knows what to do.

#of nodes - specify exactly where each node goes. Those are splines, and you have to edit manually where the splines go. Don't worry about banking, especially for the go-kart. You can drag-and-drop over the reference line, and fine-tune based on boundaries. There are a lot of reference lines you can make from google maps. These lines may not be optimal, but they will do exactly what you want where you want. And with you can make them really good.

Then, set waypoint interval for the actual TTL - then you're good to go. Next, add the GPS origin, and add in the normals. 
Then you can view the regions on google earth. It is pretty accurate but not perfect.

Setting bounds: - for preparing the regions you can use google earth. Usually we collect regions in person as well for better accuracy. 

3 columns - inside bound, outside bound, centerline. We aren't using bank angle.
We define things like the points interval, acceleration/deceleration lookups, etc in the .yaml file.

Old ttl's exist in racecommon/src/common.race_metadata.ttl's. For the gokart branch specifically we have 3 ttl's.

Note - pacejka is a tire modeling formula, useful for solving coefficients of friction/rolling resistance.
