1. if [[ "${UID}" -ne 0 ]]   # check is root user . for root user UID will 0
2. read -p 'Enter the username to create: ' USER_NAME   # read variable USER_NAME
3. echo $? #This is the exit status of the last executed command.
4. passwd -e ${USER_NAME} # Force password change on first login.
5. echo "${HOSTNAME}"  # check host name
6. exit 0 # important to write end of shell script
7.  USER_NAME=$(id -un) # current user name 
8. NUMBER_OF_PARAMETERS="${#}" # ${#} gives number of perameter passed in command prompt like .[test.sh a b c] nuber will 3
9. if [[ "${NUMBER_OF_PARAMETERS}" -lt 1 ]] # check NUMBER_OF_PARAMETERS should have 1
10. for USER_NAME in "${@}"  # "${@}" recieve all perameter which we are passing in cmd like . [test.sh a b c]
11. for USER_NAME in "${*}"  # "${*}" recieve all perameter which we are passing in cmd like . [test.sh a b c]
