NAMESERVER = server
NAMECLIENT = client
NAME = putstr.c
SRCSERVER = server.c
SRCCLIENT = client.c
FLAGS = -Wall -Wextra -Werror
CC = gcc
OBJSERVER = $(SRCSERVER:.c=.o)
OBJCLIENT = $(SRCCLIENT:.c=.o)
OBJNAME = $(NAME:.c=.o)

all:  $(NAMESERVER) $(NAMECLIENT)

$(NAME) : all

$(NAMESERVER) : $(OBJSERVER)
	$(CC) $(OBJSERVER) -o $(NAMESERVER) $(NAME)

$(NAMECLIENT) : $(OBJCLIENT)
	$(CC) $(OBJCLIENT) -o $(NAMECLIENT) $(NAME)

clean:
	rm -rf $(OBJSERVER) $(OBJCLIENT) 
	
fclean: clean
	rm -rf $(NAMESERVER) $(NAMECLIENT) 

norm:
	norminette *.[ch]

re:fclean all

.PHONY : re fclean clean all  norm