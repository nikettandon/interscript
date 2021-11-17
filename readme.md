The Interscript dataset contains interactive user feedback on a T5 model generated script.

## Types of feedbacks:
- explicit feedback
  - (medium) localizing the node or edge and hoping the model will fix.
  - (easy) giving an edit and hoping the model will fix the graph.

- implicit feedback
  - (medium) feedback on why there is an error.
  - (hard) feedback on a general principle that the error causes to violate.

- distractor feedback 
  - (medium) top-3 feedback from lexically similar topic.
  - (easy) top-4 feedback from lexically similar topic.



## Sample entry from the file. There are a total of 8466 entries: 

```
 {
        "input_script": "push chair in -> pull chair in; pull chair in -> push chair against wall; push chair against wall -> straighten chair legs; straighten chair legs -> Push all chairs in; line up the chairs -> push chair in",
        "input_feedback": "One would not pull chair in if they had initially pushed it in.",
        "output_script": "push chair against wall -> straighten chair legs;straighten chair legs -> Push all chairs in;line up the chairs -> push chair in;push chair in -> push chair against wall",
        "metadata": {
            "id": "301KG0KX9BKTC0HB7Z9SV1Y5HAFH2Y.2_implicit.gp",
            "goal": "push all chairs in",
            "is_distractor": false,
            "feedback_type": "implicit.gp",
            "edit": "Remove node 'pull chair in'",
            "input_script_formatted": [
                "1. line up the chairs",
                "2. push chair in",
                "3. pull chair in",
                "4. push chair against wall",
                "5. straighten chair legs",
                "6. Push all chairs in"
            ],
            "output_script_formatted": [
                "1. line up the chairs",
                "2. push chair in",
                "3. push chair against wall",
                "4. straighten chair legs",
                "5. Push all chairs in"
            ]
        }
    }

```