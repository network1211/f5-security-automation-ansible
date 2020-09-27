
### Create 'Web Access' monitoring map

   *Kibana, Maps -> New map*
    ![](images/dashboaard-map-1.png)

   *Add Layer -> Select 'World countries' -> Name (Web Access)*
    ![](images/dashboaard-map-2.png)

   *'Tooltip fields' -> 'Add' -> Select 'name'*
    ![](images/dashboaard-map-3.png)

   *'Term Joins' -> 'Add' -> 'Left source(Web Access)' -> Left field(ISO 3166-1 alpha-2 code) -> Right source(f5bd-elk) -> Right field(geoip.country_code2.keyword)*
    ![](images/dashboaard-map-4.png)

   *Set time range from '27th Apr 2020 @ 00:00:00' to '2nd May 2020 @ 00:00:00'.*
    ![](images/dashboaard-map-5.png)

   *Verify your map is similar with the below* 
    ![](images/dashboaard-map-6.png)

   *Save your map*
    ![](images/dashboaard-map-7.png)

   *Verify your map*
    ![](images/dashboard-map-8.png)
