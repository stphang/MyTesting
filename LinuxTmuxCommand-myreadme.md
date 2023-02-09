# tmux shell
https://www.youtube.com/watch?v=Yl7NFenTgIo
sudo apt install tmux


## new pane
control + b then % // new right pane

control + b then " // new bottom pane

control + b then c // new windows

control + b then <windows_number> // switching pane/windows

control + b then , // rename windows name

control + b then d // detach this session

control + b then w // tmux windows for selection

control + b then <-- // pane navigation

## tmux 
tmux ls // list tmux windows // perform powershell

tmux attach -t <session_name/session_ID> // attach session , perform at powershell

tmux rename-session -t 0 mygit  // need to perform at powershell

tmux new -s mydocker // new session, named as session // run at powershell

tmux kill-session <session_name> // kill session , run at powershell	
