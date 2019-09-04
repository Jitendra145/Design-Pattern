# What are the basic idea of the Proxy pattern

1. Proxies are objects that stands in for other objects
2. Proxy objects control access or abstract functionality of  other object.


Example of the Proxy pattern is Remote Method Invokation(RMI)

1. RMI in java was a way to make method calls to code that resided on different machine.
2. "WAS" because RMI has been superseeded by more sophisticated ways of doing this - REST APIs for instance
3. RMI was an important step in the evolution of distributed computing.
4. When you make a RMI call, you would get a "proxy object" A Stand -In  for the actual object that resided in the different machine.
5. The Underlying principle of the proxy pattern is that one object controls the access to another.
6. The Controlling object is called the Proxy or the surrogate.
7. In RMI, A Proxy is needed to Abstract the programmer from the Nitty-Gritty of dealing with an object on another machine.
8. Such a Proxy is called REMOTE PROXY
9. Proxies might also be useful If expensive method calls can be cached.
10. For instance , The proxy for a command object could maintain a cache where the key set of parameters from each call to the command and value result of the command

E.g Memization technique
