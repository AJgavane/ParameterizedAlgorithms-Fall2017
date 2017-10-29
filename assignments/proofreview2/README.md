# Proof Review Exercise 2

## Getting started
Pull and compile this assignment (you can use `make`!). It's the standard homework template, so there should not be any issues. However, feel free to post in the `#latex` channel if you encounter any problems!

## Grading the proofs

Unlike the first proof review exercise, in this one all algorithms and proofs _should_ (see note below) be correct...but not for the theorem claimed. So your goal for this proof review is to find the technical error, identify it, and salvage as much of the existing work as possible:

1. Find a contradiction between the claim made (the theorem statement) and the algorithm/proof provided. Concretely state the contradiction and where it occurs. (Tip: Providing a counterexample graph is a great way to do this succinctly and concretely).

2. Provide a fix by adjusting the _claim_, not the proof. You can adjust the claim by changing the problem that's being solved, or requiring a more specific input, etc. Ask on Slack if you're not sure what's fair game or not.

3. Provide an example for why your fix seems "maximal." By maximal, we mean that you should make an honest attempt to salvage as much of the original theorem as possible. You can claim "This algorithm works if we only run it on graphs with no edges," and you might be right, but that's boring if the algorithm also works on all trees! So provide some justification for why your fix can't be extended in any obvious direction.

4. Finally, like the first proof review exercise, provide comments on the writing clarity of the proof. If you think that something could be improved, provide the correction! Make your comments as constructive as possible.

_Note: If you think that a proof is fatally broken, please post in `#problem-discussion` in Slack and tag the TA._

Provide your feedback as `proof_review.pdf` in the `Week-11` folder.

**CSC791 students**: There is no additional work for you on this assignment!

## Tips

1. There is no need to grade or modify the background information. A proof sketch is provided as background information in Attempt \#1, and it's more brief than usual. The lemma is correct, and the proof sketch is for interested readers.

2. Try to be succinct in identifying the problematic claim. Probe out _exactly_ what goes wrong, both in the claim and where a bad assumption or two is made in the proof.
