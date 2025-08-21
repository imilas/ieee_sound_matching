
## Reviewer 1

1. **Organization**
   - Overlap between *Introduction*, *Background*, and *Past Works*.  
   - **To do**: merge into a single *Background and Related Work* section.
   
1. **More on Introduction**
   - Central research question not clearly articulated early.  
   - Core problem not obvious (“no single loss is optimal across synthesizers”)
   - Subsection structure inconsistent 

3. **Methods/Results Section**
   - Section IV (“Programs, Methodology, and Results”) overloaded.  
   - **To do**: split into (1) Experimental Setup, (2) Results, (3) Discussion).

4. **Novelty & Theory**
   - DTW_Envelope and SIMSE_Spec not framed with sufficient theoretical justification.  
   - Limited interpretability analysis (e.g., why DTW works well on modulated noise, why SIMSE beats L1 in some cases).
   - **To do:** Provide loss function landscape and gradient graphs to explain why what works with what

4. **Limitations**
   - Synthesizers too simple (2–3 parameters).  
   - All experiments in-domain → generalizability limited.
   - To do: Justify value of small experiments

6. **Practical Implications**
   - Paper rejects “universal loss” but offers no actionable heuristics.  
   - Suggestion: give practical guidance (e.g., DTW for AM, SIMSE for subtractive).

7. **Hypotheses**
   - Additional hypotheses only implicit.  
   - Need to clearly state them upfront (e.g., metric agreement, loss novelty, iterative optimization viability).

---

## Reviewer 2 

1. **Novelty & Related Work**
   - Similarity to prior works not acknowledged:  
     - Barkan et al. (2023), *Inversynth II*.  
     - Cherep et al. (2024), *Creative Text-to-Audio Generation*.  
   - Differentiable iterative sound-matching not as unexplored as claimed.  

2. **Clarity of Proposed Method**
   - Not clear what the proposed method really is.  
   - Paper reads mostly as an evaluation readout, not a novel methodology.

3. **Takeaways**
   - Results inconclusive: not clear how to select loss/synth pairings.  
   - Needs clearer, reusable insights and takeaways.

---

## Reviewer 4 

1. **Notation & Symbols**
   - Using `t` for target is confusing (usually denotes time).  
   - Suggestion: use `x_θ` (output) and `x₀` (target).  

2. **Notation Placement**
   - Symbol explanations come too late (after first equation).  
   - Suggestion: move earlier.

3. **Clarification of Hypothesis**
   - “No correct version of an 8-bit snare” → confusing.  
   - Needs clarification (imitation vs replication).

4. **Terminology**
   - “Out-of-domain” called “unexplored,” but cited works exist.  
   - Suggestion: say “underexplored.”

5. **Synthesizers**
   - Mentioned late (p.8), should be described earlier in Section IV.  

6. **Listening Tests**
   - Only conducted by authors → potential bias.  
   - Suggestion: add independent listener if possible, or clarify limitation.

7. **Redundancy**
   - Likert scale description repeated twice.  

8. **Spectrogram Loss**
   - Clarify that STFT losses fail under time-shift unless aligned (e.g., DTW).  

9. **Grammar**
   - In “While cannot prove…,” missing subject (“we”).  

10. **Convergence**
    - Algorithm always runs 200 steps.  
    - Concern: could overfit; optimal step might be earlier.  
    - Suggestion: discuss whether final step is always best.
