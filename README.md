# SAT-solving-many-to-many-matching

This github page contains the code, data sets and results of an experiment that was done for a bachelor AI thesis for the University of Amsterdam.
For questions about this thesis or any other questions, you can contact me using this email: svonkuvathesis@gmail.com.

The abstract of the thesis is the following:

In this thesis, the possibility of solving many-to many matching problems with 
two-sided preference using satisfiability solving will be investigated. First, there 
was done theorethical research into matching problems and SAT solving. After this,
an experiment was conducted. For the experiment, five data sets were used, that
contain bidding data of reviewers on submissions they could review. Using python
and the z3 library in specific, logical rules were set up to translate this problem
into a SAT problem. These rules were then combined with a variable bid score
distribution to represent yes, maybe and no bids from the data. Furthermore,
the cardinality in the form of a maximum number of submissions per reviewer
was added. The logical rules and variable values were then used to calculate a
model of matches for each of the files using the z3 SAT algorithm, where the
total bid score for matches was optimised. Using the social welfare score of the
matches, together with some other values like the computed equity and algorithm
running time, the created models were evaluated. There was found that SAT
can be a satisfying approach for solving this type of problem, but the success
rate highly depends on the properties of the data set. The size of a data set
strongly impacted the algorithm running time, which highly limits the fitness of
SAT for finding matches for large data sets. Also, properties like the ratio between
reviewers and submissions for different data sets, impact the number of reviews
each submissions gets for an equally set maximum number of submissions per
reviewer. Consequently, this makes it very difficult to find a good balance in
cardinality for reviewers and submissions for some files. Another property that
influences the matching quality is the ratio of yes bids in a file. Because of all these
different factors, it is difficult to answer the main question of this thesis; How to
find high quality matchings for many-to-many two-sided matching problems using
satisfiability solving? Nevertheless, high quality matchings can be found using
SAT, although the time it takes to find a solution increases exponentially with the
number of rows a data set contains.
