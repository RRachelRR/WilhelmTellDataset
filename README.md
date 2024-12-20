![WilhelmTellHeader](https://github.com/user-attachments/assets/1550a5bb-9e08-4ac6-9335-79f20deb43c4)

# The Wilhelm Tell Dataset of Affordance Demonstrations

The Wilhelm Tell Dataset is a novel dataset for affordance learning of common household tasks. Our dataset consists of video sequences demonstrating tasks from first- and third-person perspectives, along with metadata about the affordances that are manifested in the task, and is aimed towards training perception systems to recognize affordance manifestations.  The demonstrations were collected from 23 participants and in total record about seven hours of human activity.

![e70069e0-99d1-4c22-b1f0-15abca138e56](https://github.com/user-attachments/assets/9222d47d-5e8b-4d1a-a4a1-fe2cb4b6006e)
*Picture showing a comparison of both perspectives recorded in the dataset* 

## Data collection methodology

Participants were asked to stand in front of a table with a variety of household objects and instructed to perform various small tasks centered around apples, using the objects
to demonstrate affordances. The tasks were filmed from the ego perspective using a GoPro headset camera and from the frontal perspective using a stationary camera.

![ca1e3842-5765-4206-845d-5596f6627405](https://github.com/user-attachments/assets/12330d6b-487c-4dea-a815-f38a0eb7ed22)
*Picture of lab environment showing the table with the objects as well as the recording setup*

The data was collected in three sessions. In the first sessionceight participants were asked to complete 14 tasks in two bundles of 7 as shown in Table I. Task 3 and 4 were varied with the a option used in the first round and the b option used in the second round of the study. The tools used were switched after the first 7 tasks to provide more variety in the recordings and the apple was replaced with an intact one.

| Id | Task Given | Demonstrated Affordance |
|------| -------- | ------- |
| 1 | Please stab the apple with the fork and lift it. Then move it around a bit and take it off the fork, if needed with your fingers.  | Stab    |
| 2 | Now cut the apple in halves with the knife. | Cut (AffordanceNet)     |
| 3 | Please now stab one of the apple halves with the fork and lift it. Then move it around a bit and take it off the fork, if needed with your fingers, and \{(a) return it to the cutting board/(b) put it into the mug\}    | Stab |
| 4 | Please put \{(a) the apple pieces/(b) the other apple half\} into the mug.    | Contain - ability (AfNet) / Contain (AffordanceNet) |
| 5 | Pick up the mug and move it around a bit, tilting it a bit without spilling its contents. Look into the cup as you move it around.    | Contain - ability (AfNet) / Contain (AffordanceNet) |
| 6 | Now pour the apple halves into the bowl.    | Pour |
| 7 | Pick up the bowl and move it around a bit, tilting it a bit without spilling its contents. Look into the bowl as you move it around.   | Contain - ability (AfNet) / Contain (AffordanceNet) |

For the second and third recording session the list of tasks was expanded with more tasks that demonstrate additional affordances. Due to the time needed for those added tasks theywere split into four parts. During the first round participants completed tasks 8-10 in the a-variant and then continued with tasks 1-7 in the a-variant. The objects were then replaced with different variations of the same object and the participants repeated tasks 8-10 and then 1-7 in the b-variant. Afterwards the objects on the table were replaced with different objects and the participants received instructions for tasks 11-20 in the a-variant. Following this, the objects were again replaced with different variations, and participants then instructed to complete tasks 11-20 in the b-variant.

| Id | Task Given | Demonstrated Affordance |
|------| -------- | ------- |
| 8 | Please roll the apple over the table \{(a) with your hand/(b) from hand to hand\} a few times.  | 3D - roll ability (AfNet) |
| 9 | Please wrap the apple in the \{(a) dishtowel/(b) tinfoil\}, pick up the wrapped apple, move it around a bit and then unwrap it and return both items to the table. | Wrap - ability (AfNet)     |
| 10 | Please take the knife and carve an X into the apple.    | Engrave + Incision ability (AfNet) |
| 11 | Please stack the four \{(a) plates/(b) books\} on top of each other.    | Stack - ability (AfNet) |
| 12 | Please take the wine glass and roll it over the table \{(a) with your hand/(b) from hand to hand\} a few times.   | 2D - roll ability (AfNet) |
| 13 | Please pick up the stack of \{(a)plates/(b) books\} and move it around a bit, then return it to the table.    | Stack - ability (AfNet) |
| 14 | Please take the pencil and write the word “apple” \{(a) into the notebook/(b) onto the post-it\}   | Engrave (AfNet) |
| 15 | Please pick up the large bowl with \{(a) sugar/(b) chia seeds\} and move it around a bit, without spilling its contents, then return it to the table.  | Contain - ability (AfNet) / Contain (AffordanceNet)    |
| 16 | Then take the funnel and use it to transfer the \{(a) sugar/(b) chia seeds\} from the large bowl into the mug. Then remove the funnel. | Flow Support ability (AfNet)     |
| 17 | Please take the spoon and use it to transfer the \{(a) sugar/(b) chia seeds\} into the small bowl. Use the spoon for the first four or five spoonfuls, afterwards you can pour the rest.    | Scoop (AffordanceNet) |
| 18 | Put apple halves into the small bowl with \{(a) sugar/(b) chia seeds\}.    | Contain - ability (AfNet) / Contain (AffordanceNet) |
| 19 | Please place the colander over the empty large bowl. Pour the \{(a) sugar/(b) chia seeds\} and the apple into the colander. Then lift the colander and move it over the bowl until the \{(a) sugar/(b) chia seeds\} drops through, then return it to the table.    | Filter - ability (AfNet) |
| 20 | Please pick up the \{(a) mixing cup and insert it into the blender/(b) blender plug and plug it into the extension cord. The extension cord is not plugged in, so there is no danger. Then pick up the extension cord and move it around a bit, then return it to the table\}.    | Connect - ability (AfNet) |

### Description of the data

The data is split into folders by participant id. Each participant folder contains the ego and frontal perspective videos in mp4 format for each bundle of tasks as well as a video containing all task bundles in one.

```
WilhelmTellDataset/
  -P1/
    -P1_Ego_1.mp4
    -P1_Ego_2.mp4
    -...
    -P1_Ego_Complete.mp4
    -P1_Frontal_1.mp4
    -P1_Frontal_2.mp4
    -...
    -P1_Frontal_Complete.mp4
    -...
  -P2/
    -P2_Ego_1.mp4
    -P2_Ego_2.mp4
    -...
    -P2_Ego_Complete.mp4
    -P2_Frontal_1.mp4
    -P2_Frontal_2.mp4
    -...
    -P2_Frontal_Complete.mp4
    -...   
  -...
  -train_test_split.yml
  -README.md
  -LICENSE.md

```

### File formats

- 189 videos in MP4 format with a total of 417 minutes of material

## Test-Train Split

The videos of bundles of tasks from each participant and angle were grouped into 102 training videos and 44 testing videos. A typical use case we envision for the dataset is to use a perception system capable to detect object interactions to automatically label frames from the training videos and then use the annotated frames to train an object detection or semantic segmentation model. The goal of this process is to teach the semantic segmentation model to detect functional parts of objects, i.e. parts particularly relevant for manifesting some affordance, both in contexts where the affordance is manifested and in contexts where the object sits idle. Some of the frames of the test videos are annotated to segment functional parts. For the test videos, annotations of when affordances manifest are also available, allowing to evaluate systems that would perform event segmentation. 

## Download link

* [Wilhelm Tell Dataset Repository](https://nc.uni-bremen.de/index.php/s/3prZnQBz7pL8M2i) - Link to the dataset videos hosted on university servers.

## Related publications

[Link]() and Bibtex for HRI paper here

## Authors

* **Rachel Ringe** - rringe@uni-bremen.de 
* **Mihai Hawkin** - mpomarlan@uni-bremen.de
* **Nikolaos Tsiogkas** - nikolaos.tsiogkas@kuleuven.be
* **Stefano De Giorgis** - stefano.degiorgis2@unibo.it
* **Maria Hedblom** - maria.hedblom@ju.se
* **Rainer Malaka** - malaka@tzi.de

## License

This project is licensed under the CC-BY license - see the [LICENSE.md](LICENSE.md) file for details

## Maintenance Plans

The videos, still images, and annotation files are hosted on university servers and on the [NEEMHub](https://vib.ai.uni-bremen.de/page/softwaretools/neemhub/), an infrastructure dedicated to maintaining artifacts created during our supporting collaborative research center, [EASE](https://ease-crc.org).

## Acknowledgments

This work was funded by the FET-Open Project #951846 [*MUHAI – Meaning and Understanding for Human-centric AI*](https://muhai.org) by the EU Pathfinder and Horizon 2020 Program.

This work has also been supported by the German Research Foundation DFG, as part of Collaborative Research Center 1320 Project-ID 329551904 [*EASE -- Everyday Activity Science and Engineering*, University of Bremen](https://www.ease-crc.org). The research was conducted in subproject *P01 – Embodied semantics for the language of action and change: Combining analysis, reasoning and simulation*
