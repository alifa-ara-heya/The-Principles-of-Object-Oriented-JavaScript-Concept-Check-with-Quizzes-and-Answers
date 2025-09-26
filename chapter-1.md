# The-Principles-of-Object-Oriented-JavaScript-Concept-Check-with-Quizzes-and-Answers

Sure — here's the complete Markdown study note with every question including the a/b/c/d options and the correct answers shown.

📘 JavaScript Quiz Notes

Based on The Principles of Object-Oriented JavaScript, Chapter 1: Primitive and Reference Types


---

Section 1: Core Concepts & Definitions (Q1–Q5)

1. List the five primitive types in JavaScript.
Short Answer: Undefined, Null, Boolean, Number, String


2. Storage Difference: What is the fundamental difference in how primitive values and reference values are stored relative to the variable object in JavaScript?
Short Answer:

Primitive values are stored directly in the variable's storage.

Reference values store a reference (pointer) to an object in memory; the variable holds that reference.



3. Default Value: Which primitive type is the value automatically assigned to a variable that has been declared but not initialized?

a) null

b) undefined

c) Boolean

d) Object
Answer: b) undefined



4. Value vs. Reference: When you assign one variable holding a primitive value to another variable (e.g., var a = 10; var b = a;), what kind of data transfer occurs?

a) A reference/pointer to the value is copied.

b) The entire value is copied into the new variable's storage location.

c) The new variable becomes an alias for the first variable.
Answer: b) The entire value is copied into the new variable's storage location.



5. Literal Representation: What term is used for a value that is not stored in a variable, such as a hardcoded name or number (e.g., "Nicholas" or 25)?
Short Answer: Literal (or literal value)




---

Section 2: Identifying Types & The typeof Operator (Q6–Q10)

6. The null Issue: What is the string value that the typeof operator incorrectly returns for the primitive value null?
Short Answer: "object"


7. typeof for References: For all reference types (like Arrays, Dates, and custom Objects), what is the return value of the typeof operator, except when used on a function?
Short Answer: "object"


8. Array Identification: What is the most reliable operator or method recommended in the chapter to confirm that a value is an Array, as the typeof operator is not sufficient?
Short Answer: Array.isArray(value)


9. instanceof Utility: The instanceof operator takes two parameters: an object and a constructor. What does it return if the object is an instance of the type that the constructor specifies?
Short Answer: true


10. True or False: Since JavaScript lacks formal class support, it also lacks the concept of types like primitive and reference entirely.
Answer: False




---

Section 3: Objects, Properties, and Syntax (Q11–Q15)

11. Dereferencing: What should an object variable be set to when there are no more references to the object in memory, allowing the garbage collector to free up the memory space?
Short Answer: null (set the variable to null)


12. Property Access: Which of the two property access notations (dot notation or bracket notation) allows you to use a variable to specify the property you want to access?
Short Answer: Bracket notation — obj[variableName]


13. Literal Forms: Provide the correct syntax for an Object Literal and an Array Literal.



Object Literal: { key: value, anotherKey: anotherValue }

Array Literal: [element1, element2, element3]


14. Dynamic Properties: True or False: You can add and remove properties from JavaScript objects (that you create) at any point during code execution.
Answer: True


15. Function Literal: What is the term for a function that is used where other values can also be used, such as an assignment expression, function parameter, or return value of another function?



a) Function Declaration

b) Function Constructor

c) Function Expression

d) Function Overloading
Answer: c) Function Expression



---

Section 4: Primitive Wrapper Types (Q16–Q20)

16. Primitive Methods: Why can a primitive string value like "hello".toUpperCase() execute a method, even though the chapter states that primitive values themselves are not objects?
Short Answer: JavaScript temporarily wraps the primitive in its corresponding wrapper object (e.g., a String object) so the method can be invoked, then discards the wrapper.


17. Wrapper Type Creation: Primitive wrapper types (String, Number, Boolean) are automatically created when you try to access a property or method on a primitive value. What happens to this wrapper object immediately after the method or property access is complete?
Short Answer: The temporary wrapper object is immediately discarded (garbage-collected when eligible).


18. Wrapper instanceof: If you check a primitive value against its wrapper type using instanceof (e.g., "Nicholas" instanceof String), the result is false. Why?
Short Answer: Because "Nicholas" is a primitive string, not an instance of the String object type.


19. Manual Wrapper Side Effect: If you manually create a primitive wrapper type instance using the new operator (e.g., new Boolean(false)), what is the potentially confusing result when you check its type using the typeof operator?
Short Answer: typeof new Boolean(false) returns "object" (not "boolean"), since you created an object wrapper.


20. Conditional Danger: Why does a Boolean object created manually (new Boolean(false)) still execute code within an if statement (e.g., if (new Boolean(false)) { ... })?
Short Answer: Because all objects are truthy in JavaScript — the if checks the truthiness of the expression (an object), not the wrapped primitive value. So new Boolean(false) is truthy even though it wraps the primitive false.
