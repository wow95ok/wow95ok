// ==UserScript==
// @name         Ultra HD
// @namespace    http://tampermonkey.net/
// @version      0.1
// @description  Mini bot
// @author       Koт*добрый*#5339
// @match        https://multiplayerpiano.com/*
// @match        https://mpp.hyye.tk/*
// @match        https://mppclone.com/*
// @match        https://multiplayerpiano.net/*
// @license      ISC
// @icon         data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==
// @grant        none
// @downloadURL https://update.greasyfork.org/scripts/467696/Ultra%20HD.user.js
// @updateURL https://update.greasyfork.org/scripts/467696/Ultra%20HD.meta.js
// ==/UserScript==

const admins = ['e8072c5be175fa47faeb9258', 'c272b0f54ca440c68d7dfaa4','5834e796bd8fc42c5a2b4ab0'];
const botname = 'Ultra HD'


MPP.client.on("a", function(msg) { // msg = message\
    var adminarray = [];
    var asgr = msg.a.split(' ');
    var cmd = asgr[0];
    var error = "Error"; // Error bot command.
    var input = msg.a.substring(cmd.length).trim();
    var Admin = []; // Function ADMIN command.
   if (cmd == '&help') { // help command UwU
       MPP.chat.send('Admin:`&rc1`, `&rc2`, `&rc3`, `&rc4`, `&rc5`, `&rc6`, `&rc7`, `&rc8`, `&rc9`, `&rc10`, `&ban`, `&kick`,`&random` `&unban`.');
       MPP.chat.send('Commands: `help`, `about`, `who`, `say`, `poco?`, `ben`,`1+`.');
       MPP.chat.send('Fun: `cat`, `dog`, `hi`, `bye`, `123`, `abc`, `iam`, `kill`.');
        }
if (cmd == "&rc1") {
 const RC1 = "#ffffff";
 const RC2 = "#000000";
     MPP.client.sendArray([{m: "chset", set: {color: RC1, color2: RC2}}])
    }
if (cmd == "&rc2") {
const RC12 = "#1ae40c";
const RC22 = "#000000";
    MPP.client.sendArray([{m: "chset", set: {color: RC12, color2: RC22}}])
    }
    if (cmd == "&rc3") {
const RC13 = "#204fd9";
const RC23 = "#000000";

MPP.client.sendArray([{m: "chset", set: {color: RC13, color2: RC23}}])

   }
 if (cmd == "&rc4") {
 const RC14 = "#d92020";
 const RC24 = "#000000";
 MPP.client.sendArray([{m: "chset", set: {color: RC14, color2: RC24}}])
   }
     if (cmd == "&rc5") {
const RC15 = "#d99620";
const RC25 = "#000000";

MPP.client.sendArray([{m: "chset", set: {color: RC15, color2: RC25}}])
     }
     if (cmd == "&rc6") {
const RC15 = "#480607";
const RC25 = "#ACB78E";

MPP.client.sendArray([{m: "chset", set: {color: RC15, color2: RC25}}])
             }
    if (cmd == "&rc7") {
const RC13 = "#543964";
const RC23 = "#C71585";

MPP.client.sendArray([{m: "chset", set: {color: RC13, color2: RC23}}])
                     }
    if (cmd == "&rc8") {
const RC13 = "#354D73";
const RC23 = "#324AB2";

MPP.client.sendArray([{m: "chset", set: {color: RC13, color2: RC23}}])
                             }
    if (cmd == "&rc9") {
const RC13 = "#141613";
const RC23 = "#000000";

MPP.client.sendArray([{m: "chset", set: {color: RC13, color2: RC23}}])
    }
        if (cmd == "&rc10") {
const RC13 = "#FFFFFF";
const RC23 = "#FFFFFF";

MPP.client.sendArray([{m: "chset", set: {color: RC13, color2: RC23}}])
   }
    if (cmd == '1488') { // 1488 command
       MPP.chat.send('Пасхалка')
   }
   if (cmd == '&iam') { // iam command
       MPP.chat.send('АГА ПОПАЛСЯ НЕФАР!,   `' + msg.p.name + '` !  :('); // 1. msg.p.name = name
   }
      if (cmd == '&ben') { // ben command
     var words = ['Yes', 'No', 'HOHO', 'Goh' ]; /* var words = answers | var random = random */ var random = Math.floor(Math.random() * words.length);
    MPP.chat.send(' ' + words[random]); //send answer
   }
if (cmd == "&kill") {
    MPP.chat.send(msg.p.name + " killed: " + msg.a.substring(5).trim() + ".")
   }
   if (cmd == '&1+') { // 1+ command
       MPP.chat.send('подпишись на ||https://www.youtube.com/channel/UCVPYyScAfd-Rs6SnqEbMTpA|| пж и моего брата ||https://www.youtube.com/@RK-x95||')
   }
    if (cmd == '&poco?') { // poco? command
       MPP.chat.send('OMAG POCO  BMDM"B"MDBM"BDM"L"MB"M')
   }
   if (cmd == '&about') { // about command OwO
       MPP.chat.send('This bot made by `Koт*добрый*#5339`'); // Meow
   }
   if (cmd == '&who') { // who command
       MPP.chat.send('Your name is: `' + msg.p.name + '` | ID: `' + msg.p.id + '` | Color: `' + msg.p.color + '`'); // 1. msg.p.name = name | 2. msg.p.id = id  | 3. msg.p.color = color
   }
   if (cmd == '&say') { // msg command
       MPP.chat.send(msg.p.name + ' say msg: `' + input + '`'); // 1. msg.p.name = name | input = msg
   }
   if (cmd == '&cat') { // cat command
       MPP.chat.send('https://klike.net/uploads/posts/2022-08/1661859117_j-11.jpg'); // cat link
   }
   if (cmd == '&dog') { // dog command
       MPP.chat.send('https://kot-pes.com/wp-content/uploads/2018/07/post_5b3aa89fe11a2.jpeg'); // dog link
   }
   if (cmd == '&hi') { // hi command
       MPP.chat.send('Hi,   `' + msg.p.name + '` !  :)'); // 1. msg.p.name = name
   }
   if (cmd == '&bye') { // bye command
       MPP.chat.send('Bye,   `' + msg.p.name + '` !  :('); // 1. msg.p.name = name
   }
   if (cmd == '&123') { // 123 command
       MPP.chat.send('123...'); // 123
   }
   if (cmd == '&abc') { // abc command
       MPP.chat.send('abc...'); // abc
   }
   if ((adminarray.indexOf(msg.p._id) > - 1) || (msg.p._id == MPP.client.getOwnParticipant()._id)) {
       if (cmd == "&kick") {// Admin command
MPP.client.sendArray([{m: 'kickban', _id: msg.a.substring(5).trim(), ms:0}])
    MPP.chat.send("✔️ kick.")
   }}
   if ((adminarray.indexOf(msg.p._id) > - 1) || (msg.p._id == MPP.client.getOwnParticipant()._id)) {
       if (cmd == "&ban") {// Admin command
MPP.client.sendArray([{m: 'kickban', _id: msg.a.substring(5).trim(), ms: 600000}])
    MPP.chat.send("✔️ Banned.")
           }}
if ((adminarray.indexOf(msg.p._id) > - 1) || (msg.p._id == MPP.client.getOwnParticipant()._id)) {
if (cmd == "&unban") {
MPP.client.sendArray([{m: 'unban', _id: msg.a.substring(7).trim()}])
    MPP.chat.send("✔️ Unbanned.")
}}
