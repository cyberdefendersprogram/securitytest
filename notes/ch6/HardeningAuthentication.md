**_Wednesday, February 3rd, 2021_ | _Chapter 6: Hardening Authentication_ | _Nick Handy_**

# 6.6 Hardening Authentication

## Section Focus

User account and password security policies.

## Key Terms

| Terms                                         | Definition                                                   |
| --------------------------------------------- | ------------------------------------------------------------ |
| Multifactor authentication                    | Using more than one method to authenticate users.            |
| Smart cards                                   | Similar in appearance to credit cards, smart cards have an embedded memory chip that contains encrypted authentication information. These cards are used for authentication. |
| Microprobing                                  | The process of accessing a smart cards chip surface directly to observe, manipulate, and interfere with the circuit. |
| Radio frequency identification         (RFID) | The wireless, non-contact use of radio frequency waves to transfer data. |

#### User Education

User education is a large part of hardening authentication

- Don't share access
- Don't write passwords down
- Create memorable passwords
- Understand Social Engineering

#### Stronger Passwords

- Password Aging
- Password History
- Password Complexity
- Password Management

##### Password Policies

Account policies help you control the composition and use of passwords. Password policies include:        

- Enforce password history
  - Disables users from using a specified number of previous passwords when creating a new one
- Maximum password age
  - Requires user to change password when maximum age is reached
- Minimum password age
  - Stops user from changing password until the minimum password age is reached
- Minimum password length
- Password must meet complexity requirements
  - Prevent easy to guess passwords
  - Complexity Requirements:
    - Cannot contain the user's account name or parts of the user's full name that exceed two consecutive characters
    - Must be at least six characters in length
    - Must contain characters from three of the following four categories:            
      - English uppercase characters (A through Z)
      - English lowercase characters (a through z)
      - Base-10 digits (0 through 9)
      - Non-alphabetic characters (for example, !, $, #, or %)
  - Complexity requirements are enforced when passwords are changed or created.

#### Multifactor Authentication

Using more than one method to authenticate users. End users can be authenticated using four types of factors:        

- Something you know
- Something you have
- Something you are
- Something you do

When possible multifactor authentication should be used 

#### Account Restrictions

Places restrictions on user logins. For example, you can:

- Prohibit multiple concurrent logins
- Restrict logins to specific day/time
- Allow logins only from specific computers
- Create expiration dates for user accounts

#### Account Monitoring

Account monitoring can help you detect unusual or risky behavior. You should monitor for the following:        

- Login activity.
- Suspicious logins for the user (spikes, logins at unusual time of day, and/or frequent or failed logins).
- Remote-access traffic.

#### Account Maintenance

The following list provides best practices for account maintenance:        

- Delete an employee's account when the employee leaves the organization.
- Disable inactive accounts.
- Use automatic account expiration when applicable.
- Restrict remote access only to authorized clients (filtering by IP address).

#### Limit Remote Access

- Limited remote access
- Connected through dmz
- Restrict IP addresses
- Limit concurrent logins
- Audit remote logins

The following precautions should be taken when administering remote access:        

- Allow remote access to the network only for those users who need it to perform their duties (not standard for all users).
- Do not allow remote access clients to connect directly to  the internal network. Allow remote access clients to connect to a DMZ  and then monitor the traffic.
- Restrict remote access only to authorized clients. You can filter by IP address.

#### Account Policies Lockout

Account lockout disables a user account after a specified number of incorrect login attempts. Account lockout policies include:        

- Account lockout duration
  - Specifies the number of minutes a locked-out account remains locked out before automatically becoming unlocked. When set to 0, an administrator must unlock the account.
- Account lockout threshold
  - Specifies the number of failed logon attempts that causes a user account to be locked out.
- Reset account lockout counter after
  - Specifies the number of minutes that must elapse after a failed logon attempt before the failed logon attempt counter is reset to 0 bad logon attempts. For example, if this value is set to 60 minutes and the account lockout threshold is set to 5, the  user can enter up to four incorrect passwords within one hour without the account being locked.

Account lockout can be used to prevent attackers from guessing passwords, but it can also be used maliciously to lock an account and prevent a valid user from logging in

#### Hardening Best Practices

Hardening Authentication Best Practices

When controlling user account and password security, be aware of the following:

- For large environments, implement a password management system with a self-service password reset management system.

- Implement account auditing to track incorrect login attempts.

- Scan systems to identify unused user accounts or accounts with blank passwords.

- Disable and/or remove default accounts.

- Prohibit the use of generic user accounts.

- Prohibit the use of shared user accounts.      

  Shared accounts:      

  - Increase attack vectors.
  - Make password management more difficult.
  - Reduce responsibility for the account.
  - Destroy audit trails for the account.
  - Make it difficult to monitor the account for unusual  activity.

#### Smart Cards

Smart cards are plastic cards similar to credit cards that have an embedded memory chip that contains encrypted    authentication information. 

- Can be divided into two categories:      
  - Contact smart cards (Gold Plated Contact)
  - Contactless smart cards (RFID)

#### Smart Card Benefits and Weaknesses

Key benefits of smart cards include the following:

- They provide tamper-resistant storage for a user's private key and other personally identifying information (PII).
- They isolate security-related operations from the rest of the system.
- They allow security credentials to be portable.

Smart cards are subject to the following weaknesses:

- Microprobing  
  - This is the process of accessing the chip surface directly to observe, manipulate, and interfere with the circuit.
- Software attacks
  - These exploit vulnerabilities in the card's protocols or encryption methods.
- Eavesdropping 
  - This captures transmission data produced by the card as it is used.
- Fault generation 
  - This deliberately induces malfunctions in the card.