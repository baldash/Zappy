##
## Makefile for malloc in /home/sylvain/Documents/projets/tek2/PSU/PSU_2016_malloc/malloc
## 
## Made by Sylvain Chaugny
## Login   <sylvain.chaugny@epitech.eu>
## 
## Started on  Mon Jan 30 17:23:36 2017 Anthony Leclerc
## Last update Thu Jun 22 11:19:22 2017 Anthony LECLERC
##

CC		=	gcc

include		sources.mk

TARGET		=	../lib

NAME		=	$(TARGET)/libsocket.a

OBJ		=	$(SRC:.c=.o)
CFLAGS		=	-W -Wall -Wextra

INC		=	-I.. -L../lib

ifeq ($(DEBUG), 1)
CFLAGS		+=	-g -ggdb3
endif

all:			lib

lib:			$(NAME)

$(NAME):		$(OBJ)
			ar rc $(NAME) $(OBJ)
clean:
			rm -rf $(OBJ)

fclean:			clean
			rm -rf $(NAME)

re:			fclean all

.PHONY:			all clean fclean re

%.o :			%.c
			$(CC) -c $< -o $@ $(CFLAGS) $(INC)
