
**Raúl Mar**<br>
**Javier Rodríguez**

## Lexical Specification table

<head>
  <link href="../mdStyles/style.css" rel="stylesheet">
</head>
<body>
<table>
  <tr>
    <th>Lexeme</th>
    <th>Token Name</th>
    <th>Token</th>
    <th>REGEX</th>
    <th>Priority</th>
  </tr>
  <tr>
    <td>IF</td>
    <td>if</td>
    <td>&lt;IF:conditional&gt;</td>
    <td>r'if'</td>
    <td>3</td>
  </tr>
  <tr>
    <td>ELSE</td>
    <td>else</td>
    <td>&lt;ELSE:conditional&gt;</td>
    <td>r'else'</td>
    <td>4</td>
  </tr>
    <tr>    
    <td>WHILE</td>
    <td>while loop</td>
    <td>&lt;WHILE:loop&gt;</td>
    <td>r'while'</td>
    <td>5</td>
  </tr>
  <tr>    
    <td>VAR</td>
    <td>ID</td>
    <td>&lt;ID:name&gt;</td>
    <td>r'[a-zA-z][a-zA-z0-9_]*'</td>
    <td>1</td>
  </tr>
  <tr>    
    <td>CONST</td>
    <td>constant ID</td>
    <td>&lt;ID:const_name&gt;</td>
    <td>r'[a-zA-z][a-zA-z0-9_]*' </td>
    <td>2</td>
  </tr>
  <tr>    
    <td>STRING</td>
    <td>string type</td>
    <td>&lt;STRING:type&gt;</td>
    <td>r'[0-9]'</td>
    <td>12</td>
  </tr>
  <tr>    
    <td>BOOLEAN</td>
    <td>boolean type</td>
    <td>&lt;BOOL:type&gt;</td>
    <td>r'[.]*'</td>
    <td>11</td>
  </tr>
  <tr>    
    <td>NUMBER</td>
    <td>Numerical type</td>
    <td>&lt;NUM:type&gt;</td>
    <td>r'[0-9]*</td>
    <td>10</td>
  </tr>
  <tr>    
    <td>PLUS</td>
    <td>plus operation</td>
    <td>&lt;PLUS:+&gt;</td>
    <td>r'[\+]'</td>
    <td>15</td>
  </tr>
  <tr>    
    <td>MINUS</td>
    <td>minus operation</td>
    <td>&lt;MINUS:-&gt;</td>
    <td>r'-'</td>
    <td>16</td>
  </tr>
  <tr>    
    <td>DIVIDE</td>
    <td>Division Op</td>
    <td>&lt;DIV:/&gt;</td>
    <td>r'/'</td>
    <td>17</td>
  </tr>
  <tr>    
    <td>MULT</td>
    <td>Multiplicaton Op</td>
    <td>&lt;MULT:*&gt;</td>
    <td>r'[\*]'</td>
    <td>18</td>
  </tr>
  <tr>    
    <td>EQ</td>
    <td>Equals</td>
    <td>&lt;EQ:=&gt;</td>
    <td>r'='</td>
    <td>19</td>
  </tr>
  <tr>    
    <td>lParen</td>
    <td>Left parenthesis</td>
    <td>&lt;lParen:(&gt;</td>
    <td>r'\('</td>
    <td>6</td>
  </tr>
  <tr>    
    <td>rParen</td>
    <td>Right parenthesis</td>
    <td>&lt;rParen:)&gt;</td>
    <td>r'\)'</td>
    <td>7</td>
  </tr>
  <tr>    
    <td>lBckt</td>
    <td>Left bracket</td>
    <td>&lt;lBckt:{&gt;</td>
    <td>r'\{'</td>
    <td>8</td>
  </tr>
  <tr>    
    <td>rBckt</td>
    <td>Right bracket</td>
    <td>&lt;rBckt:}&gt;</td>
    <td>r'\}'</td>
    <td>9</td>
  </tr>  
  <tr>   
    <td>semiC</td>
    <td>Semi colon</td>
    <td>&lt;semiC:;&gt;</td>
    <td>r'[;]'</td>
    <td>13</td>
  </tr>
    <td>RETURN</td>
    <td>Global Variable</td>
    <td>&lt;VAR, loop&gt;</td>
    <td>r'[return]'</td>
    <td>14</td>
  </tr>
</table>
</body>

### Lexical Specification Python

```
tokens = (IF, ELSE, WHILE, VAR, LET, CONST, STRING, BOOL, NUMBER,
PLUS, MINUS, DIVIDE, MULT, EQ,
lPAREN, rPAREN, lBckt, rBckt, semiC
RETURN)

#tokens
t_IF       = r'if' 
t_ELSE     = r'else'
t_WHILE    = r'while'
t_VAR      = r'[a-zA-z][a-zA-z0-9_]*'
t_LET      = r'[a-zA-z][a-zA-z0-9_]*'     #starts with letters, then letters, numbers & _
t_CONST    = r'[0-9]'
t_STRING   = r'[.]*'                       #Any character except newline
t_NUMBER   = r'[0-9]*

t_PLUS     = r'[\+]'
t_MINUS    = r'-'
t_DIVIDE   = r'/'
t_MULT     = r'[\*]'
t_EQ       = r'='

t_lParen   = r'\('
t_rParen   = r'\)'
t_lBckt    = r'\{'
t_rBckt    = r'\}'
t_semiC    = r'[;]'

t_RETURN   = r'[return]'
```


