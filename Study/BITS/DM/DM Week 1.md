# Propositions, Truth Tables, and Connectives: Real-World Analogy
Let's first explain the basics of propositions, truth tables, and connectives with a simple real-world analogy. Then, we'll map these concepts to the detailed information provided in the video.
# **Simple Real-World Analogy: Lights and Switches**
## **Scenario: Controlling Lights with Switches**
Imagine you have two light switches, S1 and S2, and a light bulb. The light bulb's state (on or off) depends on the positions of these switches. Here's how we can relate this to propositions, truth tables, and connectives:
## **1. Propositions**:
- A proposition is like a statement about whether a light is on or off.
- **Example propositions:**
- S1 is on.
- S2 is off.
## **2. Truth Values:**
- The truth value of a proposition can be either true (T) or false (F).
- **For example:**
- S1 is on: True (if the switch is actually on).
- S2 is off: False (if the switch is actually on).
## **3. Logical Operators (Connectives):**
- Connectives combine propositions to form new statements.
- **Negation:**
- Denotes "not". If S1 is on, "not S1" means S1 is off.
- **Conjunction (AND):**
- Both conditions must be true for the result to be true.
- For the light to be on, both S1 and S2 must be on.
- **Disjunction (OR):**
- At least one condition must be true for the result to be true.
- For the light to be on, either S or S must be on.
    
    1
    
    2
    
## **4. Truth Tables:**
- A truth table lists all possible combinations of truth values for propositions and shows the result of the compound proposition.
- For example, the truth table for S AND S shows when the light will be on or off based on the positions of both switches.
    
    1
    
    2
    
# **Mapping to the Video Example:**
## **1. Propositions:**
- Defined as declarative sentences that are either true or false.
- Example: "India is a part of Asia" (True), "The sun rises from the West" (False).
## **2. Truth Values:**
- True (T) or False (F) based on the proposition's accuracy.
- Example: "1 + 1 = 2" is True, "2 + 3 = 4" is False.
## **3. Logical Operators (Connectives):**
**Negation:**
- Denoted as ¬p, meaning "not p".
- If p is True, ¬p is False, and vice versa.
**Conjunction (AND):**
- Denoted as p ∧ q.
- True only if both p and q are True.
**Disjunction (OR):**
- Denoted as p ∨ q.
- False only if both p and q are False.
## **4. Truth Tables:**
- List all possible truth values for propositions and their combinations.
- **Example for Negation:**
|   |   |
|---|---|
|𝑝|¬𝑝|
|𝑇|𝐹|
|𝐹|𝑇|
- **Example for Conjunction:**
|   |   |   |
|---|---|---|
|𝑝|𝑞|𝑝∧𝑞|
|𝐹|𝐹|𝐹|
|𝐹|𝑇|𝐹|
|𝑇|𝐹|𝐹|
|𝑇|𝑇|𝑇|
- **Example for Disjunction:**
|   |   |   |
|---|---|---|
|𝑝|𝑞|𝑝∨𝑞|
|𝐹|𝐹|𝐹|
|𝐹|𝑇|𝑇|
|𝑇|𝐹|𝑇|
|𝑇|𝑇|𝑇|
## **Summary:**
- **Propositions**: Declarative sentences that are true or false.
- **Truth Values:** True (T) or False (F).
- **Connectives:**
- **Negation (NOT):** Reverses the truth value.
- **Conjunction (AND):** True if both propositions are true.
- **Disjunction (OR):** True if at least one proposition is true.
- **Truth Tables:** Tables listing all possible truth values and results for compound propositions.
Using the analogy of controlling lights with switches helps illustrate how propositions and connectives work together to form logical statements, similar to how logical operators combine propositions to create compound propositions in mathematics.
  
# Conditional, Converse, Contrapositive, and Inverse: Real-World Analogy
Let's break down the concepts of conditional statements, converse, contrapositive, and inverse using a real-world analogy and map it to the information from the video.
# **Real-World Analogy: Promises and Outcomes**
Imagine a promise scenario involving a parent and a child. The parent makes a promise: "If you finish your homework, then you can watch TV."
## **1. Conditional Statement (Implication):**
- This is the original promise.
- **If p then q:** If you finish your homework (p), then you can watch TV (q).
- In logic, this is written as 𝑝→𝑞.
- The promise is broken only if the child finishes their homework (p is true) but is not allowed to watch TV (q is false).
## **2. Truth Table for Conditional Statement:**
- There are four possible combinations of whether the child finishes the homework (p) and whether they can watch TV (q):
|   |   |   |
|---|---|---|
|𝑝|𝑞|𝑝→𝑞|
|𝑇|𝑇|𝑇|
|𝑇|𝐹|𝐹|
|𝐹|𝑇|𝑇|
|𝐹|𝐹|𝑇|
- The only time 𝑝→𝑞 (the promise) is false is when the child finishes their homework (p is true) but cannot watch TV (q is false).
## **3. Understanding Conditional Statements with Intuition:**
- **True Promise:** If the child finishes their homework and watches TV, the promise is kept (True).
- **Broken Promise:** If the child finishes their homework but is not allowed to watch TV, the promise is broken (False).
- **Unrelated Cases:** If the child does not finish their homework, the promise does not apply, regardless of whether they watch TV or not (True).
## **4. Converse:**
- **Converse of** "If p then q" is "If q then p".
- **If q then p:** If you can watch TV, then you finished your homework.
- In logic, this is written as 𝑞→𝑝.
- This is not necessarily true; just because the child is watching TV does not mean they finished their homework.
## **5. Contrapositive:**
- **Contrapositive** of "If p then q" is "If not q then not p".
- **If not q then not p:** If you cannot watch TV, then you did not finish your homework.
- In logic, this is written as ¬𝑞→¬𝑝.
- This is logically equivalent to the original promise. If the child cannot watch TV, it implies they did not finish their homework.
## **6. Inverse:**
- Inverse of "If p then q" is "If not p then not q".
- If not p then not q: If you did not finish your homework, then you cannot watch TV.
- In logic, this is written as ¬𝑝→¬𝑞.
- This is not necessarily true; the child might not finish their homework and still watch TV.
# **Mapping to the Video:**
## **1. Conditional Statement (Implication):**
- **p implies q:** If p (you get 100% on the final exam), then q (you get an A in the course).
- This is false only when p is true and q is false.
## **2. Truth Table for Conditional:**
- The truth table for 𝑝→𝑞 shows it is true in all cases except when p is true and q is false.
## **3. Intuition for Implication:**
- Think of the implication as a promise. The promise is broken only when the premise (getting 100%) is true, but the conclusion (getting an A) is false.
## **4. Converse:**
- **q implies p**: If q (you get an A in the course), then p (you get 100% on the final exam).
- This is not necessarily true.
## **5. Contrapositive:**
- **Not q implies not p:** If not q (you do not get an A), then not p (you did not get 100% on the final exam).
- This is logically equivalent to the original implication.
## **6. Inverse:**
- Not p implies not q: If not p (you do not get 100% on the final exam), then not q (you do not get an A).
- This is not necessarily true.
## **Summary:**
- **Conditional (Implication):** If p, then q.
- **Converse:** If q, then p.
- **Contrapositive:** If not q, then not p.
- **Inverse:** If not p, then not q.
Using the analogy of a promise helps illustrate how conditional statements and their related forms work in logic, similar to how the original promise and its variations operate in real life.
![[BITSP-DM-Logical-Equivalences.pdf]]
![[BITSP-DM-Predicates-and-Quantifiers.pdf]]