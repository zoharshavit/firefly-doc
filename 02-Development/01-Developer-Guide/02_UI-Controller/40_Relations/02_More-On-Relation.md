﻿In this article We'll:
* Explain that `RelationType.Find` is the default, so no need to specify it
* Show how to use Sort in the context of a Relation
* Show how you can set more properties to a relation, or Query information about a relation using `Relations[Shippers]` syntax. 


### Example

```csdiff
public ShowOrders()
{
...
   Relations.Add(Shippers, RelationType.Find, Shippers.ShipperID.IsEqualTo(Orders.ShipVia));
+  Relations[Shippers].Where.Add(Shippers.CompanyName.IsDifferentFrom(""));
}
```

---
<iframe width="560" height="315" src="https://www.youtube.com/embed/9ifSzrZNh4U?list=PL1DEQjXG2xnKwhPzEwuvVkEL7a_D9-pkL" frameborder="0" allowfullscreen></iframe>

---

