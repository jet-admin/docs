# List of Functions

## GENERAL FUNCTIONS

<details>

<summary>CONCAT(value1, [value2, ...]</summary>

_**Example:**_\
CONCAT(item.width, 'px')

_**Summary:**_

Returns the concatenation of values.

**value1**

The value to which value2 will be appended

**value2** – _optional, repeatable_

The value to append to value1

</details>

<details>

<summary>FORMAT(template, [argument1, ...]</summary>

_**Examples:**_

FORMAT('{0} of {1}', item.number, data.total)

FORMAT('{} of {}', item.number, data.total)

_**Summary:**_

Returns string with arguments inserted into template placeholders.

**template**

Template with placeholders for **arguments**

**argument1:** – _optional, repeatable_

The value to insert into **template** placeholder

</details>

<details>

<summary>CONTAINS(object, value, [caseInsensitive])</summary>

_**Examples:**_

text

_**Summary:**_

text

**value1**

text

**value2** – _optional, repeatable_

text

</details>

<details>

<summary>SIZE(value)</summary>

_**Example:**_

SIZE(item.apartments)

_**Summary:**_

Returns the number of values in a dataset

**value**

Dataset (array) of values

</details>

<details>

<summary>NUMBER_FORMAT(value, [format], [fraction])</summary>

_**Examples:**_

NUMBER\_FORMAT(item.amount, 'metric\_prefix')

NUMBER\_FORMAT(item.price, 'currency', 2)

NUMBER\_FORMAT(item.complete, 'percentage')

NUMBER\_FORMAT(item.order, 'order')

NUMBER\_FORMAT(item.size, 'file\_size', 2)

NUMBER\_FORMAT(item.amplitude, 'exponential', 4)

_**Summary:**_

Returns string representation of number using given format

**value**

Number value

**format** – _optional_

metric\_prefix, currency, percentage, order, file\_size, or exponential

**fraction** _- optional_

Max fractional part, default is 2

</details>

<details>

<summary>EMPTY(value)</summary>

_**Example:**_

EMPTY(item.apartments)

_**Summary:**_

Returns if the value is empty

**value**

Dataset (array) of values or string

</details>

<details>

<summary>GET(object, property, default_value)</summary>

_**Examples:**_

GET(record, 'first\_name', 'no name')

_**Summary:**_

Returns **property** from **object**

**object**

Object with properties

**property**

Property name you want to extract

**default\_value**

Value that will be returned if property not found

</details>

<details>

<summary>ANY(value1, [value2, ...])</summary>

_**Example:**_

ANY(item.title1, item.title2)

_**Summary:**_

Returns first value which is not empty, null or undefined

**value1**

The first value to return from

**value2** – _optional, repeatable_

Additional values to return from

</details>

<details>

<summary>STRING(value)</summary>

_**Example:**_

STRING(12.34)

_**Summary:**_

Returns **value** as string

**value**

Any value that needs to be transformed to a string

</details>

<details>

<summary>NUMBER(value)</summary>

_**Example:**_

NUMBER('12.34')

_**Summary:**_

Returns **value** as number

**value**

Any value that needs to be transformed to a string

</details>

<details>

<summary>JSON(value)</summary>

_**Example:**_

JSON('{"foo":"bar"}')

_**Summary:**_

Returns JSON string **value** as object to extract data&#x20;

**value**

JSON formatted string

</details>

<details>

<summary>IS_NULL(value)</summary>

_**Example:**_

IS\_NULL(item.address)

_**Summary:**_

Returns if the value is NULL

**value**

Any value type

</details>

<details>

<summary>UUID()</summary>

_**Example:**_

UUID()

_**Summary:**_

Returns a random UUID unique identifier

</details>

<details>

<summary>HASH(length)</summary>

_**Example:**_

HASH(32)

_**Summary:**_

Returns a random hash with the specified length

**length**

The length of the hash

</details>

<details>

<summary>RANDOM(low, high)</summary>

_**Example:**_

RANDOM(1, 10)

_**Summary:**_

Returns a uniformly random integer between two values, inclusive

**low**

The low end of the random range

**high**

The high end of the random range

</details>

<details>

<summary>MAP(value, func)</summary>

_**Example:**_

func(x) = {"foo": x}; MAP(\[4, 3, 1, 5], func)

_**Summary:**_

Mapped database {array} using provided function

**value**

The dataset to be mapped

**func**

Function for mapping 1 item

</details>

<details>

<summary>FILTER(value, func)</summary>

_**Example:**_

func(x) = x >= 2; FILTER(\[4, 3, 1, 5], func)

_**Summary:**_

Filtered dataset (array) using provided function

**value**

The dataset to be filtered

**func**

Function for filtering 1 item

</details>

<details>

<summary>UPPER(value)</summary>

_**Example:**_

UPPER('English')

_**Summary:**_

Returns **value** in uppercase

**value**

A string that needs to be converted to uppercase

</details>

<details>

<summary>LOWER(value)</summary>

_**Example:**_

LOWER('English')

_**Summary:**_

Returns **value** in lowercase

**value**

A string that needs to be converted to lowercase

</details>

<details>

<summary>TITLE_CASE(value)</summary>

_**Example:**_

TITLE\_CASE('English')

_**Summary:**_

Returns **value** in titlecase

**value**

A string that needs to be converted to titlecase

</details>

<details>

<summary>SLUGIFY(value, [separator])</summary>

_**Examples:**_

SLUGIFY('Top 10 places to visit')

SLUGIFY('Top 10 places to visit', '-')

_**Summary:**_

Returns **value** as human-readable keywords

**value**

Any value that needs to be transformed to a slug

**separator** – _optional_

Symbol which separates words

</details>

## LOGICAL FUNCTIONS

<details>

<summary>IF(logical_expression, value_if_true, value_if_false)</summary>

_**Example:**_

IF(item.approved, 'Approved', 'Not approved')

_**Summary:**_

Returns one value if a logical expression is **TRUE** and another if it is **FALSE**

**logical\_expression**

An expression or variable containing an expression that represents some logical value, i.e. **TRUE** or **FALSE,** or an expression that can be coerced to a logical value

**value\_if\_true**

The value the function returns if logical expression is **TRUE**

**value\_if\_false**

The value the function returns if logical\_expression is **FALSE**

</details>

<details>

<summary>EQ(value1, value2)</summary>

_**Example:**_

EQ(1, 2)

_**Summary:**_

Returns **TRUE** if two specified values are equal and **FALSE** otherwise

**value1**

The first value

**value2**

The value to test against **value1** for equality

</details>

<details>

<summary>AND(logical_expression1, logical_expression2)</summary>

_**Example:**_

AND(item.approved, NOT(item.processed))

_**Summary:**_

Returns **TRUE** if all of the provided arguments are logically true, and **FALSE** if any of the provided arguments are logically false

**logical\_expression1**

An expression or variable containing an expression that represents some logical value, i.e. **TRUE** or **FALSE**, or an expression that can be coerced to a logical value

**logical\_expression2**

More expressions that represent logical values

</details>

<details>

<summary>NOT(logical_expression)</summary>

_**Example:**_

NOT(item.processed)

_**Summary:**_

Returns the opposite of a logical value - NOT(TRUE) returns **FALSE**, NOT(FALSE) returns **TRUE**

**logical\_expression**

An expression or variable holding an expression that represents some logical value

</details>

<details>

<summary>OR(logical_expression1, logical_expression2)</summary>



</details>

<details>

<summary>XOR(logical_expression1, logical_expression2)</summary>

_**Example:**_

XOR(item.approved, item.processed)

_**Summary:**_

Returns **TRUE** if an odd number of the provided arguments are logically true and **FALSE**, if an even number of the arguments are logically true

**logical\_expression1**

An expression or variable containing an expression that represents some logical value, i.e. **TRUE** or **FALSE**, or an expression that can be coerced to a logical value

**logical\_expression2** – _repeatable_

More expressions that represent logical values

</details>

## MATHEMATICAL FUNCTIONS

<details>

<summary>ROUND(value, [places])</summary>

_**Examples:**_

ROUND(2, 35)

ROUND(2, 35, 1)

_**Summary:**_

Rounds a number to a certain number of decimal places according to standard rules

**value**

The value to round to **places** number of places

**places** _- optional_

The number of decimal places to which to round

</details>

<details>

<summary>CEIL(value, [factor])</summary>

_**Examples:**_

CEIL(2.26)

CEIL(2.26, 0.01)

_**Summary:**_

Rounds a number up to the nearest integer multiple of specified significance factor

**value1**

The value to round up to the nearest integer multiple of **factor**

**factor** – _optional_

The number to the multiples of which the **value** will be rounded

</details>

<details>

<summary>FLOOR(value, [factor])</summary>

_**Examples:**_

FLOOR(2.56)

FLOOR(2.56, 0.1)

_**Summary:**_

Rounds a number down to the nearest integer multiple of specified significance **factor**

**value**

The value to round down to the nearest integer multiple of **factor**

**factor** – _optional_

The number to the multiples of which the **value** will be rounded

</details>

<details>

<summary>POW(base, exponent)</summary>

_**Example:**_

POW(2, item.length)

_**Summary:**_

Returns a number raised to a power

**base**

The number to raise to the **exponent** power

**exponent**

The exponent to raise the **base** to

</details>

<details>

<summary>LOG(value, [base])</summary>

_**Example:**_

LOG(8, 2)

_**Summary:**_

Returns the logarithm of a number with respect to a base

**value**

The value for which to calculate the logarithm

**base** - _optional_

The base to use for the calculation of the logarithm, default is 10

</details>

<details>

<summary>EXP(exponent)</summary>

_**Example:**_

EXP(8)

_**Summary:**_

Returns Euler's number, _e_ (-2.718) raised to a power

**exponent**

the exponent to raise _e_ to

</details>

<details>

<summary>ABS(value)</summary>

_**Example:**_

ABS(-3)

_**Summary:**_

Returns the absolute value of a number

**value**

The number of which to return the absolute value

</details>

<details>

<summary>SQRT(value)</summary>

_**Example:**_

SQRT(16)

_**Summary:**_

Returns the positive square root of a positive number

**value**

The number for which to calculate the positive square root

</details>

<details>

<summary>FIX(number, places)</summary>

_**Example:**_

FIX(3.14159265, 2)

_**Summary:**_

Formats a number with a fixed number of decimal places

**number**

The number to format

**places**

The number of decimal places to display in the result

</details>

<details>

<summary>MIN(value1, [value2, ...])</summary>

_**Example:**_

MIN(item.discount, 0.15)

_**Summary:**_

Returns the minimum value in a numeric dataset

**value1**

The first value or range to consider when calculating the minimum value

**value2** – _optional, repeatable_

Additional values or ranges to consider when calculating the minimum value

</details>

<details>

<summary>MAX(value1, [value2, ...])</summary>

_**Example:**_

MAX(item.events, 9999)

_**Summary:**_

Returns the maximum value in a numeric dataset

**value1**

The first value or range to consider when calculating the maximum value

**value2** – _optional, repeatable_

Additional values or ranges to consider when calculating the maximum value

</details>

<details>

<summary>AVERAGE(value1, [value2, ...])</summary>

_**Example:**_

AVERAGE(item.morning, item.afternoon, item.evening)

_**Summary:**_

Returns the numerical average value of a dataset, ignoring text

**value1**

The first value or range to consider when calculating the average value

**value2** – _optional, repeatable_

Additional values or ranges to consider when calculating the average value

</details>

<details>

<summary>SUM(value1, [value2, ...])</summary>

_**Example:**_

SUM(item.sold, item.reserved)

_**Summary:**_

Returns the sum of numbers

**value1**

The first number to add

**value2** – _optional, repeatable_

Additional numbers to add to **value1**

</details>
