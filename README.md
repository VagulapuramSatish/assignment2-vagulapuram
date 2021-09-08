# assignment2-vagulapuram
# Satish Vagulapuram
## Switzerland
Switzerland, officially the **Swiss Confederation**, is a **landlocked country** situated at the confluence of Western, Central and Southern Europe. A landlocked country of towering mountains, deep Alpine lakes, grassy valleys dotted with neat farms and small villages, and thriving cities that blend the old and the new, Switzerland is the nexus of the diverse physical and cultural geography of western Europe, renowned for both its **natural beauty and its way of life**.
---
## Travelling to Switzerland
1. The fastest way to travel from Maryville to Switzerland is Airways.
2. First go to the Kansas city international airport by road ways.
   1. Book a flight from Kansas city to Switzerland.
3. After that, I will reach my favourite Destination.

* Some clothes
* Hat
* Food
  * Snacks
  * Biscuits

**[AboutMe](AboutMe.md)**

---

## tables

This table shows the data related to my favourite food items. Which I would recommend others.

|FOOD|LOCATION|AMOUNT|
|---|---|---|
|Biryani|Bawarchi|$15|
|Ras malai|Radhe Sweet Shop|$5|
|Paneer Butter masala with butter naans|Santhosh Dhaba|$20|
|Butter Chicken|N village|$10|
|Chocolate Cake ice-cream|Masquti|$10|
|Lassy|Galaxy lassi point|$5|

---

## My Quotes

>You cannot believe in God until you believe in yourself.
-*Swami Vivekananda*

>Your time is limited, so don't waste it living someone else's life. Don't be trapped by dogma – which is living with the results of other people's thinking.
-*Steve Jobs*

---

## Code Fencing

   struct Montgomery {
      Montgomery(u128 n) : mod(n), inv(1), r2(-n % n) {
         for (int i = 0; i < 7; i++)
             inv *= 2 - n * inv;

         for (int i = 0; i < 4; i++) {
             r2 <<= 1;
             if (r2 >= mod)
                 r2 -= mod;
         }
         for (int i = 0; i < 5; i++)
             r2 = mul(r2, r2);
     }

     u128 init(u128 x) {
         return mult(x, r2);
     }

     u128 mod, inv, r2;
 }

 >Montgomery modular multiplication relies on a special representation of numbers called Montgomery form. The algorithm uses the Montgomery forms of a and b to efficiently compute the Montgomery form of ab mod N. The efficiency comes from avoiding expensive division operations. Classical modular multiplication reduces the double-width product ab using division by N and keeping only the remainder. This division requires quotient digit estimation and correction. The Montgomery form, in contrast, depends on a constant R > N which is coprime to N, and the only division necessary in Montgomery multiplication is division by R. The constant R can be chosen so that division by R is easy, significantly improving the speed of the algorithm. In practice, R is always a power of two, since division by powers of two can be implemented by bit shifting.

 [Montgomery multiplication](https://en.wikipedia.org/wiki/Montgomery_modular_multiplication)

  function MultiPrecisionREDC is
     Input: Integer N with gcd(B, N) = 1, stored as an array of p words,
            Integer R = Br,     --thus, r = logB R
            Integer N′ in [0, B − 1] such that NN′ ≡ −1 (mod B),
            Integer T in the range 0 ≤ T < RN, stored as an array of r + p words.

     Output: Integer S in [0, N − 1] such that TR−1 ≡ S (mod N), stored as an array of p words.

     Set T[r + p] = 0  (extra carry word)
     for 0 ≤ i < r do
         --loop1- Make T divisible by Bi+1

         c ← 0
         m ← T[i] ⋅ N′ mod B
         for 0 ≤ j < p do
             --loop2- Add the low word of m ⋅ N[j] and the carry from earlier, and find the new carry

             x ← T[i + j] + m ⋅ N[j] + c
             T[i + j] ← x mod B
             c ← ⌊x / B⌋
         end for
         for p ≤ j ≤ r + p − i do
             --loop3- Continue carrying

             x ← T[i + j] + c
             T[i + j] ← x mod B
             c ← ⌊x / B⌋
         end for
     end for

     for 0 ≤ i < p do
         S[i] ← T[i + r]
     end for

     if S ≥ N then
         return S − N
     else
         return S
     end if
  end function

 [Code Source](https://en.wikipedia.org/wiki/Montgomery_modular_multiplication)


