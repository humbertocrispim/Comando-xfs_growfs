# Comando xfs_growfs para aumentar o tamanho de um sistema de arquivos XFS + Proxmox
No exemplo abaixo mostrarei como expamdir (resize),um sitema de arquivo tipo XFS, para este exemplo usarei um sistema virtualizado Promox, na versao PVE 5.11.22-8

Primeiro va ate a pagina web do Promox, escolha a VM que deseja alterar,va em Hardware > Hard Disk >Resize Disk
![image](https://user-images.githubusercontent.com/79642492/145046544-d9cd555d-3b78-4119-a477-4bb0518fd9ed.png)

Apos coloque o valor em GB que deseja expandir, no exemplo 5GBi:


![image](https://user-images.githubusercontent.com/79642492/145047219-4b13eb19-8191-4e5c-956e-38ea00a69b0b.png)

Apos a auteraçao, sera nescessario expamdir o disco da VM em questao:


