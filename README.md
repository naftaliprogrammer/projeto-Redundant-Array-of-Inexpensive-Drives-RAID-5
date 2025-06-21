# projeto-Redundant-Array-of-Inexpensive-Drives-RAID-5
Tutorial prático de configuração de RAID 5 no Windows Server utilizando DiskPart! 🚀 Aprenda a criar um array com 3 discos. Assista ao vídeo completo e aprende como formatar, converter discos em dinâmicos,e atruibuir uma letra ao volume usando o diskpart pelo powershell.
---

### **Configuração do RAID 5 com DiskPart no Windows Server**

**Quantidade de Discos Necessários:**

* O RAID 5 requer, no mínimo, **3 discos**. É fundamental que os discos utilizados sejam **dinâmicos** e não **básicos**, pois apenas discos dinâmicos podem ser configurados para um array RAID no Windows Server. Discos básicos não oferecem suporte à criação de volumes RAID.

**Cálculo do Armazenamento Total:**

* **Capacidade Total do RAID 5**: No RAID 5, a capacidade total de armazenamento é calculada pela **soma do tamanho de todos os discos** menos o tamanho do maior disco, que será utilizado para paridade.

  * **Fórmula**: Capacidade Total = $(N - 1) \times$ Tamanho do Disco, onde **N** é o número total de discos e **Tamanho do Disco** é o tamanho de cada disco.
  * Exemplo: Se você utilizar 3 discos de 60 GB, o cálculo seria $(3 - 1) \times 60 GB$ = 120 GB de capacidade utilizável no array RAID 5.

**Dicas Importantes:**

* **Discos Dinâmicos**: Certifique-se de que os discos sejam configurados como **dinâmicos**. Discos básicos não suportam a criação de arrays RAID no Windows Server.
* **Sistema de Arquivos NTFS**: Ao formatar o volume do RAID 5, sempre opte pelo **NTFS**. O NTFS é o sistema de arquivos mais adequado para servidores, pois oferece suporte a recursos como segurança avançada, compressão de arquivos, auditoria e recuperação em caso de falhas. Além disso, o NTFS é mais eficiente no gerenciamento de grandes volumes de dados, como os encontrados em configurações RAID 5.

**Menções Finais:**

* O RAID 5 oferece **alta disponibilidade** e **tolerância a falhas**, pois distribui a paridade entre os discos, permitindo a reconstrução do array caso um disco falhe.
* Lembre-se de que, apesar de o RAID 5 proteger contra falhas de um disco, o desempenho de gravação pode ser ligeiramente inferior ao RAID 0, devido ao cálculo e gravação da paridade.

---





