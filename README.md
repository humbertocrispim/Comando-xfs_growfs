# Comando xfs_growfs para aumentar o tamanho de um sistema de arquivos XFS + Proxmox


No exemplo abaixo mostrarei como expamdir (resize),um sitema de arquivo tipo XFS, para este exemplo usarei um sistema virtualizado Promox, na versao PVE 7.0.1

Primeiro va ate a pagina web do Promox, escolha a VM que deseja alterar,va em Hardware > Hard Disk >Resize Disk, coloque o valor em GB que deseja expandir, no exemplo 5GBi:
![image](https://user-images.githubusercontent.com/79642492/145046544-d9cd555d-3b78-4119-a477-4bb0518fd9ed.png)


![image](https://user-images.githubusercontent.com/79642492/145047219-4b13eb19-8191-4e5c-956e-38ea00a69b0b.png)

Apos a auteraçao, sera nescessario expamdir o disco da VM em questao, para isso usaremos o utilitario cfdisk para alterar a unidade Sda1.

![image](https://user-images.githubusercontent.com/79642492/145049093-1486d282-4666-4133-9bb4-59c6a9729582.png)

```bash
# cfdisk /dev/sda 
```


Note que exitem um espaço livre de 5G, entao iremos alocar este espaço ao disco sda1

![image](https://user-images.githubusercontent.com/79642492/145049584-462df95f-c0e7-4803-bb7a-eb2a1f55215c.png)



Clique aqui para ver o exemplo: ![aqui](https://user-images.githubusercontent.com/79642492/145095399-e226d06a-78ad-4411-872e-feb29e863e15.gif)









