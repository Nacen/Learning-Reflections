# Reflections for May 28

## Forms and Inputs

### Making Code simple

I've learned something new with python called List Comprehension
It simplifies the idea of

for item in list
    condition
        expression

to the syntax of

expression for item in list  if conditional

example of this is

* list example

x = [i for i in range(10)]
print x

this will give the output:

[0,1,2,3,4,5,6,7,8,9]

without list comprehension

for i in range(10):
    x.append(i)

* Dictionary Example

month_abbvs = dict((m[:3].lower(), m) for m in months)

without list comprehension
for m in months:
    month_abbvs[m[:3].lower()] = m