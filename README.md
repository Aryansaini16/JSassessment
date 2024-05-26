/* 
// Metacrafters - Beginning Javascript
//
// This is a javascript playground for testing your javascript code!
// When you are ready to test, simply right click and select "Run Code"
// to see the result print below. If you have more then one snippet of code,
// you can highlight the code you want to test, and then right click and select "Run Code"
*/

// Enter your code below this line

// Code example
/*
Assessment Requirements
1. Create a variable that can hold a number of NFT's. What type of variable might this be?
2. Create an object inside your mintNFT function that will hold the metadata for your NFTs. 
   The metadata values will be passed to the function as parameters. When the NFT is ready, 
   you will store it in the variable you created in step 1
3. Your listNFTs() function will print all of your NFTs metadata to the console (i.e. console.log("Name: " + someNFT.name))
4. For good measure, getTotalSupply() should return the number of NFT's you have created
*/

// create a variable to hold your NFT's
const NFTs = []
// this function will take in some values as parameters, create an
// NFT object using the parameters passed to it for its metadata, 
// and store it in the variable above.
function mintNFT ($name,$eyecolor,$shirtType,$bling) {//parameters starting with $ to distinguish as a parameters
    const NFT = {
        "name": $name,//creating obj for parameters
        "eyecolor": $eyecolor,
        "shirtType": $shirtType,
        "bling": $bling
    }
    NFTs.push(NFT);//adding data declared in NFT to empty array NFTs
    console.log("minted:" + $name);//print it to check the success of the code
}

// create a "loop" that will go through an "array" of NFT's
// and print their metadata with console.log()
function listNFTs () {//print all NFTs metadata to console
 for(let i=0; i< NFTs.length; i++){
    console.log("\n" + NFTs[i].name);
    console.log(NFTs[i].eyecolor);
    console.log(NFTs[i].shirtType);
    console.log(NFTs[i].bling);
 }
}

// print the total number of NFTs we have minted to the console
function getTotalSupply() {//show number of NFTs created
 console.log("\n"+ NFTs.length);
}

// call your functions below this line
mintNFT("Aryan","Brown","shirt","gold chain");
mintNFT("Aakash","Brown","T-shirt","silver chain");
mintNFT("Ravneet","Black","Hoddie","watch");
mintNFT("Madhav","Black","Kurta","Bracelete");
listNFTs();
getTotalSupply();
