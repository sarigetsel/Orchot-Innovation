# Orchot

A classroom system for a guided group project. Students move through a fixed process on their screens: define a challenge, choose an idea, design a product, send it to the lab machines, and finish with a personal summary. The teacher runs the lesson from a control panel: processes, screens, goals, timers, budget, the content library, and the materials catalog.

## Process video

The video walks through the whole lesson: control panel, student entry, stages A–G, and sending the product to the machines.

https://github.com/user-attachments/assets/a4f97afb-30d3-4b25-aaa1-9f7d294c4d60

## Who uses it

| Who | What they do |
|-----|----------------|
| Teacher | Opens a process, sets the goal, presentation time, and budget, assigns screens to groups, manages the content library and the materials catalog, and can pause a process, a group, or one student |
| Student | Enters from her group's screen, fills in the stages, and sees the group's work update live |
| Group | Each stage has a coordinator who collects the group's answers. The others keep contributing from their own screens |

A screen that is not assigned to an active process cannot enter. After the student picks a name and an avatar, the welcome screen locks.

## The process

| Stage | What happens |
|-------|----------------|
| Opening | The screen identifies itself, the process is explained, the student picks an avatar and a name, and joins her group |
| A · Define the challenge | Goal, current state and desired state, the group board, a summary, and the challenge question |
| B · Needs and constraints | A shared list, ranking, and a summary of the challenge |
| C · Sources and ideas | Search the library, a personal idea, a presentation round, ranking, and a fit table until the group chooses one option |
| D · Sketch and design | Product vision, inspiration images (each student shares one; the coordinator keeps one to three), what to take from each image, look and feel, product items, and the product sheet |
| E · Preview and choice | The sketch is generated, personal opinions and the group impression, improvements, the materials store within the budget, and a fit check against the challenge, the needs, and the age group |
| F · Print model | Files are built and sent automatically. Each item is routed to a machine by material and action |
| G · Evaluation | Strengths and weaknesses, scores, a closing word, three questions, a personal certificate, and a thank-you screen |

Students can go back and view screens they already passed. Editing stays on the live screen, except during an active improvement loop.

## Lab machines

Stage F does not ask the group to pick a machine. Material plus action decides the route:

| Machine | When |
|---------|------|
| Wide-format plotter | Print, and print-and-cut for vinyl |
| Laser printer with camera | Cut or engrave around artwork that is already printed |
| Manual laser | Cut or engrave with no print |
| Double bend | Fold and bend |
| Vacuum forming | Heat-and-vacuum forming of plastic |
| Sublimation printer and heat press | Print on fabric, then press it onto the product |

A material and action the lab cannot run is stopped, and the group sees a message in Hebrew.

## How it is built

| Part | Role |
|------|------|
| Interface | React and TypeScript, Hebrew, right to left. Student screens and the control panel |
| Server | Spring Boot. Stores the process, sketches, evaluation, and the machine handoff |
| Sync | The group sees the same answers as they are submitted. A pause from the control panel reaches the screens immediately |
