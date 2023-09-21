### Configure bash
` sudo apt install figlet `\
` cd `\
` nano .bashrc `\
edit and add scripts
```
#——————————————////
# Colors:
#——————————————////
black='\e[0;30m'
blue='\e[0;34m'
green='\e[0;32m'
cyan='\e[0;36m'
red='\e[0;31m'
purple='\e[0;35m'
brown='\e[0;33m'
lightgray='\e[0;37m'
darkgray='\e[1;30m'
lightblue='\e[1;34m'
lightgreen='\e[1;32m]'
lightcyan='\e[1;36m]'
lightred='\e[1;31m'
lightpurple='\e[1;35m'
yellow='\e[1;33m'
white='\e[1;37m]'
nc='\e[0m]'
#——————————————////
echo -e "${lightblue}";figlet "GEMBEL";
echo "================================================="
echo -e "${lightgreen}Informasi waktu : \t${lightpurple}"; date;echo " ";
echo -e "${lightgreen}Informasi Kernel : \t${lightpurple}"; uname -smr;
#———————————————#
echo -e "${lightred}";echo "Indonesia linux Community";
echo "~~~~~~~~~~~~~~~~~~~~~~~~~~";

#export PS1="\[$(tput setaf 3)\]\u@\h:\w $ \[$(tput sgr0)\]"
export PS1="\[${lightgreen}\]\u@\h:\w $ \[$(tput sgr0)\]"
```
save with `ctl + x` and `enter`
