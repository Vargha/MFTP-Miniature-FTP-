Description: MFTP is a network communication program in C language,
             and it can be used to transfer different kinds of data
             and commands between a server and a client.
_____________________________________________________________________________
To Compile:  Open the terminal and type make, then press enter.

             It is totally possible to execute the code without using
             the Make file, but please Read the following notes before
             compiling the code:

             Program is sensitive about the name of the file, and
             it is necessary to name the executed file names as below:
             Executed file name for the Server: server
             Executed file name for the Client: client

_____________________________________________________________________________
How to Run:
    Server:  Run the server, before running the client, using the command:
             server

             To exit simply type the command:
             exit

             ________________________________________________________________
    Client:  Read the Server's Host Name from the server. Server displays
             it as soon as you run the server.

             Internal commands to use the client program:

             1. exit
                Terminate the client program

             2. cd <pathname>
                Changes the current directory of the client process to
                <pathname>.
                It is an error if <pathname> does not exist, or is not a
                readable directory.

              3. rcd <pathname>
                Change the current directory of the server to <pathname>.
                It is an error if <pathname> does not exist, or is not a
                readable directory.

              4. ls
                Executes the “ls –l” command locally and displays the output
                to standard output, 20 lines at a time.
                Waits for a carriage return (newline) or a space character on
                standard input before displaying the next 20 lines.

              5. rls
                Executes the “ls –l” command on the remote server and displays
                the output to the client’s standard output, 20 lines at a time
                in the same manner as “ls” above.

              6. get <pathname>
                Retrieves <pathname> from the server and store it locally in the
                client’s current working directory using the last component of
                the <pathname> as the file name.
                It is an error if <pathname> does not exist, or is anything other
                than a regular file, or is not readable.
                It is also an error if the file cannot be opened/created in the
                client’s current working directory.

              7. show <pathname>
                Retrieves the contents of the indicated remote <pathname> and
                write it to the client’s standard output, 20 lines at a time.
                Waits for the user to type a carriage return or a space character
                before typing out the next 20 lines.
                It is an error if <pathname> does not exist, or is anything except
                a regular file, or is not readable.

              8. put <pathname>
                Transmits the contents of the local file <pathname> to the server
                and store the contents in the server process’ current working
                directory using the last component of <pathname> as the file name.
                It is an error if <pathname> does not exist locally or is anything
                other than a regular file.
                It is also an error if the file cannot be opened/created in the
                server’s child process’ current working directory.
