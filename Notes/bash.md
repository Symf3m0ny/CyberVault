---
aliases:
type:
createdon: 2026-01-01 22:25:34
tags:
---
[[Linux]]
# Bash
---

The **B**ourne **A**gain **Sh**ell, was release in 1989 as a completely free alternative to the Bourne Shell (sh) and other proprietary shells.


---

**IMPORTANT**
These notes are not fully representative of the capabilities of Bash, but rather just areas of knowledge I felt I needed to have. Check out Black Hat Bash by Dolev Farhi and Nick Aleks from no starch press or the [[#References]] below for additional information.

## Configuration Files
---

Bash uses various configuration files, I've listed some of them out here and what their purpose is.

/etc/profile
~/.profile
~/.bash_profile
~/.bash_login
~/.bash_logout
~/.bashrc

## Scripting
---

### Operators

#### Arithmetic 
`+=` Incrementing by a constant
`-=` Decrementing by a constant

#### Control

`&`  Send command to the background
`&&` Used as a logical AND. The second command will run if the first one evaluates to true.
`( and )` Used for command grouping
`;` Used as a list terminator. A command following the terminator will run after the preceding one regardless if it evaluates to true or not.
`;;` Ends a case statement
`||` Used as a logical OR. The second command will run if the first one evaluates to fase.
#### Redirection

`>` Redirects stdout to a file.
`>>` Redirects stdout to a file by appending it to the existing document
`&> or >&` Redirects stdout and stderr to a file
`&>>` Redirects stdout and stderr to a file by appending them to the existing content
`<` Redirects input to a comand
`<<` Called a here document, or heredoc, redirects multiple lines to a command
`|` Redirects the output of a command as input to another command

### Arrays

Bash allows for single-dimensions Arrays. An Array can be defined with `()` and then an index can be selected using `[]`

```bash

# Create an Array
IP_ADDRESSES = (192.168.1.1, 192.168.1.10, 192.168.1.100)

# Print all the items in the Array
echo "${IP_ADDRESSES[*]}"

# Print the item at Index 0
echo "${IP_ADDRESSES[0]}"
```



## Tips
---

Printing variables with `${VariableName}` will improve readability


# References
---

