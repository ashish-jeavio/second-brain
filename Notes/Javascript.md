
`Note : Remaining : Generator functions, Proxy & Reflect`

---
Resources :

https://youtu.be/eiC58R16hb8?si=gqzp_p5MthCBuc5P

https://youtu.be/vKJpN5FAeF4?si=vlfqtFJe39MgU_Mb

https://youtu.be/AOPmqw9scfc?si=Z_smWyRnRt_hxNfd

https://youtu.be/IJ6EgdiI_wU?si=N5f4eTGjwZfVem6X

yet to watch : https://youtu.be/TGGoiJBuv-Y?si=GtxDch0sEZghrqaq , https://youtu.be/9jl1lhFylJs?si=OCUHH9NdnR50be5d

---

Notes : Every function that accesses an outer variable is a closure.

----

# 🔥 **THE DEFINITIVE JAVASCRIPT TYPE COERCION CHEAT SHEET**
---

# ✅ **1. JavaScript Does Automatic Type Conversion (Coercion)**

JavaScript tries to convert values **implicitly** when different types are used together.

There are **three** important conversions:

### **1. ToPrimitive (object → primitive)**

### **2. ToString (value → string)**

### **3. ToNumber (value → number)**

Most weirdness comes from these conversions happening at the wrong time.

---

# 🔥 **2. The SINGLE most important rule:**

# 💡 **`+` operator behaves differently from all other operators.**

| Operator                     | Coercion Rule                                                       |
| ---------------------------- | ------------------------------------------------------------------- |
| **`+`**                      | If either operand is a **string**, JS does **string concatenation** |
| **`-`, `*`, `/`, `%`, `**`** | ALWAYS convert operands to **numbers**                              |

This ALONE explains >90% of coercion weird cases.

---

# 🔵 **3. Why `+` behaves weirdly**

Because `+` is **overloaded**:

### It can mean:

* **Numeric addition**
* **String concatenation**

So JS checks:

```
If any operand is string → convert both to string → concatenate.
Else → convert to number → add.
```

### Examples:

```
1 + "1" → "1" + "1" = "11"
"5" + 2 → "5" + "2" = "52"
```

---

# 🔴 **4. Why `-`, `/`, `*` do NOT behave like `+`**

These operators **only have numeric meaning**.

So JS converts operands to **numbers** first:

```
"5" - 2
→ Number("5") - 2
→ 5 - 2 = 3
```

Same for multiply/divide:

```
"2" * "3" → 6
"10" / "5" → 2
```

---

# 🟢 **5. How primitives convert internally**

## **5.1 ToNumber Conversion Rules**

Here’s the full mapping:

| Value       | ToNumber result |
| ----------- | --------------- |
| `"10"`      | 10              |
| `" 10 "`    | 10              |
| `""`        | 0               |
| `" "`       | 0               |
| `true`      | 1               |
| `false`     | 0               |
| `null`      | 0               |
| `undefined` | **NaN**         |
| `"abc"`     | **NaN**         |
| `[]`        | 0               |
| `[5]`       | 5               |
| `{}`        | NaN             |
| `["1","2"]` | NaN             |

---

## **5.2 ToString Conversion Rules**

| Value       | ToString result     |
| ----------- | ------------------- |
| `1`         | `"1"`               |
| `true`      | `"true"`            |
| `[]`        | `""`                |
| `[1,2]`     | `"1,2"`             |
| `{}`        | `"[object Object]"` |
| `null`      | `"null"`            |
| `undefined` | `"undefined"`       |

This explains:

```
[] + [] → "" + "" = ""
[] + {} → "" + "[object Object]"
{} + [] → tricky parsing; can be "[object Object]" or 0
```

---

# 🟣 **6. ToPrimitive (for objects, arrays, dates)**

When JS needs a primitive from an object/array:

1. Try `valueOf()`
2. If still object → try `toString()`
3. If still object → throw error

### Arrays:

```
[].toString() → ""
[1,2].toString() → "1,2"
```

### Objects:

```
{}.toString() → "[object Object]"
```

---

# 🔥 **7. Why these specific weird cases happen**

### **Case: `"10" - "5" + "2"` → `"52"`**

Step 1: `"10" - "5"` → numeric → `5`
Step 2: `5 + "2"` → string concat → `"52"`

---

### **Case: `null + 1` → 1**

Because:

```
null → 0  
0 + 1 = 1
```

---

### **Case: `undefined + 1` → NaN**

Because:

```
undefined → NaN  
NaN + 1 = NaN
```

---

### **Case: `" " - 1` → -1**

```
" " → 0  
0 - 1 = -1
```

---

# 🧠 **8. Operator Precedence with Coercion**

JS evaluates left to right for `+`:

```
1 + 2 + "3"
→ 3 + "3"
→ "33"
```

But:

```
1 + "2" + 3
→ "12" + 3
→ "123"
```

---

# 🧩 **9. The Most Important Summary — Final Rules**

Here is the **everything-in-one-page** summary:

---

## ⭐ **Rule 1: Only `+` does string concatenation.**

If either operand is a string:

```
a + b → String(a) + String(b)
```

---

## ⭐ **Rule 2: All other arithmetic ops → force Number(a).**

```
a - b
a * b
a / b
a % b
```

All convert inputs to numbers.

---

## ⭐ **Rule 3: Coercion Priority**

When performing an operation, JS applies:

1. **Check operator**
2. If `+`, check if any operand → string
3. If not string → convert both to **number**
4. If operand is object/array → apply **ToPrimitive**:

   * `valueOf()`
   * then `toString()`

---

## ⭐ **Rule 4: Special conversions to memorize**

* `null` → **0**
* `true` → **1**
* `false` → **0**
* `""` → **0**
* `" "` → **0**
* `undefined` → **NaN**
* `[]` → **""** (string), **0** (number)
* `{}` → `"[object Object]"` (string), **NaN** (number)

---

# 💯 FINAL CHEAT SHEET (Print this mentally)

### **If operator is `+`:**

* If string involved → **string concat**
* Else → **number addition**

### **If operator is not `+`:**

* Convert everything to **number**

### **Converting to Number:**

* `"10"` → 10
* `""` → 0
* `" "` → 0
* `true` → 1
* `false` → 0
* `null` → 0
* `undefined` → NaN
* `[]` → 0
* `{}` → NaN

### **Converting to String:**

* `[]` → `""`
* `{}` → `"[object Object]"`

---
