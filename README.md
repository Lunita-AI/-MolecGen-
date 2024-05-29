# *[MolecGen]:
This code performs several key functions in the context of using a kind of Artificial Intelligence named Generative Adversarial Network (GAN) for the possibility to generate "new" chemical polymer sequences.
---
<br>
⚗️ (> Please, consider that for this Machine Learning system "new" may mean "unseen" examples in its training data)!!!⚗️
<br>
<br>

Here's a summary of what each part of the code does:

- **Definition of the original dataset:** The "data" dataset contains a list of chemical polymer sequences. This represents the original data set that will be used to train the GAN.

- **Printing of the original dataset:** Prints the original dataset before any processing.

- **Data encoding:** The function in this step takes the polymer sequences and converts them into numerical representations using one-hot encoding. This involves converting each character in the sequences into a binary vector of length equal to the vocabulary size (total number of unique characters) with a "1" in the position corresponding to the character and "0" in all other positions. All hail Claude Shannon!

- **Definition of the GAN architecture:** It defines the neural network architectures of the generator and discriminator, as well as the structure of the entire GAN model.

- **GAN training:** The train_gan function trains the GAN using the one-hot encoded dataset. During training, the generator attempts to generate increasingly realistic polymer sequences, while the discriminator learns to distinguish between real and fake sequences.

- **Generation of new polymer sequences:** After training, the generator is used to generate new polymer sequences from random noise. These generated sequences are returned as a list of encoded sequences.

- **Decoding of the generated sequences:** The generated sequences are decoded back to the original text format from their one-hot representation. This involves reversing the one-hot encoding process and converting the binary vectors back into character sequences.

- **Printing of the generated sequences:** After the decoding, the generated polymer sequences are printed for display.

- **Graphics and illustrations:** Finally, one of the generated polymer sequences is displayed as a chemical graph and creativily transformed into an illustration for popular science communication.

- # GRAPHING THE RESULTS

In the last step knowledge of chemistry is required to carry out the SMILES (Simplified Molecular Input Line Entry Specification) encoding, by hand, of the results and represent the structure of each molecule using an ASCII character string.
<br> <br>First we are going to convert one of the results into a molecular structure that AI can "understand" and manipulate, then we are going to make a graph.

---

**Basic Components of SMILES:**
<br>**Atoms**
<br>They are represented using their chemical symbol (e.g., C for carbon, O for oxygen, N for nitrogen). Carbon atoms that do not have formal charges or explicit hydrogens can be omitted, and it is assumed that the bonds are single unless otherwise indicated.

**Bonds**
- Single: Not explicitly indicated (e.g., CC means a single bond between two carbons).
- Double: Represented with = (e.g., C=C).
-Triple: Represented with # (e.g., C#C).
- Aromatic: Atoms in an aromatic ring are indicated with lowercase letters (e.g., c1ccccc1 for benzene).
Rings
Atoms in rings are numbered. For example, C1CCCCC1 represents cyclohexane.

**Functional Groups**
<br>Common functional groups such as hydroxyl group (-OH), amino group (-NH2), carbonyl group (-C=O), etc., are represented using their respective symbols.

**Branches**
<br>Branching structures are indicated with parentheses. For example, CC(C)C for isobutane.

**Cycles**
<br>Cycles in molecules are described by indicating the atoms that form the cycle in sequence, followed by an additional closing number to indicate the end of the cycle.

**Charges and Stereochemistry**
- Charges: Charges are indicated with [C+] for a positive charge and [C-] for a negative charge.
- Stereochemistry: Stereochemistry is indicated with @ and @@ for chiral centers.

-------------------------->

**Hydrogens in SMILES:**
<br>**Implicit**<br>
Hydrogens are not explicitly represented in most cases. The software interpreting the SMILES string assumes that each atom has the correct number of hydrogens to fulfill its standard valence. For example:

- C represents a carbon atom with four bonds (if there are no other atoms explicitly bonded, it is assumed to have four hydrogens: CH₄).
- CC represents two carbon atoms bonded by a single bond, and it is assumed that the other bonds needed to complete the valence are filled with hydrogens: C-C (ethane, CH₃-CH₃).

<br>**Explicit**<br>
If you need to specify hydrogens explicitly, you can do so using [H] for an independent hydrogen atom, or by using a notation that includes the number of hydrogens as part of an atom in brackets.
<br>For example: Methane (CH₄):
- Implicit: C
- Explicit: [CH4]



---

# CREATIVE ILLUSTRATIONS:#

---
**⚠️ WARNING!!! ⚠️**
<br><br>In this step analytical precision is not sought so much, although it is an important aspect, but rather the aim is to achieve a suggestive graphic representation for popular scientific communication with an artistic touch.
<br><br>The process is complex and iterative, so the attached image is a sample of the many creative possibilities and may not necessarily correspond to the reality of the compound represented.

---
<br>
The following illustration is created with another external Generative Al system developed by Lunita.ai called TXT2IMG. This solution is a latent diffusion model applied to the production of intricate images based on prompting, although it also has versatility for tasks including inpainting, outpainting, and creating image-to-image translations influenced by textual cues.
<br><br>
A "prompt" in Al is a detailed textual instruction or description used to guide content creation, and the provided message has attempted to graphically describe the structure of the artificial chemical element achieved in the previous steps: "C₁₀H₈O₄".
<br><br>

In this case, the provided was prompt was:
"*Design a kawaii style superhero whose body structure is inspired by a complex artificial compound. This character has a backbone composed of ten interconnected black orbs, giving them a sleek and robotic appearance. It has four powerful and flexible arms, each arm capable of holding clusters of spheres. These arms can manipulate eight white orbs that form single bonds and four red orbs that form double bonds, which they use to create and control various forms of energy and matter. The black, white and red spheres should be visually integrated into the character's body and powers, reflecting his ability to manipulate atomic structures. Create a visually striking and cute design that emphasizes its unique abilities and futuristic aesthetic.*"
<br><br>
*(Note: the graphic obtained with the SMILES representation in the step before has also been used as a visual prompt during the design of the illustration).


