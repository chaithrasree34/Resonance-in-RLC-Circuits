# Resonance-in-RLC-Circuits
# Resonance in RLC Series Circuit

import math

print("====================================")
print("   RLC CIRCUIT RESONANCE CALCULATOR")
print("====================================")

R = float(input("Enter resistance R (Ohms): "))
L = float(input("Enter inductance L (Henrys): "))
C = float(input("Enter capacitance C (Farads): "))

# Resonant frequency
fr = 1 / (2 * math.pi * math.sqrt(L * C))

# Angular resonant frequency
wr = 2 * math.pi * fr

# Quality factor
Q = wr * L / R

# Bandwidth
BW = R / (2 * math.pi * L)

print("\n--- Results ---")
print("Resonant Frequency =", round(fr, 2), "Hz")
print("Angular Frequency =", round(wr, 2), "rad/s")
print("Quality Factor =", round(Q, 2))
print("Bandwidth =", round(BW, 2), "Hz")