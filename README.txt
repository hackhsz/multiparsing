This is the implementation of Dependency Parsing algorithm, which describes the relation between different part of speech in a sentence. For example, a noun can be really far away from its main structure, but it is still possible that these two are linked. 



QUESTION 1
	 PART B:By Definition, dependency graph is projective if it could be drawn without any crossing arrows. A dependency graph is non-projective if it has any crossing links. Non-projective dependency is associated with topicalization and extraposition explained in provideddata file. Therefore, for any i positions between position a and b there can not have a parent/child of i outside a and b. 

	 PART C: projective: He goes to a party
	      	 non-projective: I got a girlfriend who is really kind but ugly

QUESTION 2

	 PART B: badfeatires.model

	 UAS:0.229038040231
	 LAS:0.125473013344

QUESTION 3

	 PART A:
	      For this question, I have only added corresponding features listed in the table,making sufficient improvements along the way

	      Lemma:
	      1,After implementing the first index of of the stack, function see if this token is an empty string. Then, append this tag with stack/buffer lemma
              2,O(n)
	      3,After adding LEMMA, UAS improved 0.0139 in average, LAS improved 0.0024 in average

	      Form:
	      1, I followed the idea in the provided code, and by the same logic,add form tag for buffer[0] and buffer[1]
	      2,O(n)
	      3, After adding FORM, UAS improved 0.015  in average, LAS improved 0.02  in average 

	      FEATS:
	      1, the same logic and implementation except for the name of the tag for above functions
	      2, O(n)
	      3, After adding FEATS, UAS improved 0.0003  in average, LAS improved 0.003   in average


	      POSTAG:
	      1, same 
	      2,O(n)
	      3, After adding POSTAG, UAS improved 0.15  in average, LAS improved 0.18  in average


	      
	       	 


	 PART D:
	      For the complexity of the arc-eager-shift-reduce parser,
	      functions with pre-conditions are O(n) such as left and reduce
	      Functions without pre-conditions are O(1))

	      Tradeoff: Although fast, using this algorithm would let to have sentence that are not projective to have inaccurate tags and misleading results because we presusmp they are all projective.


