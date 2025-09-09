# EX-NO-10-Diffie-Hellman-Key-Exchange-Algorithm

## AIM:
To Implement Diffie Hellman Key Exchange Algorithm 

## Algorithm:

1. Diffie-Hellman Key Exchange is used for securely sharing a secret key between two parties over an insecure channel.

2. Initialization: Agree on a large prime number \( p \) and a primitive root \( g \) modulo \( p \) (both are public values).

3. Key Exchange Process: 
   - Each party selects a private key and calculates their public key using the formula \( g^{\text{private key}} \mod p \).
   - Each party then shares their public key with the other.

4. Secret Key Computation: 
   - Each party computes the shared secret key using the received public key and their own private key.

5. Security: The difficulty of computing discrete logarithms ensures that the shared key remains secure even if public values are intercepted.

## Program:

```


# Step 1: Public values (p and g)
p = int(input("Enter a prime number (p): "))
g = int(input("Enter a primitive root modulo p (g): "))

# Step 2: Private keys
a = int(input("Enter Alice's private key (a): "))
b = int(input("Enter Bob's private key (b): "))

# Step 3: Compute public values
A = pow(g, a, p)  # Alice's public value
B = pow(g, b, p)  # Bob's public value

# Step 4: Each computes the shared secret
secret_alice = pow(B, a, p)
secret_bob = pow(A, b, p)

# Step 5: Show results
print("\n--- Diffie–Hellman Key Exchange ---")
print("Public prime (p):", p)
print("Primitive root (g):", g)
print("Alice's Public Value (A):", A)
print("Bob's Public Value (B):", B)
print("Shared Secret (Alice):", secret_alice)
print("Shared Secret (Bob):", secret_bob)

```

## Output:

<img width="344" height="216" alt="image" src="https://github.com/user-attachments/assets/27d42869-1022-49ab-8f7e-f2a1f704a42d" />


## Result:
  The program is executed successfully.

