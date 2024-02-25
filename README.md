Configure Firewall Rules using Windows Defender Firewall with Advanced Security
We will look at Windows Defender Firewall with Advanced Security. This advanced view provides more in-depth options for configuration. All Windows Firewall rules, and their details, are stored here, allowing you to edit configurations for each rule or exception.

We want to use Windows Defender Firewall with Advanced Security to edit an existing firewall rule. We want to enforce the following rules:
Allow the connection for Key Management Service on the Domain and Private network.
Deny the connection for Key Management Service on the Public network.

1. Select Advanced settings on the Firewall & network protection screen.

![Alt text](https://github.com/Bryan-Mahadeea/Win-Firead/blob/main/1.png)

2. Here you will see an Overview in the center panel. Make special note of the two rule types listed on the left panel:
**Inbound rules**: Inbound rules determine what traffic is allowed to the computer.
**Outbound rules**: Outbound rules determine what traffic is allowed to leave the computer.
**Connection security rules**:
Monitoring:

![Alt text](https://github.com/Bryan-Mahadeea/Win-Firead/blob/main/2.png)

Each of these rules can be configured to filter traffic based on computers, users, applications, ports, protocols, and so on.
Click Inbound rules.
3. Here you will see a long list of inbound rules. Note that some of the rules have a green checkmark next to them. This indicates that the rule is enabled to allow inbound communication. The rules without a checkmark are available for use but are not enabled.

![Alt text](https://github.com/Bryan-Mahadeea/Win-Firead/blob/main/3.png)

4. Scroll to the Key Management Service inbound rule in the Overview panel of Windows Defender Firewall with Advanced Security. Note the following:
The policy is currently not enabled (the Enabled column says No.)
If enabled, the rule would allow communication (the Action column says Allow.)
Double-click this rule.

![Alt text](https://github.com/Bryan-Mahadeea/Win-Firead/blob/main/4.png)

5. Here you will see the details of this rule. You will note that the General tab includes the name of the rule, a description of the rule, and whether the rule has been allowed or blocked. In this case, the connection is allowed. Click the Advanced tab.

![Alt text](https://github.com/Bryan-Mahadeea/Win-Firead/blob/main/5.png)

6. Here you will see which profiles the rule applies to. In this case, Domain, Private and Public are all selected.

![Alt text](https://github.com/Bryan-Mahadeea/Win-Firead/blob/main/6.png)

7. Because we want to allow communication only with the domain and private networks, For Public this box should not have a checkmark. Next, click Apply, then click Ok.

![Alt text](https://github.com/Bryan-Mahadeea/Win-Firead/blob/main/7.png)

8. Now we will create an inbound rule that blocks communication with the public network. Since the new rule will be similar to the last, we will copy the existing rule. Right-click the Key Management Service (TCP-In) inbound rule and click Copy. Press Ctrl+V to paste.

![Alt text](https://github.com/Bryan-Mahadeea/Win-Firead/blob/main/8.png)

9. You will now see a second Key Management Service (TCP-In) inbound rule. Double-click the second rule to open the **Key Management Service *TCP-IN) Properties.

![Alt text](https://github.com/Bryan-Mahadeea/Win-Firead/blob/main/9.png)

10. Since we want to block connection with the public network, select Block the connection on the General tab. Click Apply.

![Alt text](https://github.com/Bryan-Mahadeea/Win-Firead/blob/main/10.png)

11. Click the Advanced tab.

![Alt text](https://github.com/Bryan-Mahadeea/Win-Firead/blob/main/11.png)

12. Click the Domain and Private boxes to remove the checkmarks. Click the Public to add the checkmark. Click Ok.

![Alt text](https://github.com/Bryan-Mahadeea/Win-Firead/blob/main/12.png)

13. The Overview panel will show your changes. Right-click each Key Management Service (TCP-In) rule and click Enable rule.

![Alt text](https://github.com/Bryan-Mahadeea/Win-Firead/blob/main/13.png)

14. Now you will see that a green checkmark appears next to the first rule indicating that the rule allowing communication is enabled. A circle with a line through it appears next to the second rule indicating that the rule blocking communication is enabled.



