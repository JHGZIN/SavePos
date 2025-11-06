# 🧩 SavePos

Inclui um sistema simples e eficiente para salvar posições de jogadores e veículos no **SA:MP**, gerando automaticamente linhas prontas para uso em *AddPlayerClass* ou *AddStaticVehicle*.  
Ideal para quem faz mapeamentos, testes de spawns ou desenvolvimento de gamemodes.

---

## 📝 Descrição

O **SavePos** é um filterscript leve que permite salvar coordenadas diretamente em um arquivo `Positions.txt`.  
Com o comando `/SavePos`, você pode capturar a posição do jogador ou do veículo atual, além de adicionar uma descrição personalizada.

---

## ⚙️ Instalação

1. Baixe ou compile o arquivo `SavePos.pwn`.  
2. Coloque o `SavePos.amx` na pasta **`filterscripts`** do seu servidor.  
3. No arquivo `server.cfg`, adicione:
   ```bash
   filterscripts SavePosPro

4. Inicie o servidor normalmente.

---

## 💬 Comandos

```pawn
/SavePos
/SavePos [descrição]
```

* **Sem descrição:** salva a posição e o ângulo do jogador ou veículo.
* **Com descrição:** adiciona um comentário no final da linha, facilitando a organização das posições.

---

## 💾 Saída gerada

Ao usar o comando, as posições são salvas automaticamente no arquivo:

```
Positions.txt
```

### Exemplos:

```pawn
AddPlayerClass(280, 1532.1, -1678.4, 13.5, 90.0, 0, 0, 0, 0, 0, 0); //SpawnInicial
AddStaticVehicle(411, 1535.0, -1670.5, 13.5, 180.0, 0, 0); //Infernus
```

---

## 🧠 Funções internas

```pawn
savedposition(const string[])
strtok(const string[], &index)
GetVehicleColor(vehicleid, &color1, &color2)
```

Essas funções são utilizadas internamente para formatação e gravação no arquivo `Positions.txt`.

---

## 📂 Estrutura de arquivos

```
📁 samp-server/
 ┣ 📁 filterscripts/
 ┃ ┗ 📄 SavePosPro.amx
 ┣ 📄 server.cfg
 ┗ 📄 Positions.txt
```
