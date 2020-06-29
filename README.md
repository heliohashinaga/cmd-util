# Util
Lista de comandos úteis.

# Criar Service Reference com svcutil
1. Abrir Developer Command Prompt for VS 20xx (versão do visual studio)
2. Executar o comando
```
svcutil http://locahost/service.svc /Language=c# /t:Code /ct:System.Collections.Generic.List`1 /out:ServiceName.cs /config:ServiceName.config 
```
