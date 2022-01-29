# C++ / Naming Convention / Java

### Preview
``` cpp
namespace network {
    enum struct State {
        PENDING,
        ON_PROGRESS,
        DONE,
    };

    struct Packet {
        uint8_t* data;
        uint32_t size;
    };
    
    class Socket {
    public:
        void bind(const Address& address);
      
        void listen();
        
        Socket accept(Address& address);
      
        int getFd()
        {
            return fd;
        }
        
    private:
        int fd;
    };
}

int main() {
   const int PORT = 8000;
  
  network::Socket socket;
  socket.bind(Address("::", PORT));
  socket.listen();
  
  return 0;
}
```
