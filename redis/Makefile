CXXFLAGS := -Wall -Wextra -g
CXXFLAGS += -Wpedantic -Warray-bounds -Weffc++
CXXFLAGS += -Werror

COMMON_SRCS := helper.c
SERVER_SRCS := server.c
CLIENT_SRCS := client.c

all: server client

server: $(SERVER_SRCS) $(COMMON_SRCS)
	g++ $(CXXFLAGS) $(SERVER_SRCS) $(COMMON_SRCS) -I. -o server

client: $(CLIENT_SRCS)
	g++ $(CXXFLAGS) $(CLIENT_SRCS) $(COMMON_SRCS) -I. -o client

.PHONY: clean
clean:
	rm -f server client
