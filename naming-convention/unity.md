# C++ / Naming Convention / Unity

### Preview
```
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
        
        Socket Accept(Address& address);
        
    private:
        int _fd;
        Address _address;
    };
}
```
