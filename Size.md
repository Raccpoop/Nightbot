const girthRange = [0, 5];
 
const bestSizeMessage = "😳";
const largeSizeMessage = "Nice.";
const smallSizeMessage = "LMAO";
const worstSizeMessage = "💀";
 
const subCommands = ["+m", "+girth", "+duel"];
 
function GenerateNumber(min, max)
{
    return Math.floor(Math.random() * ((max + 1) - min) + min);
}
var sizer1 = GenerateNumber(sizeRange[0], sizeRange[1]);
var sizer2 = GenerateNumber(sizeRange[0], sizeRange[1]);
var sizerc = GenerateNumber(0, 1);
var size = 0;
var size2 = 0;
size = sizer1;
size2 = sizer2;
 
var girthr1 = GenerateNumber(girthRange[0], girthRange[1]);
var girthr2 = GenerateNumber(girthRange[0], girthRange[1]);
var girthrc = GenerateNumber(0, 1);
var girth = 0;
if(girthrc == 0) girth = girthr1;
else girth = girthr2;
 
var message = "";
if(size == sizeRange[1]) message = bestSizeMessage;
else if(size == sizeRange[0]) message = worstSizeMessage;
else if(size > (sizeRange[0] + sizeRange[1]) / 2) message = largeSizeMessage;
else if(size <= (sizeRange[0] + sizeRange[1]) / 2) message = smallSizeMessage;
 
var name;
if(q == "") name = u;
else
{
    name = q;
    if(name.includes(subCommands[0]) || name.includes(subCommands[1])) name = u;
}
var name2;
var winner;
if(q.includes(subCommands[2])) 
{
    name2 = q.substring(q.lastIndexOf("+") + 5);
    name = u;
}
winner = "The winner is " + name;
if(size < size2) winner = "The winner is " + name2;
else if( size == size2) winner = "The winner is nobody.";
 
var finalMessage = name + "'s PP size is " + size;
if(q.includes(subCommands[1])) finalMessage = finalMessage + "inches long. with a " + girth + "inch girth. ";
else finalMessage = finalMessage + "inch. ";
if(q.includes(subCommands[0])) finalMessage = finalMessage + message;
else if(q.includes(subCommands[2])) finalMessage = name + ": " + size + " | " + name2 + ": " + size2 + " | " + winner;
 
finalMessage;