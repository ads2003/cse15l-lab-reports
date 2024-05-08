# Lab Report 3 - Bugs and Commands


## *Part 1(Bugs)*

Inputs that induce failiure

```
import static org.junit.Assert.assertArrayEquals;

public class TestReverseInPlace {
    @org.junit.Test
    public void testReverseInPlace() {
        int[] input1 = {3, 4, 5};
        ArrayExamples.reverseInPlace(input1);
        assertArrayEquals(new int[]{5, 4, 3}, input1);
    }
}
```
Inputs that does not cause failure

```
import static org.junit.Assert.assertArrayEquals;

public class TestReverseInPlace {
    @org.junit.Test
    public void testReverseInPlace() {
        int[] input1 = {3};
        ArrayExamples.reverseInPlace(input1);
        assertArrayEquals(new int[]{3}, input1);
    }
}
```

## *Symptoms*


<img width="556" alt="Screenshot 2024-05-08 at 3 06 35 PM" src="https://github.com/ads2003/cse15l-lab-reports/assets/156348741/7664e73c-58cb-4940-9182-e569f5c6b82e">


*Before fixing bug*

```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```


*After fixing bug*

```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length/2; i += 1) {
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length - i - 1] = temp;
    }
  }
```


## *Part 2(Researching commands)*



### *grep -n*
use: It helps us locate the exact lines that have the same phrases. You can save a ton of time by doing this.
Function: It's used to give the line number for each matching word.

### *Example 1*
```
tyasharma@Adityas-MBP technical % grep -n "alcohol" government/Alcohol_Problems/Session3-PDF.txt
10:Excessive alcohol consumption plays an important role in many of
13:documented the presence of alcohol among patients admitted to
15:studies have demonstrated that even blood alcohol concentration
16:(BAC) determinations under-estimate the extent of alcohol problems
19:admission, and the fact that alcohol is a risk factor both for the
22:alcohol problems in these settings.8-12 Although there are problems
31:intervening effectively with alcohol problems in emergency
45:patients with alcohol problems encountered in the emergency
52:asked, "To what extent do you believe your alcohol consumption was
70:We do know that alcohol consumption changes for many problem
74:However, changes in alcohol consumption are often not sustained
79:emergency department seem to dissipate without an alcohol-specific
91:of re-admission or prevent re-injury related to alcohol
117:alcohol workers intervening with problem drinkers. A brief
118:intervention in an emergency department by alcohol health workers
122:referral to alcoholism treatment for patients and families who
125:alcohol treatment in 62% of the 100 consecutive cases
131:drinking or in successful connection with appropriate alcohol
133:have used blood alcohol concentration as one of the critical
144:the mechanism of action of these interventions was reduced alcohol
152:alcohol consumption and consequences. Several current publications
157:combination of blood alcohol concentration (BAC), serum gamma
171:reduction occurred among the patients with mild to moderate alcohol
177:with more chronic and severe alcohol dependence. Another limitation
185:following an alcohol-related event randomly assigned 94 of the 184
188:driving and a list of alcohol treatment agencies. The intervention,
194:alcohol-related injuries, and alcohol-related problems were
209:specialists trained in alcohol or substance abuse counseling or in
217:avoid alcohol-related injuries in the future. Substance abuse
223:settings have delivered brief alcohol-focused interventions. These
226:brief, patient-centered alcohol counseling intervention delivered
228:produced significant reductions in alcohol consumption among both
232:alcohol intervention.9,26,35,36 However, few studies of
237:these alcohol-focused interventions for a variety of practical,
241:problematic alcohol consumption, the connection between injury and
250:alcohol is the goal of these treatment programs.37 On the other
261:abstinence from alcohol.
268:alcohol interventions.25 However, postponing intervention to the
274:alcohol interventions in medical settings have been effective,32
298:department and trauma center patients into alcoholism
320:This review of interventions, focused on addressing alcohol
333:have alcohol use problems, and there are published guidelines for
337:positioned to implement pro-grams of alcohol screening,
339:control and prevention, little has been done to incorporate alcohol
342:of trauma centers which revealed that blood alcohol testing, which
349:to identify patients with alcohol use problems.
351:regarding alcohol problems in emergency departments, a survey of
354:alcohol-impaired drivers.41 However, ambivalent attitudes were
355:revealed concerning alcoholics and alcoholism. On a scale of 0
356:(strongly disagree) to 7 (strongly agree) the statement "alcoholics
358:statement "alcoholism is a treat-able disease" received a mean
362:"defeatism about alcoholism management." In a recent survey of
363:emergency medicine physicians, 78% agreed that alcohol
371:asking about alcohol use but few used recommended screening
389:settings to reduce drinking and alcohol related risks. The first
393:problems can be identified along a range of alcohol use and
397:set for more or less severe alcohol problems. However, whatever the
414:the alcohol problem and the needs of the patient. Many treatment
416:by level of alcohol problem, although controlled trials do not
425:screening instrument that identifies individuals with alcohol
430:interventions, understand alcohol problems, and are armed with a
453:levels of severity? Individuals with less severe alcohol problems
463:the intervention for alcohol problems? Most emergency department
501:make interventions for alcohol problems more feasible? For example,
526:template with options incorporating the alcohol problem
530:been published that deal with alcohol dependence and abuse and
538:Zuska, a surgeon with an interest in alcohol problems among injured
539:patients noted: "The crisis that brings the alcoholic to the
545:alcohol problems have the potential to reduce alcohol-related
551:1. Cherpitel CJ. Screening for alcohol problems in the
553:2. Degutis LC. Screening for alcohol problems in emergency
557:3. Ewing JA. Detecting alcoholism: the CAGE questionnaire. JAMA
567:alcohol abuse in trauma patients. Arch Surg 1993;128:907-13.
573:PA, Craig SA, Zink BJ. Patients with alcohol problems in the
578:PA, Craig SA, Zink BJ. Patients with alcohol problems in the
589:role of alcohol and other drugs-an EAST position paper prepared by
593:alcohol-related injuries. Substance abuse interventions in general
600:Russlee AC. Attribution of injury to alcohol involvement in
602:seriously injured in alcohol-related motor vehicle crashes.
623:reduction with alcohol-positive older adolescents in a
633:opportunity to initiate treatment in the alcoholic. Am J Surg
653:alcohol-related trauma. Br J Oral Maxillofac Surg
658:alcohol health worker in an accident and emergency
675:alcohol problems. Acad Emerg Med 2000; 7:1383-92.
681:Brief physician advice for problem alcohol drinkers: a randomized
686:recovery after alcoholism treatment. JAMA 1992;267(5):663-7.
691:for performing alcohol interventions in trauma centers. J Trauma
698:alcohol problems: a review. Addiction 1993;88:315-36.
708:alcohol-impaired drivers: results from a national survey of
711:surveillance of alcohol intoxication after motor vehicular
714:attitudes concerning intervention for alcohol abuse/dependence in
717:interventions for alcohol problems: a national survey of primary
726:reduce alcohol intake in primary health care populations: a
729:alcoholism. In: Gurman AS, Jacobson N, editors. Clinical Handbook
740:trauma patients for alcohol problems: are insurance companies
774:emergency department (ED) with alcohol problems. We have just heard
792:to report heavy drinking, consequences of drinking, alcohol
793:dependence, or history of treatment for an alcohol problem.2
812:patients about their alcohol use. The intervention featured, the
864:often tracked. Why not include patients with alcohol problems in
876:alcohol consumption or decreases in negative consequences, such as
910:department: screening and brief intervention for alcohol problems
933:alcoholic client: The influence of experience, support, training,
949:psychotherapy for alcohol dependence. Arch Gen Psychiatry
962:Reducing death and disability related to alcohol remains a
965:identify alcohol problems and to begin interventions, particularly
967:compelling reasons make the ED an important setting for alcohol
972:alcohol problems are released from the ED rather than being
976:identification of and intervention for an alcohol problem.
1003:efficacy and ultimate effectiveness of brief alcohol interventions
1005:or alcohol-dependent drinkers. It is clear from their manuscript
1006:that a spectrum of alcohol problems presents in the ED and that a
1013:or deliver brief alcohol interventions in the ED. Previous research
1017:attrition rates, types of interventions, levels of alcohol use,
1020:drinkers, problem drinkers, alcohol-dependent drinkers) and the
1024:Brief alcohol interventions have generally included feedback by
1026:positive) to questions about alcohol consumption or consequences.
1035:effective, an ED-based brief alcohol intervention model that
1041:alcohol use. It is thought that this is particularly true if the
1046:providers cannot easily find time to conduct brief alcohol
1050:interest in doing alcohol interventions in the ED. On the other
1052:it difficult to address alcohol issues at all, particularly for
1054:conditions clearly linked to alcohol consumption.
1055:The implementation of brief alcohol intervention systems in
1058:first step, but implementation of proven alcohol screening and
1064:alcohol consumption of at-risk drinkers and the limited time for
1067:research on brief alcohol interventions specifically with the use
1076:positive for at-risk drinking or more serious alcohol-related
1082:system of intervention. Just as there is a spectrum of alcohol use
1090:New directions in brief alcohol interventions in emergency
1107:multiple health risks (e.g., smoking, alcohol use, seat belt use),
1118:to alcohol misuse and abuse.
1120:alcohol problems to those with severe dependence. In the next few
1125:alcohol use. Any methods that are developed with researchers and
1138:of alcohol-related emergency room admission. J Stud Alcohol
1150:alcohol-related injuries. Substance abuse interventions in general
1156:McCarthy M, Russlee AC. Attribution of injury to alcohol
1157:involvement in young adults seriously injured in alcohol-related
1169:physician advice for problem alcohol drinkers: a randomized
1176:alcohol health worker in an accident and emergency
1208:what motivates patients to change their use of alcohol. He noted
1215:alcohol or not, patients did equally well at follow-up.
1222:alcohol-related negative consequences and injuries at 1 year.
1250:of the study was to encourage post-discharge alcohol treatment, but
1289:alcohol-related harm, he was disappointed to find no effect on
1332:Many of the college students who visit the ED have mild alcohol
1333:problems and are confident they could overcome their alcohol
1360:control groups receive so much attention focused on alcohol that it
1365:about alcohol, and that could affect their answers. These
1368:severe alcohol problems is premature. In his study of adolescents,
1375:participate in research still had measurable blood alcohol levels.
1379:correlate mental status exam scores with alcohol levels at the time
1382:blood alcohol level patients could remember an intervention. If
1431:they know we need to be addressing alcohol problems. She asked the
1482:alcohol problems.
1486:like an appropriate venue for alcohol interventions because many ED
1487:patients have alcohol problems and the ED visit may represent a
1491:screen for alcohol-related problems, then primary care has failed.
1511:resources currently spent on alcohol problems in the ED. She noted
1512:that we have to help patients who have severe alcohol problems.
1545:severity of injury, degree of alcohol dependence, readiness to
1567:Patricia Perry reported that one alcohol intervention project in
1584:Jean Shope expressed her belief that addressing alcohol problems
1589:believed that the ED setting is just one of many where alcohol
1596:selling alcohol interventions because they are in competition with
1615:alcoholics anymore. Most use other substances as well, so it is
1630:it did not lead to changes in alcohol variables or weapon
1638:of alcohol problems was higher than other risk factors. Physicians
```

### *Example 2*
```
adityasharma@Adityas-MBP technical % grep -n "effect" government/Alcohol_Problems/Session3-PDF.txt
21:occasioned a call for an effective method of intervening with
31:intervening effectively with alcohol problems in emergency
81:natural or unaided salutary effect on drinking resulting from
83:emergency setting,20 that effect appears to be short-lived for many
149:and effect sizes reported in these studies were modest.
205:was strong for a harm reduction effect across various indicators of
224:interventions also appear to be effective in reducing drinking and
258:of problem drinkers and have been found to be effective in reducing
274:alcohol interventions in medical settings have been effective,32
293:studies that have demonstrated effects either with volunteer or
294:randomized participants is modest but increasing, and the effects
317:appear to be as effective as some type of specific
323:to creating sustained, effective intervention programs in the
327:trauma center implement a coordinated, effective, and feasible
379:effectiveness studies. Feasibility and successful dissemination
385:effectiveness studies can then be used to promote change in
390:step to developing an effective and efficient intervention program
465:best persons to provide effective treatment.42 There are a variety
487:be more effective in reaching emergency physicians and nurses?
783:effect demonstrated in 32 of these studies.1 We also know that the
796:effectiveness trials. In doing so, we face unique challenges. These
803:To be effective, our research strategies must be brief and
821:To be successful in developing effectiveness trials in the ED
888:the effect of the brief intervention may be short lived. Therefore,
891:may be a "sleeper effect," or delayed emergence of treatment
895:we are to prove that SBI is effective in the ED setting. It is
936:physician performance: a systematic review of the effect of
953:for cocaine dependence: delayed emergency of psychotherapy effects.
1003:efficacy and ultimate effectiveness of brief alcohol interventions
1015:effective in reducing drinking levels across of variety of health
1018:outcomes measured, and effect sizes have varied greatly across the
1027:These results indicate that while this approach is effective for a
1028:percentage of hazardous drinkers, it is not effective for everyone
1029:(effect sizes of ~30% to 40%). The intervention studies based on
1035:effective, an ED-based brief alcohol intervention model that
1044:moment may be effective for non-injured persons who drink at risk
1072:In addition, because of the effect sizes shown by the studies to
1088:health perspective, methods are sought that are the most effective
1098:found effective in the areas of depression, smoking cessation,
1194:The effects of computer-tailored smoking cessation messages
1261:evaluate the effect of counselors' skill levels. In future trials,
1279:or ED staff is more cost effective than using specially hired
1289:alcohol-related harm, he was disappointed to find no effect on
1326:short-lived effect that degrades over time. Consequently, a booster
1342:concurred with Hungerford's observation that intervention effects
1346:Maintenance of effect might be possible with yearly
1366:methodological problems can mask valid intervention effects.
1370:patients who showed a differential effect from the brief
1436:better in 12-step programs. However, to examine the effect of
1467:Longabaugh noted one matching effect that persisted throughout
1570:shown to be effective, they will have to be adapted to new
1602:can intervene effectively and simultaneously for the top two or
1667:efficacy or effectiveness studies behind them are adopted and
```


### *grep -w*

use: It is advantageous for us when words possess the capacity to have often used substrings.
function: This is the scenario you should be in if you want to match words solely, without including substrings.

### *Example 1*
```
adityasharma@Adityas-MBP technical % grep -w "terrorism" 911report/chapter-2.txt 
                terrorism and of attacks on civilians, he replied:"We believe that the worst thieves
                terrorism, without the need for the Islamic Army Shura. Bin Ladin was prepared to
```

### *Example 2*
```
adityasharma@Adityas-MBP technical % grep -w "Colin" 911report/chapter-10.txt
                State Colin Powell, who had returned from Peru after hearing of the attacks, joined
```

### *grep -c*

use: It helps us find recurrent words and phrases in a large data set.
Function: This counts the number of lines in the given text that correspond to a certain pattern.

### *Example 1*
```
adityasharma@Adityas-MBP technical % grep -c "is" 911report/chapter-2.txt
368
```
### *Example 2*
```
adityasharma@Adityas-MBP technical % grep -c "it" 911report/chapter-3.txt
1131

```

### *grep -r*

use: When there are phrases that could be discovered in multiple directories, it is helpful.
Function: You want to look for matching patterns in each of the aforementioned directories' subdirectories as well as all of the directories themselves.

### *Example 1*
```
adityasharma@Adityas-MBP technical % grep -r "police" 911report 
911report/chapter-13.4.txt:                coincided with a police station bombing in Zagreb where the timing device of the
911report/chapter-13.4.txt:                other than the CIA. According to Lance, the Philippine police officer, who after
911report/chapter-13.4.txt:                police custody in Qatar. See CIA briefing by CTC specialists (June 22, 2004); Walter
911report/chapter-13.4.txt:                Hamburg police, and the UAE official's search, see German BKA report, investigative
911report/chapter-13.5.txt:                recorded calls to the Port Authority police desk from people in the towers on
911report/chapter-13.5.txt:                from police that morning.
911report/chapter-13.5.txt:                special approval by senior U.S. government officials. On September 13, Tampa police
911report/chapter-13.5.txt:                the airport so they could get on a plane to Lexington. Tampa police arranged for two
911report/chapter-13.5.txt:                Saudi nationals debarked from the plane and were met by local police. Their private
911report/chapter-13.5.txt:                security guards were paid, and the police then escorted the three Saudi passengers
911report/chapter-13.5.txt:                to Lexington by a local police officer in Lexington who did not have firsthand
911report/chapter-13.5.txt:                White House to kill the president. The man was shot by police and then killed
911report/chapter-13.5.txt:            8. For Pakistan's unpoliced areas, see Tasneem Noorani interview (Oct. 27, 2003).
911report/chapter-13.3.txt:                line workers, but not police or the Department of Corrections, from transmitting
911report/chapter-13.3.txt:            47. On the relationship between the FBI and state and local police forces, see
911report/chapter-13.3.txt:                screener. The terminal was evacuated, and police found miscellaneous gun parts,
911report/chapter-3.txt:            Yousef was captured in Pakistan following the discovery by police in the Philippines
911report/chapter-3.txt:                in tracking fugitives, with much local police knowledge. The department's Drug
911report/chapter-3.txt:                specifically accorded "no police, subpoena, or law enforcement powers or internal
911report/chapter-3.txt:                only for the FBI and CIA but also for local police.
911report/chapter-3.txt:                enhanced, at least on paper, Clarke's authority to police these assignments. Because
911report/chapter-3.txt:                critical infrastructures, our power systems, water supplies, police, fire, and
911report/chapter-3.txt:                police from an al Qaeda cell in Nairobi.
911report/chapter-6.txt:                was a signal for Abu Hoshar to commence a terrorist operation, Jordanian police
911report/chapter-6.txt:                informed the President that the FBI would advise police in the United States to step
911report/chapter-6.txt:                governments' police and intelligence officers to stop them. You are left waiting for
911report/chapter-7.txt:                law-abiding citizen with long-standing, friendly contacts among local police and FBI
911report/chapter-7.txt:                police and a UAE representative tried to find him in Germany, visiting mosques and
911report/chapter-7.txt:                in Hamburg. The UAE government then told the Hamburg police they could call off the
911report/chapter-7.txt:                Arabia that borders Yemen; this weakly policed area is sometimes called "the wild
911report/chapter-9.txt:                local public servants, especially the first responders: fire, police, emergency
911report/chapter-9.txt:            Most Port Authority police commands used ultra-high-frequency radios. Although all
911report/chapter-9.txt:            The 40,000-officer NYPD was headed by a police commissioner, whose duties were not
911report/chapter-9.txt:            The 11,000-member FDNY was headed by a fire commissioner who, unlike the police
911report/chapter-9.txt:                Authority police desk in 5 WTC, to be activated by members of the Port Authority
911report/chapter-9.txt:                police when the FDNY units responding to the WTC complex so requested. However, in
911report/chapter-9.txt:            Civilians who called the Port Authority police desk located at 5 WTC were advised to
911report/chapter-9.txt:            Several South Tower occupants called the Port Authority police desk in 5 WTC. Some
911report/chapter-9.txt:                working on upper floors. Chiefs also spoke with Port Authority police personnel and
911report/chapter-9.txt:                Authority police officer to evacuate the South Tower, because in their judgment the
911report/chapter-9.txt:                and 800 police officers from all over the city. The Chief of Department arrived at
911report/chapter-9.txt:            The Port Authority's on-site commanding police officer was standing in the concourse
911report/chapter-9.txt:                officers in the WTC Command to meet at the police desk in 5 WTC. Soon thereafter, he
911report/chapter-9.txt:            One Port Authority police officer at the WTC immediately began climbing stairwell C
911report/chapter-9.txt:            Within minutes of impact, Port Authority police officers from the PATH, bridges,
911report/chapter-9.txt:                calamity in the North Tower. This order was given over WTC police radio channel W,
911report/chapter-9.txt:            At 8:59, the Port Authority police desk at Newark Airport told a third party that a
911report/chapter-9.txt:                Port Authority police desk in Jersey City confirmed that employees on the 64th floor
911report/chapter-9.txt:                should "be careful, stay near the stairwells, and wait for the police to come up."
911report/chapter-9.txt:                When the third party inquired again at 9:31, the police desk at Newark Airport
911report/chapter-9.txt:                advised that they "absolutely" evacuate. The third party informed the police desk
911report/chapter-9.txt:                concourse, where other police officers guided them to exit the concourse and complex
911report/chapter-9.txt:                decided to send one ESU team (each with approximately six police officers) up each
911report/chapter-9.txt:            Throughout this period (9:03 to 9:59), a group of NYPD and Port Authority police
911report/chapter-9.txt:            Initial responders from outside PAPD commands proceeded to the police desk in 5 WTC
911report/chapter-9.txt:                police desk reporting at least 100 people trapped.
911report/chapter-9.txt:                9:30, the PAPD central police desk requested that responding officers meet at West
911report/chapter-9.txt:                advised orally to leave the building by other firefighters and police who were
911report/chapter-9.txt:                police officers to descend because they lacked the protective gear and equipment
911report/chapter-9.txt:                needed to handle the increasing smoke and heat. The police officers reluctantly
911report/chapter-9.txt:                teamed up with a Port Authority police officer and acted as a spotter in advising
911report/chapter-9.txt:                37 fatalities-the largest loss of life of any police force in history. The NYPD
911report/chapter-9.txt:                suffered 23 fatalities-the second largest loss of life of any police force in
911report/chapter-9.txt:                response. Many fire and police agencies that responded had extensive prior
911report/chapter-9.txt:                attack. In addition to county fire, police, and sheriff 's departments, the response
911report/chapter-9.txt:                were not (1) fire or police first responders, (2) security or fire safety personnel
911report/chapter-9.txt:                themselves. Although there were ESU teams and a few individual police officers
911report/chapter-9.txt:                command that comprehensively deploys all dispatched police, fire, and other first
911report/chapter-9.txt:            The story with respect to Port Authority police officers in the NorthTower is less
911report/chapter-9.txt:                Authority police evacuation order was given. Since September 11, the Port Authority
911report/chapter-12.txt:                violent extremism. According to Karachi's police commander, there are 859 madrassahs
911report/chapter-12.txt:            The country's vast unpoliced regions make Pakistan attractive to extremists seeking
911report/chapter-12.txt:                with al Qaeda. Saudi police are regularly being killed in shootouts with terrorists.
911report/chapter-10.txt:                of a military police lead vehicle and a van; the proposed briefing theater had no
911report/chapter-11.txt:                officials-local airport managers and local police departments- who had not seen such
911report/chapter-11.txt:                concerned citizens. Representatives of the Justice Department, the FAA, local police
```


### *Example 2*
```
adityasharma@Adityas-MBP technical % grep -r "addiction" biomed 
biomed/1472-6807-2-1.txt:        addiction liability and other undesirable side-effects of
biomed/1472-6807-2-1.txt:        addiction, and alpha7-alpha7 with GABA release [ 4 ] .
biomed/1471-2458-2-25.txt:              okay. That was due to my addiction, not getting the
biomed/1472-684X-1-5.txt:          opioid analgesics for pain management causes addiction [
biomed/1472-684X-1-5.txt:          27 ] . Confusion about the differences between addiction,
biomed/1472-684X-1-5.txt:          The hallmark of opioid addiction is psychological
biomed/1472-684X-1-5.txt:          Care must be taken to differentiate a true addiction
biomed/1472-684X-1-5.txt:          (substance use disorder) from pseudo addiction due to
biomed/1472-684X-1-5.txt:          time), is not evidence of addiction, [ 30 ] and is rarely
biomed/1472-684X-1-5.txt:          unintended effect), or cause addiction are not relevant.
```



## *SOURCES*

*I looked into the different grep command kinds and their implementations using Chat GPT*
