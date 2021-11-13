import pyopenms
from pyopenms import *
seq = AASequence.fromString("DFPIANGER")
prefix = seq.getPrefix(4)
suffix = seq.getSuffix(5)
concat = seq + seq


print("Sequence:", seq)
print("Prefix:", prefix)
print("Suffix:", suffix)
print("Concatenated:", concat)


mfull = seq.getMonoWeight()
mprecursor = seq.getMonoWeight(Residue.ResidueType.Full, 2)


mz = seq.getMonoWeight(Residue.ResidueType.Full, 2) / 2.0 

mz = seq.getMZ(2) 

print()
print("Monoisotopic mass of peptide [M] is", mfull)
print("Monoisotopic mass of peptide precursor [M+2H]2+ is", mprecursor)
print("Monoisotopic m/z of [M+2H]2+ is", mz)