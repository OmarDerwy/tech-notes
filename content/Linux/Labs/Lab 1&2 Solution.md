# 1	Lab 1
## 1.1	)
## 1.2	)

| Cat                                                 | More                                                        |
| --------------------------------------------------- | ----------------------------------------------------------- |
| Displayes files as continues flow form start to end | Displays files as seperate pages that you can cycle between |
| better for small files                              | better for larger files for easier viewability              |
## 1.3	)

![[Pasted image 20241123140630.png|400]]
![[Pasted image 20241123140713.png|400]]

| rm                                                 | rmdir                          |
| -------------------------------------------------- | ------------------------------ |
| remove file and also directories if using the `-r` | only remvoes empty directories |
 

## 1.4	)
![[Pasted image 20241123141913.png|400]]
![[Pasted image 20241123142034.png|400]]
### 1.4.1	)
![[Pasted image 20241123142805.png|400]]
I noticed that I cannot remove directories without using the `-r` option with `tm`

### 1.4.2	)
![[Pasted image 20241123143426.png|400]]
Entire path has been removed. `dir12` and its parent directory `dir1`
### 1.4.3	)
absolute : /home/user/docs/mycv
relative: ~/docs/mycv

## 1.5	)
![[Pasted image 20241123144725.png|400]]
## 1.6	)
![[Pasted image 20241123144757.png|400]]
## 1.7	)
```bash
cd $HOME
```
```bash
cd ~
```
```bash
cd /home/derwy
```
```bash
cd ../../home/derwy
```
## 1.8	)
![[Pasted image 20241123145117.png|400]]
## 1.9	)
![[Pasted image 20241123145149.png|400]]
## 1.10	)
![[Pasted image 20241123145226.png|400]]
## 1.11	)
```bash
man -a passwd | more
```
## 1.12	)
```bash
man 5 passwd
```
## 1.13	)
```bash
man -a passwd
```

# 2	Lab 2
## 2.1	)
```bash
sudo useradd -c "Islamn Askar" islam
sudo passwd islam 
```
## 2.2	)
```bash
sudo useradd -c "Bad User" baduser
sudo passwd baduser
```
## 2.3	)
```bash
sudo groupadd -g 30000 pgroup
```
## 2.4	)
```bash
sudo groupadd badgroup
```
## 2.5	)
```bash
sudo usermod -aG pgroup islam
```
## 2.6	)
![[Pasted image 20241123153423.png|400]]
## 2.7	)
![[Pasted image 20241123153710.png|400]]
## 2.8	)
![[Pasted image 20241123154446.png|400]]
## 2.9	)
## 2.10	)
![[Pasted image 20241123154338.png|400]]