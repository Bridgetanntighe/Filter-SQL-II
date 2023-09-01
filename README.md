<h1>Analyze a packet with Wireshark  </h1>


<h2>Description</h2>
Analyzing packets can help security teams interpret and understand network communications. Network protocol analyzers such as Wireshark, which has a graphical user interface or GUI, can help examine packet data during your investigations. Since network packet data is complex, network protocol analyzers (packet sniffers) like Wireshark are designed to help find patterns and filter the data in order to focus on the network traffic that is most relevant to your security investigations.


<h2>Task 1. Apply a basic Wireshark filter and inspect a packet</h2>
Below shows Port 80 is the TCP destination port for this packet. It contains the initial web request to an HTTP website that will typically be listening on TCP port 80. <br>
<img src="https://github.com/Bridgetanntighe/FilterSQLTheory/assets/134883216/553b5bf4-0fd7-4d74-82f0-c957d2a058aa" height="50%" width="50%" alt="Active Directory Lab"/>


<h2>Task 2. Use filters to select packets</h2>
TCP is the internal protocol contained in the first packet from MAC address 42:01:ac:15:e0:02.
<img src="https://github.com/Bridgetanntighe/FilterSQLTheory/assets/134883216/38a013dc-c2a9-4164-8081-395885ac97ba" height="50%" width="50%" alt="Active Directory Lab"/>


<h2>Task 3. Use filters to explore DNS packets:</h2>
The IP address 142.250.1.139 is displayed in the expanded Answers section for the DNS query for opensource.google.com.
<img src="https://github.com/Bridgetanntighe/FilterSQLTheory/assets/134883216/e240ad3a-0a09-4e60-9c7c-d67b512c4afe" height="80%" width="80%" alt="Active Directory Lab"/>

<h2>Task 5. Use filters to explore TCP packets:</h2>
This filters to packets containing web requests made with the <i>curl</i> command in this sample packet capture file.
<img src="https://github.com/Bridgetanntighe/FilterSQLTheory/assets/134883216/bfec4b33-2cb7-44f4-9885-78f89ff4d444 height="80%" width="80%" alt="Active Directory Lab"/>
