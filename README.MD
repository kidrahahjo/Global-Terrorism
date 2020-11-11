# Analysis of Global Terrorism Database
> Copyright University of Maryland 2018.
> National Consortium for the Study of Terrorism and Responses to Terrorism (START), University of Maryland. (2018). The Global Terrorism Database (GTD) [Data file]. Retrieved from https://www.start.umd.edu/gtd

## Context
Information on more than 180,000 Terrorist Attacks

The [Global Terrorism Database](https://www.kaggle.com/START-UMD/gtd) (GTD) is an open-source database including information on terrorist attacks around the world from 1970 through 2017. The GTD includes systematic data on domestic as well as international terrorist incidents that have occurred during this time period and now includes more than 180,000 attacks. The database is maintained by researchers at the National Consortium for the Study of Terrorism and Responses to Terrorism (START), headquartered at the University of Maryland.

## Metadata
- Geography: Worldwide
- Time period: 1970-2017, except 1993
- Unit of analysis: Attack
- Variables: >100 variables on location, tactics, perpetrators, targets, and outcomes

See the [GTD Codebook](https://start.umd.edu/gtd/downloads/Codebook.pdf) for important details on data collection methodology, definitions, and coding schema.

## Uploaded Data Sources
1. Population density of [India](https://www.macrotrends.net/countries/IND/india/population-density#:~:text=The%20population%20density%20of%20India,a%201.04%25%20increase%20from%202017.)
2. Population density of [USA](https://www.macrotrends.net/countries/USA/united-states/population-density#:~:text=The%20population%20density%20of%20U.S.,a%200.64%25%20increase%20from%202016.)

## Hypothesis
### Equal number of successful `Criterion 1` terror attacks happen in India and United States.
1. [Link to analysis](https://github.com/kidrahahjo/Global-Terrorism/blob/master/Analysis/Hypothesis%201.ipynb)
2. Rejected the null hypothesis
3. Tests conducted: ANOVA, Student's t-test (two-tailed)
4. Level of significance (α) = 0.05
5. ANOVA: F<sub>critical</sub> = 3.957, F<sub>obtained</sub> = 11.75, P = 0.0009
6. t-test (two-tailed): Degrees of Freedom = 82, |t<sub>obtained</sub>| = 16.749, P ≈ 0

## Short Descriptions
Please note that all the descriptions are copied from the [GTD Codebook](https://start.umd.edu/gtd/downloads/Codebook.pdf).

### eventid - Numeric
A unique id where first 8 numbers are date recorded “yyyymmdd” and next 4 numbers are sequential case number for the given day.
### iyear - Numeric
The year in which the incident occurred.
### imonth - Numeric
The number of the month in which the incident occurred.
### iday - Numeric
The numeric day of the month on which the incident occurred.
### approxdate - Text
Whenever the exact date of the incident is not known or remains unclear, this field is used to record the approximate date of the incident.
### extended - Numeric
Wheter the duration of an incident extended more than 24 hours or not.
If yes then 1, else 0.
### resolution - Text
Date of Extended Incident Resolution.
This field only applies if “Extended Incident?” is “Yes” and records the date in which the
incident was resolved(hostages released by perpetrators; hostages killed; successful
rescue, etc.).
Eg. '12/24/1982'
### country - Numeric
Country Code
### country_txt
Country Name
### region
Region Code
### region_txt
Region Name
### provstate - Text
This variable records the name (at the time of event) of the 1st order subnational administrative region in which the event occurs.
### city - Text
This field contains the name of the city, village, or town in which the incident occurred.
### latitude - Numeric
Latitude of the place of incident
### longitude - Numeric
Longitude of the place of incident
### specificity - Categorical
This field identifies the geospatial resolution of the latitude and longitude fields.
### vicinity - Numeric
States whether the incident occurred in the immediate vicinity of the city in question (1) or inside the city itself (0).
### location - Text
This field is used to specify additional information about the location of the incident.
### summary - Text
A brief narrative summary of the incident, noting the "when, where, who, what, how, and why."
### crit1 - Numeric
The violent act must be aimed at attaining a political, economic, religious, or social goal.
This criterion is not satisfied in those cases where the perpetrator(s) acted out of a pure profit motive or from an idiosyncratic personal motive unconnected with broader societal change.
### crit2 - Numeric
To satisfy this criterion there must be evidence of an intention to coerce, intimidate, or convey some other message to a larger audience (or audiences) than the immediate victims.
### crit3 - Numeric
The action is outside the context of legitimate warfare activities, insofar as it targets non-combatants.
### doubtterr - Numeric
In certain cases there may be some uncertainty whether an incident meets all of the
criteria for inclusion. In these ambiguous cases, where there is a strong possibility, but
not certainty, that an incident represents an act of terrorism, the incident is included in
GTD and is coded as “Yes” for this variable.
### alternative
This variable applies to only those cases coded as “Yes” for “Doubt Terrorism Proper?” (above).
This variable identifies the most likely categorization of the incident other than terrorism.
### alternative_txt
Description of above feature
### multiple
In those cases where several attacks are connected, but where the various actions do not constitute a single incident, then "Yes" is selected to denote that the particular attack was part of a "multiple" incident.
### success
Success of a terrorist strike is defined according to the tangible effects of the attack.
Success is not judged in terms of the larger goals of the perpetrators.
For example, a bomb that exploded in a building would be counted as a success even if it did not succeed in bringing the building down or inducing government repression.
### suicide
This variable is coded “Yes” in those cases where there is evidence that the perpetrator did not intend to escape from the attack alive.
### attacktype1 - Categorical
This field captures the general method of attack and often reflects the broad class of tactics used.
### attacktype1_txt
Description of above
### attacktype2
This variable utilizes the hierarchy and attack type definitions listed above.
## attacktype2_txt
Description of above
### attacktype3
This variable utilizes the hierarchy and attack type definitions listed above.
### attacktype3_txt
Description of above
### targtype1
The target/victim type field captures the general type of target/victim.
### targtype1_txt
Description of above
### targsubtype1
The target subtype variable captures the more specific target category and provides the next level of designation for each target type.
If a target subtype is not applicable this variable is left blank.
### targsubtype1_txt
Description of above
### corp1
This is the name of the corporate entity or government agency that was targeted.
### target1 - Text
This is the specific person, building, installation, etc., that was targeted and/or victimized and is a part of the entity named above.
### natlty1
This is the nationality of the target that was attacked, and is not necessarily the same as the country in which the incident occurred, although in most cases it is.
### natlty1_txt
Description of above
### targtype2
Conventions follow “Target/Victim Subtype” field.
### targtype2_txt
Description of above
### targsubtype2
Conventions follow “Target/Victim Subtype” field.
### targsubtype2_txt
Description of above
### corp2
Conventions follow “Name of Entity” field.
### target2
Conventions follow “Specific Target/Victim” field.
### natlty2
Conventions follow “Nationality of Target” field.
### natlty2_txt
Description
### targtype3
Conventions follow “Target/Victim Subtype” field.
### targtype3_txt
Description
### targsubtype3
Conventions follow “Target/Victim Subtype” field.
### targsubtype3_txt
Description
### corp3
Conventions follow “Name of Entity” field.
### target3
Conventions follow “Specific Target/Victim” field.
### natlty3
Conventions follow “Nationality of Target/Victim” field.
### natlty3_txt
Description
### gname
This field contains the name of the group that carried out the attack.
### gsubname
This field contains any additional qualifiers or details about the name of the group that carried out the attack.
This includes but is not limited to the name of the specific faction when available.
### gname2
This field is used to record the name of the second perpetrator when responsibility for the attack is attributed to more than one perpetrator.
### gsubname2
This field is used to record additional qualifiers or details about the second perpetrator group name when responsibility for the attack is attributed to more than one perpetrator.
### gname3
This field is used to record the name of the third perpetrator when responsibility for the attack is attributed to more than two perpetrators.
### gsubname3
This field is used to record additional qualifiers of details about the third perpetrator group name when responsibility for the attack is attributed to more than two perpetrators.
### motive
When reports explicitly mention a specific motive for the attack, this motive is recorded in the “Motive” field.
This field may also include general information about the political, social, or economic climate at the time of the attack if considered relevant to the motivation underlying the incident.
### guncertain1
First Perpetrator Group Suspected/Unconfirmed?
This variable indicates whether or not the information reported by sources about the Perpetrator Group Name(s) is based on speculation or dubious claims of
responsibility.
### guncertain2
Second Perpetrator Group Suspected/Unconfirmed?
### guncertain3
Third Perpetrator Group Suspected/Unconfirmed?
### individual
This variable indicates whether or not the attack was carried out by an individual or several individuals not known to be affiliated with a group or organization.
### nperps
This field indicates the total number of terrorists participating in the incident.
### nperpcap
This field records the number of perpetrators taken into custody. “-99” or “Unknown” appears when there is evidence of captured, but the number is not reported.
### claimed
This field is used to indicate whether a group or person(s) claimed responsibility for the attack.
### claimmode
This records one of 10 modes used by claimants to claim responsibility and might be useful to verify authenticity, track trends in behavior, etc.
### claimmode_txt
Description
### claim2
Second Group Claim of Responsibility?
### claimmode2
Mode for Second Group Claim of Responsibility
### claimmode2_txt
Description
### claim3
Third Group Claim of Responsibility?
### claimmode3
Mode for Second Group Claim of Responsibility
### claimmode3_txt
Description
### compclaim
This field is used to indicate whether more than one group claimed separate responsibility for the attack.
### weaptype1
Up to four weapon types are recorded for each incident. This field records the general type of weapon used in the incident.
### weaptype1_txt
Description
### weapsubtype1
This field records a more specific value for most of the Weapon Types identified immediately above.
### weapsubtype1_txt
Description
### weaptype2
Second Weapon Type
### weaptype2_txt
Description
### weapsubtype2
Second Weapon Sub-Type
### weapsubtype2_txt
Description
### weaptype3
Third Weapon Type
### weaptype3_txt
Description
### weapsubtype3
Third Weapon Sub-Type
### weapsubtype3_txt
Description
### weaptype4
Fourth Weapon Type
### weaptype4_txt
Description
### weapsubtype4
Fourth Weapon Sub-Type
### weapsubtype4_txt
Description
### weapdetail
This field notes any pertinent information on the type of weapon(s) used in the incident.
Such notes could include the novel use or means of concealing a weapon, specific weapon models, interesting details of the weapons’ origins, etc.
### nkill
This field stores the number of total confirmed fatalities for the incident.
The number includes all victims and attackers who died as a direct result of the incident.
### nkillus
This field records the number of U.S. citizens who died as a result of the incident, and follows the conventions of “Total Number of Fatalities” described above.
### nkillter
Limited to only perpetrator fatalities, this field follows the conventions of the “Total Number of Fatalities” field described above.
### nwound
Total Number of Injured.
### nwoundus
Total Number of U.S. citizens injured.
### nwoundte
Total Number of Perpetrators Injured.
### property
“Yes” appears if there is evidence of property damage from the incident.
### propextent
Extent of Property Damage.
### propextent_txt
Description
### propvalue
Value of Property Damage (in USD).
### propcomment
If “Property Damage?” is “Yes,” then non-monetary or imprecise measures of damage may be described in this field.
This field is also used to list specific details about the property that was damaged in an attack, such as the type of vehicle that was destroyed, the areas or parts of a building that were damaged, or the types of assets that were stolen.
### ishostkid
This field records whether or not the victims were taken hostage (i.e. held against their will) or kidnapped (i.e. held against their will and taken to another location) during an incident.
### nhostkid
Total Number of Hostages/ Kidnapping Victims.
### nhostkidus
Total Number of U.S. Hostages/ Kidnapping Victims.
### nhours
Hours of Kidnapping / Hostage Incident.
### ndays
Days of Kidnapping / Hostage Incident
### divert
If the “Attack Type” is “Hostage Taking (Kidnapping)” or “Hijacking” then this field will list the country that hijackers diverted a vehicle to, or the country that the kidnap victims were moved to and held.
## kidhijcountry
If the “Attack Type” is “Hostage Taking (Kidnapping)” or “Hijacking” then this field lists the country in which the incident was resolved or ended.
### ransom
Ransom Demanded
### ransomamt
Amount of ransom demanded
### ransomamtus
Ransom Amount Demanded from U.S. Sources.
### ransompaid
Total Ransom Amount Paid
### ransompaidus
Ransom Amount Paid By U.S. Sources.
### ransomnote
This field is used to record any specific details relating to a ransom that are not captured in the other fields.
### hostkidoutcome
Kidnapping/Hostage Outcome
### hostkidoutcome_txt
Description
### nreleased
Number Released/Escaped/Rescued
### addnotes
This field is used to capture additional relevant details about the attack.
### scite1
This field cites the first source that was used to compile information on the specific incident.
### scite2
Second Source Citation.
### scite3
Third Source Citation
### dbsource
This field identifies the original data collection effort in which each event was recorded.
### INT_LOG
This variable is based on a comparison between the nationality of the perpetrator group and the location of the attack.
It indicates whether a perpetrator group crossed a border to carry out an attack.
### INT_IDEO
It indicates whether a perpetrator group attacked a target of a different nationality.
### INT_MISC
It indicates whether a perpetrator group attacked a target of a different nationality.
### INT_ANY
Any of the above 3
### related
When an attack is part of a coordinated, multi-part incident the GTD IDs of the related incidents are listed here, separated by commas.