</h> SIEM Visualization: Users Added Or Removed From a Local Group Within a Specific Timeframe </h>
<h2>Description</h2>
In this project, I will create a SIEM visualization that monitors user additions or removals from the local "administrator" group from 3/5/23 to the present time.
<br />
<h2>Languages and Utilities Used</h2>
- <b>VirtualBox</p>
- <b>Elastic</b>
<h2>Environments Used </h2>
- <b>Windows 10</b> 
<h2>Project walk-through:</h2>
</p> 1. After logging into Elastic, I click "edit" for the dashboard titled "SOC-alerts"
<img width="1423" alt="Screenshot 2024-06-26 at 12 55 52 PM" src="https://github.com/bpark1223/SIEM-Visualization-Successful-RDP-Logon-Related-To-Service-Accounts/assets/77799235/14692955-9bc3-40b3-9a67-ba58370c77ae">
</p> 2. I click "create visualization" after which I will be able to customize my settings and filter
<img width="1428" alt="Screenshot 2024-06-26 at 1 04 26 PM" src="https://github.com/bpark1223/SIEM-Visualization-Successful-RDP-Logon-Related-To-Service-Accounts/assets/77799235/25cab8a8-d348-4b4f-9b2d-f731d156c6b4">
</p> 3. To display user additions or removals from the local "Administrators" group I use a filter to only consider event IDs that match 4732 – A member was added to a security-enabled local group and 4733 – A member was removed from a security-enabled local group</p>
<img width="1427" alt="Screenshot 2024-06-26 at 4 18 58 PM" src="https://github.com/bpark1223/SIEM-Visualization-Users-Added-Or-Removed-From-A-Local-Group-Within-A-Specific-Timeframe-/assets/77799235/0cc72e0d-f4cb-4e2d-809b-9ddb041f36f6">
</p> 4. Also, I create another filter to output event ID's 4732 and 4733 where the local group is "administrators" </p>
<img width="1434" alt="Screenshot 2024-06-26 at 4 21 55 PM" src="https://github.com/bpark1223/SIEM-Visualization-Users-Added-Or-Removed-From-A-Local-Group-Within-A-Specific-Timeframe-/assets/77799235/207ef56a-b963-4e71-be01-4316d9c448c8">
</p> 5. I specify the type of visualization I want to create, which is "table". I then proceed to click "rows" to choose the specific elements that I want to include in the table. </p>
 <img width="982" alt="343289927-b9e4eeb3-78d1-414f-99c5-ff3eda8f41c9" src="https://github.com/bpark1223/SIEM-Visualization-Users-Added-Or-Removed-From-A-Local-Group-Within-A-Specific-Timeframe-/assets/77799235/a2621f67-6c58-4ed2-9085-7446582b82be"></p> 6. I configure the rows settings as follows: </p>
 <img width="339" alt="Screenshot 2024-06-26 at 2 33 06 PM" src="https://github.com/bpark1223/SIEM-Visualization-Successful-RDP-Logon-Related-To-Service-Accounts/assets/77799235/13e5db2b-0392-439b-9a64-bb08e728bf00">
</p>7. In the "metrics" window, I select "count"</p>
<img width="360" alt="Screenshot 2024-06-26 at 4 35 29 PM" src="https://github.com/bpark1223/SIEM-Visualization-Users-Added-Or-Removed-From-A-Local-Group-Within-A-Specific-Timeframe-/assets/77799235/d3147eb8-f292-4ed1-bdd7-997d22371ff0"> </p>
</p> 8. Include some more "Rows" settings to enhance understanding. </p>

</p> - Which user was added to or removed from the group? (winlog.event_data.MemberSid.keyword field)</p>

</p> -To which group was the addition or the removal performed? (double-checking that it is the "Administrators" one) (group.name.keyword field)</p>

</p> -Was the user added to or removed from the group? (event.action.keyword field)</p>

</p> -On which machine did the action occur? (host.name.keyword field)</p> 
<img width="1431" alt="Screenshot 2024-06-26 at 4 40 24 PM" src="https://github.com/bpark1223/SIEM-Visualization-Users-Added-Or-Removed-From-A-Local-Group-Within-A-Specific-Timeframe-/assets/77799235/44afcba8-96f6-4aef-911b-00dae6bd30a8">
</p> 9. We need to monitor user additions or removals from the local "Administrators" group within a specific timeframe (March 5th 2023 to date). Therefore, click on options, more, customize time frame and configure to March 5th, 2023 to now and add the filter to the panel. 
<img width="1420" alt="Screenshot 2024-06-26 at 4 42 31 PM" src="https://github.com/bpark1223/SIEM-Visualization-Users-Added-Or-Removed-From-A-Local-Group-Within-A-Specific-Timeframe-/assets/77799235/617d1b57-3095-4708-90f9-161837fa1922">
<img width="1429" alt="Screenshot 2024-06-26 at 4 44 17 PM" src="https://github.com/bpark1223/SIEM-Visualization-Users-Added-Or-Removed-From-A-Local-Group-Within-A-Specific-Timeframe-/assets/77799235/a2448227-7ced-4631-a9ff-e71bf15a0cdc">
</p> 10. 





