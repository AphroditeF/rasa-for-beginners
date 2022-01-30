Making a chatbot using Rasa

I follow the course "Rasa for Beginners" from Udemy https://www.udemy.com/course/rasa-for-beginners .



Differences from tutorial and "reality".

1) nlu.md / nlu.yml
code format 
## intent:ask_lower_stress
- What do I do if I'm too stressed?
---------------------------------------------
- intent: ask_lower_stress
  examples: |
    - What do I do if I'm too stressed?



2) stories.md/stories.yml
## ask diet questions
* ask_eat_healthy
  - utter_diet_info
---------------------------------------------
- story: ask diet questions
  steps:
  - intent: ask_eat_healthy
  - action: utter_diet_info

3) Rasa interactive writes stories on stories.yml (there is no stories.md)


4) Course Video: 5 Forms


  - story: survey happy path
    steps:
    - intent: greet
    - action: utter_greet
    - intent: affirm
    - action: health_form
    - active_loop: health_form

--------------------------------------------
????????????????????????????????
* affirm
- health_form
- form{"name":"health_form"}
- form{"name":null}

https://rasa.com/docs/rasa/playground/ 3. Stories