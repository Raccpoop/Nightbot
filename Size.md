 const subCommands = ["duel"];
 
function GenerateNumber(min, max)
{
    return Math.floor(Math.random() * ((max + 1) - min) + min);
}
var sizeR1 = GenerateNumber(sizeRange[0], sizeRange[1]);
var sizeR2 = GenerateNumber(sizeRange[0], sizeRange[1]);
var size = 0;
var size2 = 0;
size = sizeR1;
size2 = sizeR2;

var name;
if(q == "") name = u;
else name = q;
var name2;
var winner;
if(q.includes(subCommands[0])) 
{
    name2 = q.substring(q.lastIndexOf("d") + 4);
    name = u;
}
winner = "The winner is " + name;
if(size < size2) winner = "The winner is " + name2;
else if( size == size2) winner = "The winner is nobody.";
 
var finalMessage = name + "'s PP size is " + size + "inch.";

if(q.includes(subCommands[0]))
{
finalMessage = name + ": " + size + " | " + name2 + ": " + size2 + " | " + winner;
}
 
finalMessage;