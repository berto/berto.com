## Why

Around 2019, after 2 years working in the Rows.com platform (then dashdash.com), I realized that we were building more than a spreadsheet. We were building a translator. 

- Our editor is, essentially, just a bunch of rectangles (cells). Users can write a language into them, which is the spreadsheet language. This language includes values and formulas, and other visual notations like data formats, colors. 
- How does the system work? Well, when users write stuff into the cells, we automatically generate a code representation of the user's input in the front end, in the back end, and we also have a method to keep both -ends synchronized. Our computation engine consumes this technical notation and performs any necessary calculations.
- If we wanted, we could generate a human-readable representation of the spreadsheet, before technical code. Example: `A1: 5` can represent a cell with a literal of value 5. `A1: =2+2 =>5` is a cell with a formula that results in the same value. 
- So, instead of forcing every user to interact with our spreadsheet language via our interface, we could have contractualized this interaction via a editable human notation that describes the spreadsheet. We would keep the table interface, but we'd also offer the human-readable representation of the spreadsheet. At a minimum, this would make it easier for our community to create scripts to generate spreadsheets. We could take it one step further and open the engine that translates this human notation into the actual code that executes on that particular spreadsheet.
- In a way, this wouldn't be that different from Markdown (see also Excalidraw, Mermaid). It is a bit more complicated than markdown, and a bit simpler than programming languages for engineers. 

This is how this document came to be. 

## The goal of Full-Stack Markdowns

To build systems where human readable notations get translated into code.

## The Problem

- coding is hard. coding is getting more complex by the day, with multiple layers of OS, frameworks, libraries, APIs, conventions, best practices, etc.
- most Low-code-No-code platforms are very proprietary and that will mean trouble.
    - few to no programming languages were ever successful while being closed/ proprietary.
    - while having an API counts as being "open", APIs often mean a gatekeeper to give you keys, to develop and maintain them.
    - the market for solutions moves in unforeseen ways, which makes it hard to keep pace unless you're investing a f- lot.
    - even with large enough investments, a platform must keep pace with the underlying paradigms, OSes, devices and form-factors, which introduce new problems and opportunities. Examples: mobile, tablets, responsive, cloud, watch, lambda, VR, AR, crypto.
    - experimentation and adaptation is best provided by the community of pros.
- pure UI drag and drop frameworks hide the logic and expressiveness of the underlying domain language (which maps to a problem space).. With the pressure to ship, this creates wrong incentives for engineering teams, who have poorly defined or hidden contracts between the Creators and the actual Code.
    - Visual development is still very interesting, but it should neither negate a tangible artifact (the markdown) nor imply being proprietary. 

## The Solution

- just as markdown translates between text and html+css, I propose that there can be N textual languages that codify a whole stack: FE (code and style)+BE+Data+comms+infra. A full-stack-markdown or human-readable-everything-as-code.
- I think that more than the particular FSMD (full stack markdown language), we need to create the software where the FSMDs are used. Think of a VSCode or Github for business people.
- In the FSMD software, there are 4 separated layers:
    1. the human readable code.
    2. the code translated from of 1.  
    3. The visual rendering of 2.
    4. Navigation, settings, etc.
- All layers should be interpreted in real-time, editing should be possible on any. (I assume this is a very hard challenge). That means, the creator should be able to change code, change the programming language translation, and/or change the visual rendering, all at once.
- Our software should be an editor which, for each folder or group of folders executes a certain script (the FSMD parser).
- FSMDs should reuse as much pre-existing code as possible. The core of this business is to create the platform, not the individual FSMDs. 

## Use cases

FSMDs should allow for many solutions. 

- creating a personal blog from markdown files.
- creating a website for a company.
- rendering a gallery of photos from a folder with image files.
- rendering vanilla markdown within a folder.
- rendering excalidraw files within a folder.
- rendering code for a wiki (Notion-like).
- creating a workflow (Zapper-like).
- creating a drive of mixed blocks that are files and links and comments that are navigable and downloadable.
- do a small mathematical model and represent it live.
- create a visual interface for a MySQL/ SQLite database.
- create a simple shopping cart for sales.
- store and read (and share) passwords as encrypted files.

# Proof of concept

TBA.
