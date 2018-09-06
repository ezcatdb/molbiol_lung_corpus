---
layout: entry
title: "Adverse effect"
category: "Effects by treatment"
shortdef: "Adverse effect by medical treatment (PHAEDRA)"
order: 6
---

This event is based on the <a href="http://www.nactem.ac.uk/PHAEDRA/">PHAEDRA corpus</a> at <a href="http://www.nactem.ac.uk/">NaCTeM</a>.

The following words can be triggers of this event:

- adverse effect
- side effect

~~~ ann
The common adverse effects of Icotinib were rash and diarrhea.
T1 Adverse_effect 4 26 common adverse effects
T2 Organic_compound_other 30 38 Icotinib
T3 Symptom 44 48 rash
T4 Symptom 53 61 diarrhea
E1 Adverse_effect:T1 has_agent:T2 affects:T3 affects2:T4
~~~

The following words also can be triggers of this event:

- induce
- cause
- lead to

~~~ ann
Chemotherapy-induced peripheral neuropathy.
T1 Medication 0 12 Chemotherapy
T2 Adverse_effect 13 20 induced
T3 Symptom 21 42 peripheral neuropathy
E1 Medication:T1
E2 Adverse_effect:T2 has_agent:E1 affects:T3
~~~
~~~ ann
We hypothesized that direct implantation might have led to metastasis.
T1 Speculation_cue 3 15 hypothesized
T2 Surgery 21 40 direct implantation
T3 Speculation_cue 41 46 might
T4 Adverse_effect 52 58 led to
T5 Disease 59 69 metastasis
E1 Surgery:T2 
E2 Adverse_effect:T4 has_agent:E1 affects:T5 cue:T3 cue2:T1 
A1 Speculated E2
~~~

Arguments:

The *has_agent* for this event must be [Organic_compound_other](), [Medical Treatment](), [Medication]() or [Surgery]().

The *has_subject* for this event must be [Subject]().

The *affects* for this event must be [Disease]() or [Symptom]().


Possible alternative annotation:

~~~ ann
The common adverse effects of Icotinib were rash and diarrhea.
T1 Adverse_effect 4 26 common adverse effects
T2 Organic_compound_other 30 38 Icotinib
T3 Symptom 44 48 rash
T4 Symptom 53 61 diarrhea
E1 Adverse_effect:T1 has_agent:T2 affects:T3 
E2 Adverse_effect:T1 has_agent:T2 affects:T4
~~~

<!---
The *Theme* for this reaction event must be other reaction events.
--->
