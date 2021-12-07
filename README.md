# Comando xfs_growfs para aumentar o tamanho de um sistema de arquivos XFS + Proxmox


No exemplo abaixo mostrarei como expandir, fazer um resize em uma partiçao linux do tipo XFS, para este exemplo usarei um sistema virtualizado Proxmox, na versão PVE 7.0.1

Primeiro vá ate a página web do Proxmox, escolha a VM que deseja alterar,depois em Hardware > Hard Disk >Resize Disk, coloque o valor em GB que deseja expandir, no exemplo 5GB:
![image](https://user-images.githubusercontent.com/79642492/145046544-d9cd555d-3b78-4119-a477-4bb0518fd9ed.png)


![image](https://user-images.githubusercontent.com/79642492/145047219-4b13eb19-8191-4e5c-956e-38ea00a69b0b.png)

Apos a alteração, sera necessário expandir o disco da VM em questão, para isso usaremos o utilitário cfdisk para alterar a unidade Sda1.

![image](https://user-images.githubusercontent.com/79642492/145049093-1486d282-4666-4133-9bb4-59c6a9729582.png)

```bash
# cfdisk /dev/sda 
```

Note que exite um espaço livre de 5G, então iremos alocar este espaço ao diretório sda1

![image](https://user-images.githubusercontent.com/79642492/145049584-462df95f-c0e7-4803-bb7a-eb2a1f55215c.png)

Apos alterar o tamanho do disco alocando-o o espaço livre para a partição sda1, você pode notar que o diretório  /  ainda esta com espaço anterior, por isso sera necessário alterá-lo também.

![image](https://user-images.githubusercontent.com/79642492/145098639-e316ecc4-c095-4356-9966-333e0011ef5a.png)


Para expandir o diretório  /  basta usar o comando xfs_growfs

```bash
# xfs_growfs /dev/sda1 

```
Agora podemos notar que a unidade está com o tamanho total.

![image](https://user-images.githubusercontent.com/79642492/145098984-bb411112-fedf-47f8-a3ce-2145230c947e.png)








