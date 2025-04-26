Pocketix V1 Project Overview
============================

**Pocketix** is a block- and form-based visual programming language and editor currently being developed by [Petr John](mailto:ijohn@fit.vut.cz) and [Jiří Hynek](mailto:hynek@fit.vut.cz) at [BUT FIT](https://www.fit.vut.cz/.en), primarily aimed at automating smart devices on mobile phones.

The first prototype was created through a collaboration between BUT FIT and [Logimic](https://www.logimic.com/cs/) as part of the project _Services for Water Management and Monitoring Systems in Retention Basins_.

More information is available on the [Pocketix GitHub Organization](https://github.com/pocketix).

**Pocketix V1** specifically refers to the current ecosystem of editors and interpreter built around the first version of the Pocketix scripting language.

Pocketix V1 Editor (React & Angular)
------------------------------------

**pocketix-react** and **pocketixng** provide drag-and-drop interfaces for designing automation flows. These editors are ideal for non-programmers and built on React and Angular respectively.

*   [React Editor Demo](https://pocketix-react.pocketix.org/)
*   [Angular Editor Demo](https://pocketixng.pocketix.org/)

### Key Features

*   Block and form-based editing
*   Configurable conditions and actions
*   Device integration and workflow logic
*   Compatible with Pocketix V1 scripting

### Quick Start

```bash
git clone <repo_url>
cd <repo_dir>  
npm run install:all  
npm run start:demo
```

Replace `<repo_url>` and `<repo_dir>` with the actual repository info.

Pocketix Node Interpreter
-------------------------

**Pocketix Node** is the backend logic engine that interprets automation flows from the editors and outputs clean, testable commands — with zero risk of triggering hardware unintentionally.

### Key Features

*   Dry-run automation execution
*   Command & state generation engine
*   Extendable with custom device logic

### Run a Program

```ts
const runner = new ProgramRunner()
	.setCommander(commander)
	.setReferenceManager(referenceManager)
	.parseProgram(program);

const { commands, toUpdate } = await runner.run();
```

### Testing

`npm run test`

Related Links
-------------
*   [Pocketix GitHub Org](https://github.com/pocketix)
*   [Node Core for IoT](https://github.com/pocketix/pocketix-node-core)

Contributing & License
----------------------

All Pocketix V1 components are open-source under the MIT License. Contributions are warmly welcomed via pull requests on GitHub.