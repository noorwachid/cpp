# C++ / Naming Convention / Unreal Engine

### Preview
``` cpp
namespace Network 
{
    enum struct EState 
    {
        Pending,
        OnProgress,
        Done,
    };

    struct TPacket {
        uint8_t* Data;
        uint32_t Size;
    };
    
    class TSocket {
    public:
        void Bind(const TAddress& address);
      
        void Listen();
        
        Socket Accept(TAddress& address);
      
        int GetFD()
        {
            return FD;
        }
        
    private:
        int FD;
    };
}

int main() 
{
   const int Port = 8000;
  
  Network::TSocket socket;
  socket.Bind(TAddress("::", PORT));
  socket.Listen();
  
  return 0;
}
```
