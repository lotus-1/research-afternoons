# Streams And Buffers
## Team :


## what streams and buffers are in Node?
### **Buffer**:  
In computer science and electronics terminology, a Buffer refers to space in memory which is used to store data temporarily. A buffer has traditionally been used between devices with speed mis-match so that they can keep on operating at their respective speeds without loss of data. In Node.js Buffers are used when dealing with file streams or tcp streams which are mainly octets of binary data.  

Buffer is a global module, therefore we don't need to use require operator in order to use buffer functionality.

![]()

### **Stream**:  
Streams are channels on which data can be sent or from which data can be received. Technically it means that we can have readable streams, writeable streams or duplex streams which can be used for both reading and writing. In some cases we can pipe data of one stream to other. Here we'll look at simple examples of readable and writeable streams.  

Streams in Node.js emit different events at different intervals in their life cycle. In order to get value out of those events, we write event handler functions which get executed whenever the stream emits the corresponding event.   
**Common events for readable streams are:** close , data , end , error and readable .  
 **Similarly events for writeable streams are:** close , drain , error , finish , pipe , unpipe .


## how are they used in conjunction?

To answer this question please click [here](https://youtu.be/GlybFFMXXmQ) and whatch the vedio.
