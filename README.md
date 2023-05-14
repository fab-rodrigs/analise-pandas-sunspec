# analise-pandas-sunspec
Este é um projeto de análise de dados lidos de inversores solares no padrão Sunspec.

> Status do Projeto: Em teste :stopwatch:
---
## Protocolo de Comunicação
A aquisição de dados dos inversores é feita com auxílio do Pymodbus, uma implementação do protocolo Modbus com um padrão Sunspec.

## Execução
Para realizar-se a conexão na porta RS485 do inversor, é necessário um adaptador ft232rl para RS485. A implementação `pymodbus_pandas.py` pode ser direcionada da seguinte forma, de acordo com a porta USB que está sendo conectada:
```
client = ModbusClient(method="rtu", port="/dev/ttyUSB1", timeout=1, baudrate=9600, dsrdtr=0)
```

