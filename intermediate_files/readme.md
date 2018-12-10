Here, we release all the intermediate data files (mostly in pkl). We wish these intermediate data files would be useful.

## codes
- around\_traffic\_mv\_avg\_15min\_1km\_completion.py: complete the missed traffic data;
- release\_traffic\_speed\_subdataset.py: the release code of the traffic speed subdataset, which may help to understand the format of the traffic speed data files (event\_traffic\_beijing\_1km\_mv\_avg\_15min\_completion.pkl);
- get\_link\_info\_feature\_beijing.py: for each link, extract link info feature;
- time\_feature\_extraction\_15min.py: time feature extraction;
- get\_query\_info\_beijing.py: get all the query information;
- release\_query\_subdataset\_beijing.py: the release code of the query subdataset. The input of this code is the same as the input of the get\_query\_info\_beijing.py, which may help to understand the format of the query;
- get\_query\_distribution\_feature\_beijing\_1km\_seq.py: get query distribution feature (algorithm 1);
- query\_distribution\_filtfilt.py: smooth the query distribution features;
- mercator\_convertor.py: interconversion between mercator and gps;

## data files  
- beijing\_bound.txt: bound of the 6th ring in Beijing;
- event\_link\_set\_all\_beijing\_1km\_filtered: set of links which are within 1km from the events. (link\_id, mercator\_x, mercator\_y);
- neighbours\_1km.txt: 1st col: link\_id, 2-11 cols: picked neighbours with PageRank in the local graph of the link_id;
- event\_link\_set\_all\_beijing\_1km\_link\_info\_feature.pkl: link info feature generated by get\_link\_info\_feature\_beijing.py;
- time\_feature\_15min.pkl: time feature generated by time\_feature\_extraction\_15min.py;
- event\_traffic\_beijing\_1km\_mv\_avg\_15min\_completion.pkl: traffic files generated by around\_traffic\_mv\_avg\_15min\_1km\_completion.py;
- event\_beijing\_extended\_filtered.txt: discovered events; (start\_time, end\_time, grid\_x, grid\_y)
- query\_beijing\_0201\_all\_information.txt: query inforamtion generated by get\_query\_info\_beijing.py; ([start\_time, end\_time, row\_grid\_id\_destination, col\_grid\_id\_destination, row\_coord\_destination, col\_coord\_destination, row\_coord\_start, col\_coord\_start])

