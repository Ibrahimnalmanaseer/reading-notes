What is OAuth?
open-standard authorization which allows connecting of unrelated servers in a safe way


Give an example of using OAuth would look like.
when a user tries to log in to the website, the website gives the user the ability to logged using the account he has on other websites such as linked-in or Gmail.


How does OAuth work? What are the steps that it takes to authenticate the user?

The first website connects to the second website on behalf of the user, using OAuth, providing the user’s verified identity.
The second site generates a one-time token and a one-time secret unique to the transaction and parties involved.
The first site gives this token and secret to the initiating user’s client software.
The client’s software presents the request token and secret to their authorization provider (which may or may not be the second site).
If not already authenticated to the authorization provider, the client may be asked to authenticate. After authentication, the client is asked to approve the authorization transaction to the second website.
The user approves (or their software silently approves) a particular transaction type at the first website.
The user is given an approved access token (notice it’s no longer a request token).
The user gives the approved access token to the first website.
The first website gives the access token to the second website as proof of authentication on behalf of the user.
The second website lets the first website access its site on behalf of the user.
The user sees a successfully completed transaction occurring.
OAuth is not the first authentication/authorization system to work this way on behalf of the end-user. In fact, many authentication systems, notably Kerberos, work similarly. What is special about OAuth is its ability to work across the web and its wide adoption. It succeeded with adoption rates where previous attempts failed (for various reasons).



                  4.  What is OpenID?

                                  authorizing mechanism, to identify the user, which makes the user's login experience easier. 




-----------------------------------------------------------------------------------------------------------------

What is the difference between authorization and authentication?
authentication is the process of verifying who a user is, while authorization is the process of verifying what they have access to. 


What is Authorization Code Flow?
exchanges an Authorization Code for a token.


What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?

OpenId Connect flow is specifically designed to authenticate native or mobile application users.


What is Implicit Flow with Form Post?
securely app stores public Client Secrets. 


What is Client Credentials Flow?
authenticate machine-to-machine 


What is Device Authorization Flow?
input-constrained devices that connect to the internet, rather than authenticate the user directly, the device asks the user to go to a link on their computer or smartphone and authorize the device. 


What is Resource Owner Password Flow?

which requests that users provide credentials (username and password), typically using an interactive form 




