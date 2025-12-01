**(# #)Class 01**

requied moduel ke baare me 


utils.js ki file me ek chota sa funtions bana kar export kar ke index.js js me import kya hai

Code
untils.js file code:

const sum = (a,b) => a+b;
const subs = (a,b) => a-b;
const multi = (a,b) => a*b;
const dived = (a,b) => a/b;


module.exports = {sum,subs,multi,dived}

Index.js ka code

const {sum,subs,multi,dived} = require('./utils')

console.log("ye function 2 value ko sum karta hai", sum(10,20))
console.log("ye function 2 value ko sum karta hai", subs(154,75))
console.log("ye function 2 value ko sum karta hai", multi(35,5))
console.log("ye function 2 value ko sum karta hai", dived(698,20))


import medule ke bare me pehly package.json me "type": "module" karna pary ga phr ap import ka syntacs use kar sago gy os code nechy dy rha hoon

utils files code sample

export const sum = (a,b) => a+b;
export const subs = (a,b) => a-b;
export const multi = (a,b) => a*b;
export const dived = (a,b) => a/b;

index.js file ka code

import { sum,subs,multi,dived} from './utils.js'

console.log("ye function 2 value ko sum karta hai", sum(10,20))
console.log("ye function 2 value ko sum karta hai", subs(154,75))
console.log("ye function 2 value ko sum karta hai", multi(35,5))
console.log("ye function 2 value ko sum karta hai", dived(698,20))


**(# #)Class 02**

## file Handling in node js

# file read code

import {readFile} from 'fs/promises'

//read file

const read_file = async (filename) =>{
    const date = await readFile (filename,"utf-8");
    console.log(date)
}
read_file('sample.txt')

# file Create code

//write file

const create_file = async (filename,content) =>{
    await writeFile (filename,content);
    console.log("file written successfully")
} 

create_file ('sample2.txt',"ye meri dosri file hai jo maine fs module se banai hai")

# file append file code

//append file


const append_file = async (filename,content) =>{
    await appendFile (filename,content);
    console.log("file appended successfully")
}
append_file ('sample2.txt',"\n ye mera new function hai jo maine append file ke liye banaya hai")

# Make Directory

//make directory

const make_directory = async (dir) =>{
    await mkdir (dir);
    // console.log("directory created successfully")
}  
make_directory ('components')

# Make recursive method

const make_directory = async (dir) =>{
    await mkdir (dir,{recursive:true});
    // console.log("directory created successfully")
}  
make_directory ('src/components/common/utils')

# Class 3 Path module in node js


import path from 'path';

## join two or more file paths

## expamle ap ke pas do file hain ek index.py or test.java in file ko joined kesaath jorna hai to ap join method ka use kar sakte hain

const fullPath = path.join('/path', 'index.py', 'file.java');
console.log("file joined is = ",fullPath); // Output: /path/index.py/file.java



## kise file ak absolute path ka pata karna hai

## absolute path

const absolutePath = path.resolve();

console.log("absolute path is = ",absolutePath); // Output: /Users/username/currentdirectory


## extension nikalna


const fileExtension = path.extname('rusume.pdf');

console.log("file extension is = ",fileExtension); // Output: .pdf

## extension nikalna or if condition ke sath chek karna


const fileExtension = path.extname('rusume.txt');

if (fileExtension==".pdf") {
    console.log("file has extension pdf allowed");
} else {
    console.log("file extension not allowed");
}


# Class 4 Building Server[http module] in node js
