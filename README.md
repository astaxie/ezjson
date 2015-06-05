# ezjson
access the json elements easily

```
{
  "ID": "2",
  "IP": "12.12.12.12",
  "Port": "3000",
  "Sensor_Count": "1",
  "Control_Count": "1",
  "Sensors": {
    "Sensor_Name": "tem",
    "Type_Count": "1",
    "Types": {
      "types": [
        "temp",
        "C"
      ],
      "types": [
        "hum",
        "N"
      ]
    }
  },
  "Controls": [
    "LCD",
    "Relay"
  ],
  "Processes":[
     {
        "Name": "A",
        "Description": "A is a"
     },
     {
        "Name": "B",
        "Description": "B is b"     
     }
  ]
}
```

```
ej:=ezjson.NewJsonFile("a.json")
fmt.Println(ej.Int("ID"))  // 2
fmt.Println(ej.String("IP"))  // 12.12.12.12
fmt.Println(ej.Slice("Sensors::Types::types")) // ["temp","C"]
fmt.Println(sj.Slice("Controls"))  // ["LCD","Relay"]
fmt.Println(sj.String("Processes[0].Name"))  // A
```
