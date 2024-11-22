
# **Exercício de Configuração e Gerenciamento de Instância EC2 - Curso Arquitetos da Nuvem (PROZ e AWS)**

Este repositório contém a documentação e evidências do exercício realizado para configurar uma instância EC2, gerenciar armazenamento, criar um volume EBS e explorar os recursos da instância utilizando comandos no terminal.

---

## **Etapas Realizadas**

### **1. Configuração da Instância EC2**
- Acesse o **Console da AWS** e navegue até o serviço EC2.
- Crie uma nova instância com as configurações abaixo:
  - **Imagem:** Amazon Linux 2.
  - **Tipo de instância:** t2.micro (ou outro tipo de acordo com os recursos necessários).
- Certifique-se de usar ou criar uma chave de par para acesso via SSH.

---

### **2. Conexão via SSH**
- Após a instância ser iniciada, utilize o arquivo de chave privada para conectar-se via SSH:
  ```bash
  ssh -i <caminho-da-chave-privada.pem> ec2-user@<IP-público-da-instância>
  ```
- Verifique o acesso ao terminal.

---

### **3. Gerenciando o Armazenamento**
- No Console da AWS:
  - Crie um volume EBS com o tamanho desejado (e.g., 10 GiB).
  - Anexe o volume à instância EC2 criada.

---

### **4. Formatando e Montando o Volume**
- Na instância EC2, liste os dispositivos disponíveis:
  ```bash
  lsblk
  ```
- Formate o volume com um sistema de arquivos (e.g., ext4):
  ```bash
  sudo mkfs.ext4 /dev/xvdf
  ```
- Crie um diretório para montar o volume:
  ```bash
  sudo mkdir /mnt/volume
  ```
- Monte o volume:
  ```bash
  sudo mount /dev/xvdf /mnt/volume
  ```
- Verifique se o volume foi montado corretamente:
  ```bash
  df -h
  ```

---

### **5. Criação de Arquivos**
- Crie um arquivo de texto simples no volume montado:
  ```bash
  echo "Exercício de EC2 e EBS - Curso PROZ e AWS" | sudo tee /mnt/volume/exercicio.txt
  ```
- Verifique o conteúdo do arquivo:
  ```bash
  cat /mnt/volume/exercicio.txt
  ```

---

### **6. Explorando Recursos**
- Execute os comandos para verificar o status do volume e conteúdo:
  - Listar diretórios: `ls /mnt/volume`
  - Verificar espaço em disco: `df -h`
  - Verificar volumes montados: `mount`
  - Exibir conteúdo do arquivo: `cat /mnt/volume/exercicio.txt`

- **Print do último passo:** Inclua uma captura de tela dos comandos acima executados.

---

### **7. Encerramento da Instância**
- Após concluir o exercício, encerre ou interrompa a instância EC2 no Console da AWS para evitar custos adicionais.

---

## **Arquivos Disponíveis**
- **`screenshots/`**: Contém prints das etapas realizadas no exercício.
- **`README.md`**: Este documento explicando as etapas realizadas.

---

## **Como Reproduzir**
1. Siga os passos descritos no README.
2. Certifique-se de ter uma conta AWS configurada e acesso ao console.

---

## **Contribuição**
Este projeto foi desenvolvido por **Victor Ramos Andrade Callegari** como parte do curso **Arquitetos da Nuvem** oferecido pela **PROZ e AWS**.

