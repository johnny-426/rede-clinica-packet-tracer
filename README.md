# Laboratório de redes IPv4 no Cisco Packet Tracer

Montei uma rede simulada para entender como um computador acessa um servidor em outra sub-rede. No cenário, dois PCs representam a recepção e a triagem de uma clínica fictícia. Eles estão na rede `192.168.10.0/24`. Um roteador liga essa rede à `192.168.20.0/24`, onde o mesmo servidor hospeda uma página de teste e o serviço DNS.

## Como testar

1. Abra [rede-clinica.pkt](./rede-clinica.pkt) no Cisco Packet Tracer.
2. No **PC0**, abra **Desktop > Command Prompt** e execute `ping 192.168.20.10` para testar o caminho até o servidor.
3. No **PC1**, abra **Desktop > Command Prompt** e execute `nslookup agenda.clinica.test`. O nome deve apontar para `192.168.20.10`.
4. Ainda no **PC1**, abra **Desktop > Web Browser** e acesse `http://agenda.clinica.test`.

Durante a montagem, a página abriu pelo endereço IP, mas o navegador não reconheceu o nome. Adicionei o registro que faltava no DNS e consegui abrir a mesma página pelos dois endereços.
