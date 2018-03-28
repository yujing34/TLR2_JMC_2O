#!/bin/csh -f
# usual.db.csh from http://zinc.docking.org
# Run this script to download ZINC
# Requires curl (default) or wget, http://wget.docking.org
#
# Thus, to run this script
#         using curl, do:     csh usual.db.csh
#         using wget, do:     csh usual.db.csh wget
#
setenv base http://zinc.docking.org/db/bysubset/2
setenv fn .zinc.$$
cat <<+ > $fn
2_0.0.db.gz
2_0.1.db.gz
2_0.10.db.gz
2_0.100.db.gz
2_0.101.db.gz
2_0.102.db.gz
2_0.103.db.gz
2_0.104.db.gz
2_0.105.db.gz
2_0.11.db.gz
2_0.12.db.gz
2_0.13.db.gz
2_0.14.db.gz
2_0.15.db.gz
2_0.16.db.gz
2_0.17.db.gz
2_0.18.db.gz
2_0.19.db.gz
2_0.2.db.gz
2_0.20.db.gz
2_0.21.db.gz
2_0.22.db.gz
2_0.23.db.gz
2_0.24.db.gz
2_0.25.db.gz
2_0.26.db.gz
2_0.27.db.gz
2_0.28.db.gz
2_0.29.db.gz
2_0.3.db.gz
2_0.30.db.gz
2_0.31.db.gz
2_0.32.db.gz
2_0.33.db.gz
2_0.34.db.gz
2_0.35.db.gz
2_0.36.db.gz
2_0.37.db.gz
2_0.38.db.gz
2_0.39.db.gz
2_0.4.db.gz
2_0.40.db.gz
2_0.41.db.gz
2_0.42.db.gz
2_0.43.db.gz
2_0.44.db.gz
2_0.45.db.gz
2_0.46.db.gz
2_0.47.db.gz
2_0.48.db.gz
2_0.49.db.gz
2_0.5.db.gz
2_0.50.db.gz
2_0.51.db.gz
2_0.52.db.gz
2_0.53.db.gz
2_0.54.db.gz
2_0.55.db.gz
2_0.56.db.gz
2_0.57.db.gz
2_0.58.db.gz
2_0.59.db.gz
2_0.6.db.gz
2_0.60.db.gz
2_0.61.db.gz
2_0.62.db.gz
2_0.63.db.gz
2_0.64.db.gz
2_0.65.db.gz
2_0.66.db.gz
2_0.67.db.gz
2_0.68.db.gz
2_0.69.db.gz
2_0.7.db.gz
2_0.70.db.gz
2_0.71.db.gz
2_0.72.db.gz
2_0.73.db.gz
2_0.74.db.gz
2_0.75.db.gz
2_0.76.db.gz
2_0.77.db.gz
2_0.78.db.gz
2_0.79.db.gz
2_0.8.db.gz
2_0.80.db.gz
2_0.81.db.gz
2_0.82.db.gz
2_0.83.db.gz
2_0.84.db.gz
2_0.85.db.gz
2_0.86.db.gz
2_0.87.db.gz
2_0.88.db.gz
2_0.89.db.gz
2_0.9.db.gz
2_0.90.db.gz
2_0.91.db.gz
2_0.92.db.gz
2_0.93.db.gz
2_0.94.db.gz
2_0.95.db.gz
2_0.96.db.gz
2_0.97.db.gz
2_0.98.db.gz
2_0.99.db.gz
2_1.0.db.gz
2_1.1.db.gz
2_1.10.db.gz
2_1.11.db.gz
2_1.12.db.gz
2_1.2.db.gz
2_1.3.db.gz
2_1.4.db.gz
2_1.5.db.gz
2_1.6.db.gz
2_1.7.db.gz
2_1.8.db.gz
2_1.9.db.gz
+
if ($#argv>0) then
     wget --base=$base -i < $fn
else
     foreach i (`cat $fn`)
          curl --url $base/$i -o $i
     end
endif
rm -f $fn
# File created on  Wed Feb 4 10:29:51 PST 2015
# This is the end of the csh script.
