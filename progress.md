# Research progress


## 2024
### July 24 - 31

* Plan for next week
  * Task 1: x
  * Task 2: x


## 2024
### July 17 - 24

* What is new: 
  * New math: Derived RAD form for pfpJ - > pfpJ
  * New code: Almost done with the resolvent vector optimization. 

* What is the roadblock:

* Plan for next week
  * Task 1: Finish derivation of resolvent vector adjoint (Rbar).
  * Task 2: Aeroelastic simulation different $\alpha,\omega$.
  * Task 3: Rewrite Diff SVD paper. Bring copies to edit.
  * Task 4: Rewrite resolvent paper added content as per discussion.
  * Task 5: Rewrite code as per repo guidelines

## 2024
### July 24 - 31
*** What is new**:
  * Attended workshop on July 25. (DAFOAM). Workshop had lots of researchers from different univs.
  * DA-FOAM session: Key take aways:
    * A common topic of application was ML-"Field Inversion" application to turbulence modeling and prediction accuracy.
    * Many used BFS and NASA-Hump cases to validate predictions
    * What was interesting is in the second talk of generalizable data driven turbulence modeling (SST level), the data set they trained on was actually pretty  small. Yet, they got a good prediction and their alebraic model which modifies the SST model gave better predictions in separation point in the flows.
    * Most used DA FOAM for aerodynamic shape optimization. In fact, there was one speaker from MDO LAB Michigan
    * Field inversion based ML is now incorporated into the DA FOAM package
    * There are some issues in the compressible flow (supersonic regime and shockwave capture issues)
    * Looks like our class of problems are picking up pace very quickly and we have a great topic to work on
* **New math**: Resolvent analysis had some issues in the RAD formulae. Will discuss in meeting. These issues were fixed.
* **New code**: Resolvent opt code was changed because of the RAD formula change. Opt code is complete and can now hande any objective function of interest.
* **Roadblocks so far**: VS was unable to compile anything when invoking the standar libraries used in MDO-latex repos. Need to see why that is happening.
* Need time till Friday to complete SVD paper write up (modified write up)
* Issue with JAX/FD for the pfpu and pfpx step. Skipped this verification step as algorithm is working anyways. This step cannot be verified eitherways as mathematically, pfpx is different from dfdx. FD/CS/JAX will inevitably give us dfdu or dfdx, not pfpu and pfpx. RAD form did not work, maybe I made a mistake in understanding there.
* Resolvent plot for \alpha and \omega: Laptop kept going out of memory for some reason. Will use the library PC for this today (07/31)

*Plan for week:
 * Finish vector optimization and then plot the optimization result. **(Add how much was done)**
 * Try to finish the simulation and get \alpha, \omega plot.
 * Push SVD paper final edits to repo.
 * To incorporate the JAX inside RAD step for resolvent.

## 2024
### July 31 - Aug 07
*** What is new**:
 * Added new maths to resolvent code. Saw an issue with going from complex -> real. Will push the new math to repo.
 * Finished the vector OPT. Working perfectly now. Only plot is pending.
 * Fixed VS issues. I am now able to pull/push to repos and also successfully compile any latex document.
*** Still pending / Roadblocks:
   * Issues with simulation. Code keeps crashing when trying to run simulation. Found a work around and need to compute resolvent.
   * SVD paper editing started on Sunday due to VS issues. All data has been transferred to local PC inside VS now.
   * SVD paper reference.bib file was corrupted for some reason, had to manually fix every citation in 56 citations. Need some more time till Friday.

**Plan for next week:**

 * Resolvent multi minima plot (x1,x2, iso f lines)
 * Latex files for SVD and Resolvent to be pushed asap (Fri)
 * Re run opt to get less than 1e-16 at least in objective error
 * Simulation try to use ISAAC and generate \omega + \alpha plots
 * Get LCO curves for unstedy sims
 * Generate three plots : LCO plot, resolvent +bifurcation diag
### Aug 10 - Aug 14
 * Next week see if we can setup pc in office space.
