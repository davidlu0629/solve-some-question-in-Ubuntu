### Q1. could not get lock /var/lib/dpkg/lock
    Ans.  
      input: 
      
         sudo rm /var/cache/apt/archives/lock 
        
          sudo rm /var/lib/dpkg/lock 

Q2. boot and auto start some app before login
Ans.
  寫程式在/etc/init.d下 run_start.sh
  擺好還不算完成
  需要: sudo update-rc.d run_start.sh defaults 99 1
  update-rc.d為必須 defaults 99 1也為必須 會在rcS.d 多一個S+是字開頭的檔案
  在完全開機完成前要做的事在這做完全沒問題，但如果要做的事不會停止則需要在進入桌面後才能執行，
  否則，會形成無窮迴圈

Q3. auto start app after login
Ans. 
  use xwindows
  搜尋startup applications
  新增指令(terminal 指令)
  ex. gnome-terminal -e 'ryu-manager'

### Q4. install google calendar
  sudo add-apt-repository ppa:atareao/atareao  
  sudo apt update  
  sudo apt-get install calendar-indicator  
