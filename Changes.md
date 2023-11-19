# Ideas For Improvement

The current library is a direct literal transcription of iouring and liburing. 

## make some fields external
 fd file descriptor 

## make parameters more go friendly

### prepare.go changes

#### (*sqe)PrepFRead

internalise necessary parameter conversions:  
 (1) pass buf []byte instead of bufptr uintptr and numbytes  
 (2) pass os.File instead of fd  

#### (*sqe)PrepFWrite

same as read  
internalise necessary parameter conversions:  
 (1) pass buf []byte instead of bufptr uintptr and numbytes  
 (2) pass os.File instead of fd  

### setup.go

add OpList [50]string: name list of Ops
