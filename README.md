## 42 Project - Get Next Line

For get next line we need to read from the file and return each new line.

This can get tough when the line is shorter or longer than the amount you read.

`BUFF_SIZE` is the macro we are setting for the read size,

lets say `BUFF_SIZE = 2`

If we had a file that was longer than that, it would need to keep reading.

As many times as it takes till it found a new line, or the end of the file.

Our function needs to be ready for that.

In another direction, what if out file is very small, but has many new lines.

Example file:
```
A
B
C
D
```
<table>
<tr>
<td>A</td>
<td>\n</td>
<td>B</td>
<td>\n</td>
<td>C</td>
<td>\n</td>
<td>D</td>
<td>\n</td>
</tr>
</table>

It's only 8 bytes, but it is made of 4 lines.

We need to return each one. 

In the case of `BUFF_SIZE = 2`, this isn't so bad.

It's perfect really.

We read two bytes:

<table>
<tr>
<td>A</td>
<td>\n</td>
<td> </td>
<td> </td>
<td> </td>
<td> </td>
<td> </td>
<td> </td>
</tr>
</table>

Then return up to the new line: `A`

We can read again and overwrite the old line.

But what about `BUFF_SIZE = 8`?

We read eight bytes:

<table>
<tr>
<td>A</td>
<td>\n</td>
<td>B</td>
<td>\n</td>
<td>C</td>
<td>\n</td>
<td>D</td>
<td>\n</td>
</tr>
</table>

How will we handle cutting up the data, returning the next line?

Saving the leftovers?

That is the point of using a static variable in this project.

---
*More notes to come, hope this helps for now*

#### TODO

* finish outline
* common pitfalls
* how to test get next line
* upload test suite
* link to more resources
