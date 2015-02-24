% title: Specific Aims
% subtitle: Admission to candidacy exam (ACE)
% author: Bas Rustenburg
% date: February 25th 2015
% thankyou: Fin...

---

title: Aims

## The binding of charged ligands

  * Host-guest model systems  
  * Corrections to free energy calculations  
  * Bayesian approach to calorimetry experiments

## Protonation state effects on binding

  * Small molecule pKa predictions  
  * Protein pKa predictions with MCCE  
  * Fluorescence and ITC experiments on kinase domains  

## Weak association and multiple binding
  * Human serum albumin as a model system  
  * Free energy calculations with semigrand canonical ensemble formalism  
  * Bayesian selection of theoretical binding models from experimental data

---

title: Aim 1
subtitle: The binding of charged ligands
class: img-top-center

<img src="images/charged.svg" alt="Drawing" style="width: 78%;"/>

---
title: Aim 1
subtitle: The binding of charged ligands
topic: Corrections to free energy calculations

A number of different corrections have been suggested.

#### Mathemathical corrections

  * <b>Rocklin et al.</b>
  J. Chem. Phys. 139, 184103 (2013);
  http://dx.doi.org/10.1063/1.4826261

  * <b>Reif and Oostenbrink</b>
  Journal of Computational Chemistry 2014, 35, 227–243
  http://dx.doi.org/10.1002/jcc.23490

#### Creating/destroying salt pairs
  * Are corrections necessary?

---

title: Aim 1
subtitle: The binding of charged ligands
topic: Host-Guest systems as model systems

provide a way to study binding interactions without the issues like:

<table>
    <td>
        <ul>
            <li> Expressing and purifying a protein</li>
            <li> Obtaining high concentration necessary for ITC experiments </li>
            <li> Timescale needed for molecular dynamics</li>
        </ul>
    </td>
    <td>

    <script type="text/javascript">
            jmolApplet1 = Jmol.getApplet("jmolApplet1", Info);
            Jmol.script(jmolApplet1,"background white; load molecules/cb7.sdf; spin on;")
    </script>

    </td>
</table>

Cucurbit-[7]-uril, a host molecule that binds cationic guests.

---
title: Aim 1
subtitle: The binding of charged ligands
topic: Bayesian isothermal titration calorimetry (ITC)
class: img-top-center

<img src="images/bayes_theorem.svg" alt="Drawing" style="width: 80%;"/>
---
title: Aim 1
subtitle: The binding of charged ligands
topic: Bayesian isothermal titration calorimetry (ITC)
class: img-top-center


<img src="images/bayes_theorem.svg" alt="Drawing" style="width: 80%;"/>
We attempt to obtain the enthalpy, mechanical heat of injection, heat of dilution, association constant, and the true concentrations.
<img src="images/theta_D.svg" alt="Drawing" style="width: 75%"/>
Our observables are the heats as measured by the calorimeter.

---

title: Aim 2
subtitle: Protonation state effects on binding
class: img-top-center

<img src="images/imatinib_pKa.png" alt="Drawing" style="width: 80%;"/>

---
title: Aim 2
subtitle: Protonation state effects on binding
topic: Why is it important to consider protonation states?

  * Proteins and small molecules can sample mixtures of different protonation states.

  * These states all contribute to the binding affinity, possibly contributing several kcal / mol.

#### Why is it a problem?

  * We do not know in which proteins this occurs, and in which it does not!
  
  * We want to identify systems where this occurs, and the effect on the binding affinity that supposedly comes from this.

  * Computationally, often only one state is simulated.
---

title: Aim 2
subtitle: How can we take the pKa into account?
topic: Computationally survey

<ul>

<h4>Small molecules</h4>
<li>Using tools such as schrodingers Epik, Jaguar</li>

<h4>Proteins</h4>
<li>Tools such as PROPKA</li>
<li>MCCE2 (Gunner et al.)</li>

<h4>And then perform free energy calculations</h4>

<li>Constant-pH simulations using the obtained pKa data</li>
</ul>

---
title: Aim 2
subtitle: How can we take the pKa into account?
topic: Experimentally

#### Measure binding affinity using

* Fluorescence assays for kinase domains

* Isothermal titration calorimetry experiments

And then we compare to the simulated data.


<script type="text/javascript">
    var Info = {
        color: "#E8F4FF",
        height: 300,
        width: 500,
        jarFile: "scripts/jsmol/java/JmolApplet.jar",
        isSigned: false,
        jarPath: "scripts/jsmol/java",
        j2sPath: "scripts/jsmol/j2s",
        serverURL: "http:/localhost:8000/scripts/jsmol/php/jsmol.php",
        use: "HTML5"
    };
</script>
<script type="text/javascript">
            jmolApplet1 = Jmol.getApplet("jmolApplet1", Info);
            Jmol.script(jmolApplet1,"background white; load molecules/2HYY.pdb; hide not *:A; center *:A; select *:A; cartoon only; color cartoon group; select ligand; wireframe 0.5; spacefill 23%; select all;")
</script>

<footer class="source"> Imatinib bound to c-abl (pdb: 2HYY) </footer>


---
title: Aim 3
subtitle: Weak association and multiple binding
class: img-top-center

<script type="text/javascript">
    var Info = {
        color: "#E8F4FF",
        height: 600,
        width: 1200,
        jarFile: "scripts/jsmol/java/JmolApplet.jar",
        isSigned: false,
        jarPath: "scripts/jsmol/java",
        j2sPath: "scripts/jsmol/j2s",
        serverURL: "http:/localhost:8000/scripts/jsmol/php/jsmol.php",
        use: "HTML5"
    };
</script>
<script type="text/javascript">
            jmolApplet2 = Jmol.getApplet("jmolApplet2", Info);
            Jmol.script(jmolApplet2,"background white; load molecules/2BXM.pdb; hide not *:A; center *:A; select *:A; cartoon only; color cartoon group; select ligand; wireframe 0.5; spacefill 23%; select all;")
</script>
<footer class="source"> Indomethacin bound to HSA (pdb: 2BXM) </footer>

---

title: Aim 3
subtitle: Weak association and multiple binding
topic: Bayesian modelling of ITC
class: img-top-center

We can describe binding of multiple ligands

##### The heats of binding as a function of concentration
<img src="images/heats.svg" alt="Drawing" style="width: 58%;"/>

##### The posterior
<img src="images/mb_posterior.svg" alt="Drawing" style="width: 58%;"/>

---

title: Aim 3
subtitle: Weak association and multiple binding
topic: Semigrand canonical simulations

* We allow the concentration of ligand(s) to fluctuate

* Measures of affinity and cooperativity can be obtained

* Allows for fragment based free energy calculation approaches

---

title: Aim 3
subtitle: Weak association and multiple binding
topic: Simulation of ITC data

* Using the data obtained from free energy calculations, we can predict and experimental titration curve. 

* We can use this curve to enhance our experimental design

* And ultimately, we can validate the predictions from simulation by performing the ITC experiments

