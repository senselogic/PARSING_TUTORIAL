# Parsing Tutorial

## Purpose

Shows how to translate a JavaScript language subset to pseudo-code instructions, using a recursive descent parser.

## Example

```javascript
var a = "hello" + 'hello';    // comment
var b = -1 + 2.0;

if ( a == 'hellohello' ) /* Print( '
Hello // " */
{
    document.write( '"' + a + "\"\n" );
}

if ( b == 0 )
{
    window.alert( 'oops' );
}
else if ( b == 1.0 )
{
    var x = window.prompt( 'name' );
}
else
{
    var r = window.confirm( 'bye ?' );

    if ( r )
    {
        document.write( 'bye !' );
    }
}

for ( var i = 1; i < 10; i++ )
{
    a = i + 1;
}

a = i / 10;

while ( a < 10 )
{
    b = a + 1;
    a += b;
}

do
{
    ++a;
}
while ( a < 100 );

for ( var i = 1; i < 20; i++ )
{
    for ( var j = 1; j - 1 < i + 1; j++ )
    {
        a = i + j;
        b = i - j;

        if ( i < j )
        {
            continue;
        }
        else
        {
            break;
        }
    }
}

var t = new Array( 'A', 'B', 'C' );
t += [ 'D', 'E', 'F' ];
t = [];
t = new Array();

function Test( a, b, c, d, e )
{
    var r = a;
    r -= b;
    r *= c;
    r /= d;

    return ( a + b + c + d + e ) / r;
}

Test( 1, 2, 3, 4, 5 );
```

```javascript
Put : "hello" + 'hello'
Into the variable : a

Put : -1 + 2.0
Into the variable : b

If : a == 'hellohello'

    Write in the document : '"' + a + "\"\n"

If : b == 0

    Show to the user : 'oops'

Else if : b == 1.0

    Ask the user : 'name'
    Put the answer into the variable : x

Else :

    Ask the user to confirm : 'bye ?'
    Put the answer into the variable : r
    
    If : r
    
        Write in the document : 'bye !'

For each : i
From : 1
While : i < 10

    Put : i + 1
    Into the variable : a

Put : i / 10
Into the variable : a

While : a < 10

    Put : a + 1
    Into the variable : b
    
    Add : b
    Into the variable : a

Repeat :

    Increment the variable : a

While : a < 100

For each : i
From : 1
While : i < 20

    For each : j
    From : 1
    While : j - 1 < i + 1
    
        Put : i + j
        Into the variable : a
        
        Put : i - j
        Into the variable : b
        
        If : i < j
        
            Repeat the loop
        
        Else :
        
            Exit the loop

Put the array : 'A' , 'B' , 'C'
Into the variable : t

Add the array : 'D' , 'E' , 'F'
Into the variable : t

Put an empty array
Into the variable : t

Put an empty array
Into the variable : t

Create the function : Test
With the parameters : a , b , c , d , e

    Put : a
    Into the variable : r
    
    Substract : b
    Into the variable : r
    
    Multiply by : c
    Into the variable : r
    
    Divide by : d
    Into the variable : r
    
    Return the value : ( a + b + c + d + e ) / r

Call the function : Test
With the arguments : 1 , 2 , 3 , 4 , 5
```

## Version

1.0

## Author

Eric Pelzer (ecstatic.coder@gmail.com).

## License

This project is licensed under the GNU General Public License version 3.

See the [LICENSE.md](LICENSE.md) file for details.
