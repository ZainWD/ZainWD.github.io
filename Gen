var website;
website = prompt("What's the name of website? (Lowercase characters only)");
var passArray = [website.charAt(0), website.charAt(1), website.charAt(2), website.charAt(3), website.charAt(4), website.charAt(5), website.charAt(6)];
var replaceArray = ["aas", "vbn", "xcv", "sdf", "wer", "dfg", "fgh", "ghj", "uio", "hjk", "jkl", "kll", "nmm", "bnm", "iop", "opp", "qqw", "ert", "asd", "rty", "yui", "cvb", "qwe", "zxc", "tyu", "zzx"];
var alphabet = ["a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z"];
var cycle = 0; // this cycle is for which index in replaceArray you are on
var cycle2 = 0; // this cycle is for which index in passArray you are on
var capitalizedLetters = 0;
var charReplaced = "no";
var keyword;
var tempNumb = 0;
var specialChar;

replaceLetters();
keyword = prompt("Enter a keyword of up to 10 characters (Lowercase characters only)");
var keywordArray = [keyword.charAt(0), keyword.charAt(1), keyword.charAt(2), keyword.charAt(3), keyword.charAt(4), keyword.charAt(5), keyword.charAt(6), keyword.charAt(7), keyword.charAt(8), keyword.charAt(9)];
removeItem(keywordArray, 9);
removeItem(keywordArray, 7);
removeItem(keywordArray, 5);
removeItem(keywordArray, 3);
removeItem(keywordArray, 1);
keywordArray = keywordArray.join('');
var password;
password = passArray.join('');
password = password + keywordArray;
var splitted = password.split("");
var strLength = splitted.length;
for (var i = 1; i < strLength; i += 3) {
splitted[i] = splitted[i].toUpperCase();
capitalizedLetters++;
}
password = splitted.join("");
var lowerLetters = password.length - capitalizedLetters;
var passNumb;
passNumb = lowerLetters - capitalizedLetters;
if (passNumb < 10) { 
  password = password + "0";
}
password = password + passNumb;
if (passNumb > 9) {
  tempNumb = passNumb - 10;
} else {
  tempNumb = passNumb;
}
findSpecialChar();
password = password + specialChar;
alert("Your password is"+password);

function replaceLetters() {
passArray = passArray.filter(Boolean);
while (charReplaced == "no") {
  if (passArray[cycle2] == alphabet[cycle]) {
   removeItem(passArray, cycle2);
   insertItem(passArray, cycle2, replaceArray[cycle]);
   cycle2++;
   cycle = 0;
   if (cycle2 == passArray.length) {
     charReplaced = "yes";
    }
} else {
    cycle++;
}
}
}

function findSpecialChar() {
  if (tempNumb === 0) {
    specialChar = ")";
  } else if (tempNumb === 1) {
    specialChar = "!";
  } else if (tempNumb === 2) {
    specialChar = "@";
  } else if (tempNumb === 3) {
    specialChar = "#";
  } else if (tempNumb === 4) {
    specialChar = "$";
  } else if (tempNumb === 5) {
    specialChar = "%";
  } else if (tempNumb === 6) {
    specialChar = "^";
  } else if (tempNumb === 7) {
    specialChar = "&";
  } else if (tempNumb === 8) {
    specialChar = "*";
  } else {
    specialChar = "(";
  }
}

