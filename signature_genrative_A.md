base
```
Given:
- g = h^((p-1)/q) mod p (where h is a generator of the multiplicative group modulo p),
- g^q ≡ 1 mod p by Fermat's little theorem, indicating g has order q,
- s = k^(-1)(H(m) + xr) mod q,
- r = (g^k mod p) mod q.

Proof of correctness:

1. Compute k:
   k ≡ H(m)s^(-1) + xr s^(-1) ≡ H(m)w + xrw mod q,
   where w = s^(-1) mod q.

2. Calculate g^k mod p:
   g^k ≡ g^(H(m)w) * g^(xrw) ≡ g^(H(m)w) * g^(xrw) ≡ g^(H(m)w) * y^(rw) ≡ g^(u_1) * y^(u_2) mod p,
   where y = g^x mod p, u_1 = H(m)w, and u_2 = rw.

3. Compute r:
   r = (g^k mod p) mod q = (g^(u_1) * y^(u_2) mod p) mod q = v,
   where v is the result of (g^(u_1) * y^(u_2) mod p) mod q.
```

![Uploading image.png…]()
