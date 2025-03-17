# Starten 
mit ```podman compose up```
# Quellen
https://vector.dev/docs/setup/deployment/

# Influx Export Query
```
from(bucket:"mybucket") 
  |> range(start: -1h) 
  |> pivot(rowKey:["_time"], columnKey: ["_field"], valueColumn: "_value")
```

# Test with codespaces
use ngrok for tunneling aggreagtor
```ngrok tcp 9000```