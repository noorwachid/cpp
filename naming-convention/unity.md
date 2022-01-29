# C++ / Naming Convention / Unity

### Preview
``` cpp
namespace Network 
{
    enum struct State 
    {
        Pending,
        OnProgress,
        Done,
    };

    struct Packet 
    {
        uint8_t* data;
        uint32_t size;
    };
    
    class Socket 
    {
    public:
        void Bind(const Address& address);
      
        void Listen();
        
        Socket Accept(Address& address);
      
        int GetFD()
        {
            return _fd;
        }
        
    private:
        int _fd;
    };
}

int main() {
   const int port = 8000;
  
  Network::Socket socket;
  socket.Bind(Address("::", port));
  socket.Listen();
  
  return 0;
}
```
