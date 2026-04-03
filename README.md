# Ownership-Transfer-9
Ownership Transfer.sol
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract OwnershipTransfer {
    address public owner;

    constructor() {
        owner = msg.sender;
    }

    function transferOwnership(address newOwner) public {
        require(msg.sender == owner, "Not owner");
        owner = newOwner;
    }
}
