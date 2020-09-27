1. Suspicious large data transfer from web-server
You can find a suspicious large volume of data transfer in your Kibana dashboard.

![](images/hunting-1.png)
![](images/hunting-2.png)

2. Suspicious source country
Once you click the suspicious data transfer, you can see the connection came from North Korea. 
![](images/hunting-3.png)

3. Apply source country filter
![](images/hunting-4.png)

4. Confirm critical WAF alerts from North Korea
You can confirm critical alerts were detected but WAF triggered alarms only because it is configured the 'Transparent mode'. 
![](images/hunting-5.png)

5. Suspicious login
North Korean attacker logged in to the 'website' with legitimate ID(James).
![](images/hunting-6.png)

Clear the pre-applied country filter and apply a new filter - 'username:james' 
![](images/hunting-7.png)

You can confirm that ID ‘James’ normally login from ‘Russia’. Now, you suspect this ID could be stolen by the attacker. 
![](images/hunting-8.png)

6. Confirm detailed attack techniques
You can find how the attacker exfiltrated the data. 
![](images/hunting-9.png)
