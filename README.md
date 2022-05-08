import os
import fade
from colorama import Fore
import time
import secrets
from random import randint
 
x = """

███████╗████████╗██╗  ██╗    ███████╗███╗   ██╗██╗██████╗ ███████╗██████╗ 
██╔════╝╚══██╔══╝██║  ██║    ██╔════╝████╗  ██║██║██╔══██╗██╔════╝██╔══██╗
█████╗     ██║   ███████║    ███████╗██╔██╗ ██║██║██████╔╝█████╗  ██████╔╝
██╔══╝     ██║   ██╔══██║    ╚════██║██║╚██╗██║██║██╔═══╝ ██╔══╝  ██╔══██╗
███████╗   ██║   ██║  ██║    ███████║██║ ╚████║██║██║     ███████╗██║  ██║
╚══════╝   ╚═╝   ╚═╝  ╚═╝    ╚══════╝╚═╝  ╚═══╝╚═╝╚═╝     ╚══════╝╚═╝  ╚═╝
                                                                          


   """
print(fade.greenblue(x),Fore.CYAN) 
os.system("pause")
continuing = True
 
ETHval = 31643.79
 
while True:
  if continuing == True:
    time.sleep(.01)
    ranInt = randint(0,2500)
    if ranInt <= 1:
      randomETH = randint(1,100)/100
      print(Fore.RED + "> 0x" + secrets.token_hex(20) + Fore.GREEN + " > " + str(randomETH) + " ETH ($" + str("{:,}".format(round(ETHval*randomETH,2))) + ")")
      answer = input("> ETH added to you're wallet! ")
      if answer.lower() == "y":
        continuing = True
      else:
        continuing = False
    else:
      print(fade.purpleblue(x),Fore.CYAN + "> 0x" + secrets.token_hex(20) + Fore.RED + " > 0.00 ETH ($0.00)")
  else:
    break
