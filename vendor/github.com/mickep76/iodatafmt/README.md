Please use https://github.com/mickep76/encoding instead.


# iodatafmt
    import "github.com/mickep76/iodatafmt"






## func Load
``` go
func Load(fn string, f DataFmt) (interface{}, error)
```
Load a file with serialized data.


## func LoadPtr
``` go
func LoadPtr(ptr interface{}, fn string, f DataFmt) error
```
LoadPtr a file with serialized data.


## func Marshal
``` go
func Marshal(d interface{}, f DataFmt) ([]byte, error)
```
Marshal YAML/JSON/TOML serialized data.


## func Print
``` go
func Print(d interface{}, f DataFmt) error
```
Print serialized data.


## func Sprint
``` go
func Sprint(d interface{}, f DataFmt) (string, error)
```
Sprint return serialized data.


## func Unmarshal
``` go
func Unmarshal(b []byte, f DataFmt) (interface{}, error)
```
Unmarshal YAML/JSON/TOML serialized data.


## func UnmarshalPtr
``` go
func UnmarshalPtr(ptr interface{}, b []byte, f DataFmt) error
```
UnmarshalPtr YAML/JSON/TOML serialized data.


## func Write
``` go
func Write(fn string, d map[string]interface{}, f DataFmt) error
```
Write a file with serialized data.



## type DataFmt
``` go
type DataFmt int
```
DataFmt represents which data serialization is used YAML, JSON or TOML.



``` go
const (
    YAML DataFmt = iota
    TOML
    JSON
    UNKNOWN
)
```
Constants for data format.







### func FileFormat
``` go
func FileFormat(fn string) (DataFmt, error)
```
FileFormat returns DataFmt constant based on file extension.


### func Format
``` go
func Format(s string) (DataFmt, error)
```
Format returns DataFmt constant based on a string.










- - -
Generated by [godoc2md](http://godoc.org/github.com/davecheney/godoc2md)