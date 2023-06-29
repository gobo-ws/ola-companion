**How-to control Shelly relays with Companion**  

    
Create a new custom variable and name it "Shelly_hostname".  
Add the Shelly device's hostname or IP address to both the 'Current value' and 'Startup value' fields.  
  
Shelly output on:  
  
Add a new button with the press action: http POST  
URL:  
`http://$(internal:custom_Shelly_hostname)/rpc/Switch.Set`  
  
Body:  
`{"id":0, "on":true}`  
  
Content Type:  
`application/json`  
  
************************************************************  
  
Shelly output off:  
  
Add a new button with the press action: http POST  
URL:  
`http://$(internal:custom_Shelly_hostname)/rpc/Switch.Set`  
  
Body:  
`{"id":0, "on":false}`  
  
Content Type:  
`application/json`  
  
  
  
If you are using a device with multiple outputs, id 0 represents the first output. For the second output, assign id 1, and continue incrementing the ID for each subsequent output.  
  
/Johan
