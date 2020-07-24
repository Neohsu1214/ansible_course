# ansible_course

https://www.udemy.com/course/learn-ansible

課程中以 VirtualBox 從 [OSBOXES.ORG](https://www.osboxes.org/virtualbox-images/) 抓下來的 CentOS7 的 64bit image 建立三台 VM
1. ansible-controller
1. target1
1. target2

大致上ansible, ansible-playbook 就跟 docker, docker-compose 一樣
前者都是一個一個下指令驗證用，後者是把指令寫成yaml檔變成劇本來跑

ansible必須先建立inventory檔，將server分群分類，之後在劇本中就可以直接拿名稱或群組來用

整個ansible的執行流程可以建立變數，變數可以建立在 inventory, playbook(劇本) 或者寫在 /etc/ansible 的config 中當global變數

每個playbook的task可以寫判斷式 when 跟 loop(with_items) 來跑重複性的動作

playbook中的 task 中執行的指令都有 module 可以對應，比如操作檔案相關的，就是用 file，解壓縮的 unarchive ... 等等，很多東西可以用，清單與document要參考 ansible官網

ansible-galaxy很像是docker registry依樣的環境，可以在自己主機上建，或者pull官網的下來，許多人分享的 role都貢獻在那個平台上，但這塊我還不太會用...
