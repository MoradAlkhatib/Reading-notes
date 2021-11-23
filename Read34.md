# Django Settings Best Practices
## Managing Django Settings: Issues
Different environments. Usually, you have several environments: local, dev, ci, qa, staging, production, etc. Each environment can have its own specific settings (for example: DEBUG = True, more verbose logging, additional apps, some mocked data, etc). You need an approach that allows you to keep all these Django setting configurations.
### Sensitive data.
You have SECRET_KEY in each Django project. On top of this there can be DB passwords and tokens for third-party APIs like Amazon or Twitter. This data cannot be stored in VCS.
### Sharing settings between team members.
You need a general approach to eliminate human error when working with the settings. For example, a developer may add a third-party app or some API integration and fail to add specific settings. On large (or even mid-size) projects, this can cause real issues.
### Django settings are a Python code.
This is a curse and a blessing at the same time. It gives you a lot of flexibility, but can also be a problem – instead of key-value pairs, settings.py can have a very tricky logic.


## Setting Configuration: Different Approaches
There is no built-in universal way to configure Django settings without hardcoding them. But books, open-source and work projects provide a lot of recommendations and approaches on how to do it best.
Let’s take a brief look at the most popular ones to examine their weaknesses and strengths.


## django-environ
Based on the above, we see that environment variables are the perfect place to store settings.
Now it’s time to talk about the toolkit.
Writing code using os.environ could be tricky sometimes and require additional effort to handle errors. It’s better to use django-environ instead.



# SSH
### What is SSH
SSH, or Secure Shell, is a remote administration protocol that allows users to control and modify their remote servers over the Internet.
The service was created as a secure replacement for the unencrypted Telnet and uses cryptographic techniques to ensure that all communication to and from the remote server happens in an encrypted manner. It provides a mechanism for authenticating a remote user, transferring inputs from the client to the host, and relaying the output back to the client.
The Figure Below shows a typical SSH Window. Any Linux or macOS user can SSH into their remote server directly from the terminal window. Windows users can take advantage of SSH clients like Putty.  You can execute shell commands in the same manner as you would if you were physically operating the remote computer.

### How Does SSH Work
If you’re using Linux or Mac, then using SSH is very simple. If you use Windows, you will need to utilize an SSH client to open SSH connections. The most popular SSH client is PuTTY, which you can learn more about here.
For Mac and Linux users, head over to your terminal program and then follow the procedure below:

The SSH command consists of 3 distinct parts:

```ssh {user}@{host}
```
The SSH key command instructs your system that you want to open an encrypted Secure Shell Connection. {user} represents the account you want to access.
For example, you may want to access the root user, which is basically synonymous for system administrator with complete rights to modify anything on the system.
{host} refers to the computer you want to access. This can be an IP Address (e.g. 244.235.23.19) or a domain name (e.g. www.xyzdomain.com).

When you hit enter, you will be prompted to enter the password for the requested account. When you type it in,
nothing will appear on the screen, but your password is, in fact being transmitted. Once you’re done typing, hit enter once again.
If your password is correct, you will be greeted with a remote terminal window.

### Understanding Different Encryption Techniques
The significant advantage offered by SSH over its predecessors is the use of encryption to ensure secure transfer of information between the host and the client.
Host refers to the remote server you are trying to access, while the client is the computer you are using to access the host.
There are three different encryption technologies used by SSH:

1. Symmetrical encryption.
2. Asymmetrical encryption.
3. Hashing.

### Symmetric Encryption
Symmetric encryption is a form of encryption where a secret key is used for both encryption and decryption of a message by both the client and the host.
Effectively, any one possessing the key can decrypt the message being transferred.

#### Asymmetric Encryption
Unlike symmetrical encryption, asymmetrical encryption uses two separate keys for encryption and decryption.
These two keys are known as the public key and the private key. Together, both these keys form a public-private key pair.

#### Hashing
One-way hashing is another form of cryptography used in Secure Shell Connections.
One-way-hash functions differ from the above two forms of encryption in the sense that they are never meant to be decrypted.

#### How Does SSH Work with These Encryption Techniques
The way SSH works is by making use of a client-server model to allow for authentication of two remote systems and encryption of the data that passes between them.
SSH operates on TCP port 22 by default (though this can be changed if needed). The host (server) listens on port 22 (or any other SSH assigned port) for incoming connections.
It organizes the secure connection by authenticating the client and opening the correct shell environment if the verification is successful.
They generate a unique value of a fixed length for each input that shows no clear trend which can exploited. This makes them practically impossible to reverse.

#### Session Encryption Negotiation
When a client tries to connect to the server via TCP, the server presents the encryption protocols and respective versions that it supports.
If the client has a similar matching pair of protocol and version, an agreement is reached and the connection is started with the accepted protocol. 
The server also uses an asymmetric public key which the client can use to verify the authenticity of the host.
Once this is established, the two parties use what is known as a Diffie-Hellman Key Exchange Algorithm to create a symmetrical key. This algorithm allows both the client and the server to arrive at a shared encryption key which will be used henceforth to encrypt the entire communication session.

#### Authenticating the User
The final stage before the user is granted access to the server is authenticating his/her credentials.
For this, most SSH users use a password. The user is asked to enter the username, followed by the password.
These credentials securely pass through the symmetrically encrypted tunnel, so there is no chance of them being captured by a third party.

#### Conclusion
Gaining an in-depth understanding of the underlying how SSH works can help users understand the security aspects of this technology.
Most people consider this process to be extremely complex and un-understandable, but it is much simpler than most people think. If you’re wondering how long it takes for a computer to calculate a hash and authenticate a user, well, it happens in less than a second. In fact, 
the maximum amount of time is spent in transferring data across the Internet.


