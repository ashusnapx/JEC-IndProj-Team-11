# JEC-IndProj-Team-11
ɪɴ ᴛʜɪꜱ ᴘʀᴏᴊᴇᴄᴛ ᴡᴇ'ʟʟ ᴍᴀᴋᴇ ᴀ ᴘᴇᴇʀ-ᴛᴏ-ᴘᴇᴇʀ ꜰɪʟᴇ ꜱʜᴀʀɪɴɢ ꜱʏꜱᴛᴇᴍ , ᴡʜɪᴄʜ ɪꜱ ꜱɪᴍɪʟᴀʀ ᴛᴏ ᴏʀ ʀᴇꜱᴇᴍʙʟᴇꜱ ʟɪᴋᴇ ʙɪᴛ-ᴛᴏʀʀᴇɴᴛ.
ᴀꜱꜱɪɢɴᴍᴇɴᴛ 1:- ᴛᴏ ʟᴇᴀʀɴ ʜᴏᴡ ᴛᴏ ᴄʀᴇᴀᴛᴇ ᴀ ꜱᴇʀᴠᴇʀ ᴀɴᴅ ᴄʟɪᴇɴᴛ ɪɴᴛᴇʀꜰᴀᴄᴇ ᴀᴋᴀ ꜱᴏᴄᴋᴇᴛ.
this is the server side made by team 11 which consists of Aditi Jain , Hritik Kumar and Ashutosh Kumar
there are various steps to create a server :



STEP 1(SERVER CREATION) :- in this step we have to create a socket. syntax for socket is 
int sockfd(domain,type,protocol) -->sockfd means socket descriptor

                                 -->domain are the communication domain(eg. AF_INET and AF_INET6)

                                 -->type are basically communication type
                                 (i)SOCK_STREAM --> TCP(reliable and connection oriented)
                                 (ii)SOCK_DGRAM --> UDP(unreliable and connectionless)

                                 -->protocol is basically the IP and this should be same on server and client side.


STEP 2(SETSOCKOPT) :- in this step we'll create a function called setsocktopt , basically this function sets the current value for a socket option associated with socket of any type and in any state or in short this also helps in controloing the options for the socket which were referred by file descriptor.Pros of it is that , it doesn't allows the error like address already in use to occur. So the syntax is :-
int setsocktopt
(
    socket     s;
    int        level;
    int        optname;
    const char *optval;
    int        optlen;
)
FOR MORE INFO I'M PUTTING THIS LINK :- https://docs.microsoft.com/en-us/windows/win32/api/winsock/nf-winsock-setsockopt


step 3(BIND) :- in this step we make a rishta between socket with address and port number, so the syntax is :-
int bind(int sockfd , const struct sockaddr *addr , socklen_t addrlen)


step 4(LISTEN) :- in this step the server goes in the waiting mode , waiting for whom ? , waiting for the client to come and make a connection.So the syntax is :-
int listen(int sockfd,int backlog);
the term backlog here means that the list of pending requests for connecting client with server and if the queue is full then the error comes that ECONNREFUSED.


step 5(ACCEPT) :- in this step a request from listen(step 4) is taken and extracted to fulfil the first request and our socket named sockfd creates a new socket and gives back a new file descriptor. 


🤩🥳 AND NOW YOUR SERVER IS READY TO GO.
*/
