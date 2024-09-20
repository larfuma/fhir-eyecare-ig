# Requirements

## Disclaimer

This is an experimental Fork of the fhir-eyecare-IG developed by the Eyes on FHIR project group (publiched under CC0 license). 

I am a trainee ophthalmologist based in germany with limited FHIR/Gíthub experience, and I am using this fork to get aquainted with both and to  explore ways in which the development of this IG can be expanded in the future. 

I will use this Readme to describe my experimental changes, in order to be transparent to people with or without FHIR/Git experience.
Please feel free to contact me for feedback or if you would like try and work on improving ophthalmic interoperability with me! 


# Work in the Visual Acuity Observation profile


To specify the values it should communicate I have copied the slicing method from the [Australian ADHA Visual Acuity Observation Profile](https://build.fhir.org/ig/AuDigitalHealth/ci-fhir-r4/StructureDefinition-dh-observation-visualacuity-1.html), Credit to the Authors!

Ophthalmologists in germany currently document >90% of their Visual acuity measurements as strings. Their EMRs are usually not certified to convert this data into numerical or ratio values I felt i sadly had to introduce some capability for the profile to handle string values as well, although this is unneccessary and damaging to interoperability. I have made an effort to to demonstrate that this is not encouraged with a warning, and it may be reasonable to remove this capability in healthcare services which are not overly reliant on string-formatted VA data. 









-------------------
Readme from the origina IG: 



## GitHub
The IG source code is stored in GitHub so you'll need to be a Github user and have GIT installed and available from a terminal or shell.  If you intend to contribute content to the project you'll need write permission so please contact us at woliver@oculo.com.au or brett.esler@oridashi.com.au

## IG Publishing Tool
In order to build the IG you'll need to install the Java publishing tool. Instructions for doing this can be found [here](https://wiki.hl7.org/FHIR_IG_Publishing_tool).  OpenJDK seems to work fine.


# Making changes
Every commit to the master branch within Github will trigger a build process.  The resulting IG will be published to [http://build.fhir.org/ig/HL7/fhir-eyecare-ig/branches/master/index.html].  If you're planning on making changes to the repo please create a branch make your changes and verify that you can build (using the Java tool) locally before merging into master.  The build tool has a QA function which will check for errors in the generation process.  We should be working towards 0 errors.

The status of the build can be found here [https://fhir.github.io/auto-ig-builder/builds.html]. You'll also find references to a number of other projects which can be used as examples.

# Knowledge base
* [US Core example](https://github.com/HL7/US-Core/tree/master)
* [AU Base IG](https://github.com/hl7au/au-fhir-base/tree/master  )
* [Example AU IG for child health](https://confluence.hl7australia.com/display/AFR/Conversation+on+IG+building)
