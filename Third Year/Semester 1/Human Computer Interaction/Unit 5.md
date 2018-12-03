# Human Computer Interaction

## Unit 5: HCI - Design Rules, Guidelines and Evaluation Techniques

### Principles that affect Usability
- The principles to support usability are divided into 3 general categories.
	1. **Learnability:** The ease with which new users can begin effective interaction and achieve maximal performance.
	2. **Flexibility:** The multiplicity of ways in which the user and system exchange information.
	3. **Robustness:** The level of support provided to the user in determining successful achievement and assessment of goals.
- Each of these categories is subdivided into more specific principles as follows.
	1. Principles affecting learnability -
		1. **Predictability:** Support for the user to determine the effect of future action based on past interaction history.
		2. **Synthesizability:** Support for the user to assess the effect of past operations on the current state.
		3. **Familiarity:** The extent to which a user’s knowledge and experience in other real-world or computer-based domains can be applied when interacting with a new system.
		4. **Generalisability:** Support for the user to extend knowledge of specific interaction within and across applications to other similar situations.
		5. **Consistency:** Likeness in input–output behaviour arising from similar situations or similar task objectives.
	2. Principles affecting flexibility -
		1. **Dialog Initiative:** Allowing the user freedom from artificial constraints on the input dialog imposed by the system.
		2. **Multithreading:** Ability of the system to support user interaction pertaining to more than one task at a time.
		3. **Task Migratability:** The ability to pass control for the execution of a given task so that it becomes either internalised by the user or the system or shared between them.
		4. **Substitutivity:** Allowing equivalent values of input and output to be arbitrarily substituted for each other.
		5. **Customisability:** Modifiability of the user interface by the user or the system.
	3. Principles affecting robustness -
		1. **Observability:** Ability of the user to evaluate the internal state of the system from its perceivable representation.
		2. **Recoverability:** Ability of the user to take corrective action once an error has been recognised.
		3. **Responsiveness:** How the user perceives the rate of communication with the system.
		4. **Task Conformance:** The degree to which the system services support all of the tasks the user wishes to perform and in the way that the user understands them.

### Golden Rules (Ben Shneiderman)
1. **Strive for consistency** by utilising familiar icons, colours, menu hierarchy, call-to-actions, and user flows when designing similar situations and sequence of actions.
2. **Enable frequent users to use shortcuts.** With increased use comes the demand for quicker methods of completing tasks. As the users becomes more experienced, they can navigate and operate the interface more quickly and efficiently.
3. **Offer informative feedback.** The user should know where they are at and what is going on at all times. For every action there should be appropriate, human-readable feedback within a reasonable amount of time.
4. **Design dialogue to yield closure.** Don’t keep your users guessing. Tell them what their action has led them to.
5. **Offer simple error handling.** Systems should be designed to be as fool-proof as possible, but when unavoidable errors occur, ensure users are provided with simple, intuitive step-by-step instructions to solve the problem as quickly and painlessly as possible.
6. **Permit easy reversal of actions.** Designers should aim to offer users obvious ways to reverse their actions. This feature relieves anxiety, since the user knows that errors can be undone; it thus encourages exploration of unfamiliar options.
7. **Support internal locus of control.** Allow your users to be the initiators of actions. Give users the sense that they are in full control of events occurring in the digital space.
8. **Reduce short-term memory load.** Human attention is limited and we are only capable of maintaining around five items in our short-term memory at one time. Therefore, interfaces should be as simple as possible with proper information hierarchy, and choosing recognition over recall.

### Heuristics (Jakob Nielsen)
1. **Visibility of system status.** The system should always keep users informed about what is going on, through appropriate feedback within reasonable time.
2. **Match between system and the real world.** The system should speak the users' language, with words, phrases and concepts familiar to the user, rather than system-oriented terms.
3. **User control and freedom.** Users often choose system functions by mistake and will need a clearly marked "emergency exit" to leave the unwanted state without having to go through an extended dialogue. Support undo and redo.
4. **Consistency and standards.** Users should not have to wonder whether different words, situations, or actions mean the same thing. Follow platform conventions.
5. **Error prevention.** Even better than good error messages is a careful design which prevents a problem from occurring in the first place.
6. **Recognition rather than recall.** Minimise the user's memory load by making objects, actions, and options visible. The user should not have to remember information from one part of the dialogue to another.
7. **Flexibility and efficiency of use.** Accelerators - unseen by the novice user - may often speed up the interaction for the expert user such that the system can cater to both inexperienced and experienced users.
8. **Aesthetic and minimalist design.** Dialogues should not contain information which is irrelevant or rarely needed.
9. **Help users recognise, diagnose, and recover from errors.** Error messages should be expressed in plain language (no codes), precisely indicate the problem, and constructively suggest a solution.
10. **Help and documentation.** Even though it is better if the system can be used without documentation, it may be necessary to provide help and documentation.

### User Interface Management System (UIMS)
- A UIMS (User Interface Management System) should not be thought of as a system but rather a software architecture (a UIMS is also called a User Interface Architecture) in which the implementation of an application's user interface is clearly separated from that of the application's underlying functionality.
- A large number of software architectures are based on the assumption that the functionality and the user interface of a software application are two separate concerns that can be dealt with in isolation.
- The objective of such a separation is to increase the ease of maintainability and adaptability of the software. Also, by abstracting the code generating the user interface from the rest of the application's logic or semantics, customisation of the interface is better supported.
- Such user interface architectures have been proven useful but also introduce problems. In systems with a high degree of interaction and semantic feedback (e.g. in direct manipulation interfaces) the boundary between application and user interface is difficult or impossible to maintain.
- Some examples of such architectures are Model-View-Controller, the linguistic model, the Seeheim model, the Higgins UIMS, and the Arch model (a specialisation of the Seeheim model).

### Goals of Evaluation
- Evaluation has three main goals:
	1. To assess the extent and accessibility of the system’s functionality.
		- The system’s functionality is important in that it must accord with the user’s requirements.
		- This includes not only making the appropriate functionality available within the system, but making it clearly reachable by the user in terms of the actions that the user needs to take to perform the task.
		- It also involves matching the use of the system to the user’s expectations of the task.
		- Evaluation at this level may also include measuring the user’s performance with the system, to assess the effectiveness of the system in supporting the task.
	2. To assess users’ experience of the interaction.
		- In addition to evaluating the system design in terms of its functional capabilities, it is important to assess the user’s experience of the interaction and its impact upon him.
		- This includes considering aspects such as how easy the system is to learn, its usability and the user’s satisfaction with it.
		- It may also include his enjoyment and emotional response.
	3. To identify any specific problems with the system.
		- The final goal of evaluation is to identify specific problems with the design.
		- These may be aspects of the design which, when used in their intended context, cause unexpected results, or confusion amongst users.

### Evaluation through Expert Analysis

- It can be expensive to carry out user testing at regular intervals during the design process, and it can be difficult to get an accurate assessment of the experience of interaction from incomplete designs and prototypes.
- Consequently, a number of methods have been proposed to evaluate interactive systems through expert analysis. These depend upon the designer, or a human factors expert, taking the design and assessing the impact that it will have upon a typical user.
- The basic intention is to identify any areas that are likely to cause difficulties because they violate known cognitive principles, or ignore accepted empirical results.
- These methods can be used at any stage in the development process from a design specification, through storyboards and prototypes, to full implementations, making them flexible evaluation approaches. They are also relatively cheap, since they do not require user involvement.
- However, they do not assess actual use of the system, only whether or not a system upholds accepted usability principles.
- There are four approaches to expert analysis: cognitive walkthrough, heuristic evaluation, the use of models and use of previous work.

### Cognitive Walkthrough

- The origin of the cognitive walkthrough approach to evaluation is the code walkthrough familiar in software engineering. Walkthroughs require a detailed review of a sequence of actions.
- In the cognitive walkthrough, the sequence of actions refers to the steps that an interface will require a user to perform in order to accomplish some known task. The evaluators then ‘step through’ that action sequence to check it for potential usability problems.
- Usually, the main focus of the cognitive walkthrough is to establish how easy a system is to learn.
- Experience shows that many users prefer to learn how to use a system by exploring its functionality hands on, and not after sufficient training or examination of a user’s manual. Hence, the focus is on learning through exploration. To do this, the evaluators go through each step in the task and provide a ‘story’ about why that step is or is not good for a new user.
- To perform a cognitive walkthrough, four things are needed:
  1. A specification or prototype of the system (not necessarily complete).
  2. A description of the task the user is to perform on the system.
  3. A complete, written list of the actions needed to complete the task with the proposed system.
  4. An indication of who the users are and what kind of experience and knowledge the evaluators can assume about them.
- For each action, the evaluators try to answer the following four questions:
  1. Is the effect of the action the same as the user’s goal at that point?
  2. Will users see that the action is available?
  3. Once users have found the correct action, will they know it is the one they need?
  4. After the action is taken, will users understand the feedback they get?

### Heuristic Evaluation
- Heuristic evaluation is a method for structuring the critique of a system using a set of relatively simple and general heuristics. Heuristic evaluation can be performed on a design specification so it is useful for evaluating early design. But it can also be used on prototypes, storyboards and fully functioning systems. It is therefore a flexible, relatively cheap approach.
- The general idea behind heuristic evaluation is that several evaluators independently critique a system to come up with potential usability problems. It is important that there be several of these evaluators and that the evaluations be done independently.
- To aid the evaluators in discovering usability problems, a set of 10 heuristics are provided by Jakob Nielsen.
- *Nielsen’s heuristics. Points only. No explanation, or else it becomes extremely long.*
- Each evaluator assesses the system and notes violations of any of these heuristics that would indicate a potential usability problem. The evaluator also assesses the severity of each usability problem, based on four factors:
	1. How common is the problem?
	2. How easy is it for the user to overcome?
	3. Will it be a one-off problem or a persistent one?
	4. How seriously will the problem be perceived?
- Once each evaluator has completed their separate assessment, all of the problems are collected. The design team will then determine the ones that are the most important and will receive attention first.

### Model-based Evaluation
- A third expert-based approach is the use of models. Certain cognitive and design models provide a means of combining design specification and evaluation into the same framework.
- For example, the GOMS (goals, operators, methods and selection) model predicts user performance with a particular interface and can be used to filter particular design options.
- Similarly, lower-level modelling techniques provide predictions of the time users will take to perform low-level physical tasks.
- Design methodologies, such as design rationale, also have a role to play in evaluation at the design stage. Design rationale provides a framework in which design options can be evaluated. By examining the criteria that are associated with each option in the design, and the evidence that is provided to support these criteria, informed judgments can be made in the design.
- Dialog models can also be used to evaluate dialog sequences for problems, such as unreachable states, circular dialogs and complexity. Models such as state transition networks are useful for evaluating dialog designs prior to implementation.

### Evaluation through User Participation
- Although evaluation by expert analysis is useful for filtering and refining the design, it is not a replacement for actual testing with the people for whom the system is intended: the users.
- There are a number of different approaches to evaluation through user participation. These include experimental methods, observational methods, query techniques, and methods that use physiological monitoring.
- User participation in evaluation tends to occur in the later stages of development when there is at least a working prototype of the system in place. This may range from a simulation of the system’s interactive capabilities without its underlying functionality, through a basic functional prototype to a fully implemented system.
- There are two distinct evaluation styles:
  1. Laboratory studies:
    - In this type of evaluation studies, users are taken out of their normal work environment to take part in controlled tests, often in a specialist usability laboratory.
    - This approach has a number of benefits and disadvantages.
    	- A laboratory may contain sophisticated equipment which cannot be replicated in the work environment. In addition, the participant operates in an interruption-free environment.
    	- However, the lack of context – for example, filing cabinets, wall calendars, books or interruptions – and the unnatural situation may mean that one records a situation that never arises in the real world.
    - There are, some situations where laboratory observation is the only option. For example, if the system is to be located in a dangerous or remote location, such as a space station.
  2. Field studies:
    - The second type of evaluation takes the designer or evaluator out into the user’s work environment in order to observe the system in action.
    - Again this approach has its pros and cons.
      - High levels of ambient noise, greater levels of movement and constant interruptions, all make field observation difficult.
      - However, the very 'open' nature of the situation means that you will observe interactions that would have been missed in a laboratory study.

### Choosing an Evaluation Technique
- A range of techniques is available for evaluating an interactive system at all stages in the design process. So how do we decide which methods are most appropriate for our needs?
- There are no hard and fast rules in this – each method has its particular strengths and weaknesses and each is useful if applied appropriately.
- However, there are a number of factors that should be taken into account when selecting evaluation techniques. These also provide a way of categorising the different methods so that we can compare and choose between them.
- We can identify at least eight factors that distinguish different evaluation techniques and therefore help us to make an appropriate choice. These are:
	1. The stage in the cycle at which the evaluation is carried out.
	2. The style of evaluation.
	3. The level of subjectivity or objectivity of the technique.
	4. The type of measures provided.
	5. The information provided.
	6. The immediacy of the response.
	7. The level of interference implied.
	8. The resources required.