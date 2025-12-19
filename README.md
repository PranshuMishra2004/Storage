# Storage
A basic smart contract 
// SPDX-License-Identifier: MIT

pragma solidity ^0.8.18;

contract Strorage1{

    uint256 Number;     // let a number variable default to 0

    function Store (uint256 numberToSave) view  public{   //fucntion to store Number
        numberToSave=Number;
    }

    function retrive() public view returns(uint256) {    // fucntion to retrieve Number
        return Number;
    }

    struct Person {         // struct an array
        uint256 age;
        string Name;
    }
    Person[] public people;   // create an dynamic array

    mapping (string => uint256) public nameToNumber;  // mapping the stored number to a perticular string

    function addPeople(uint256 number,string memory name) public {   // add name and number to array
        people.push(Person(number, name));
        nameToNumber[name]= number;    // mapping the number passed to the passed string
    }

}
