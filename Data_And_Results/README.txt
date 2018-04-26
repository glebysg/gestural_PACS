Parameters:
    Number of commands = 34
    Number of semantic descriptors = 55
    Number of subjects = 9

Files:
    1. 'command_names.xlsx'
        * This file contains the command ids and the names of the 34 commands
    2. 'semantic_descriptors.xlsx'
        * This file contains the descriptor ids and the names of the 55 semantic descriptors
    3. 'semantic_description_matrix.mat'
        * This mat file contains three variables:
            I. 'context_modifier_sd_matrix': A three dimensional (34 x 55 x 9) matrix.
                Each row is a combined semantic description of both the context and the modifier gesture.
                (i, j, k) corresponds to the ith command, jth semantic descriptor and kth subject
            II. 'context_sd_matrix': A three dimensional (34 x 55 x 9) matrix.
                Each row is a semantic description of the context of the gesture.
                (i, j, k) corresponds to the ith command, jth semantic descriptor and kth subject
            III. 'modifier_sd_matrix': A three dimensional (34 x 55 x 9) matrix.
                Each row is a semantic description of the modifier of the gesture.
                (i, j, k) corresponds to the ith command, jth semantic descriptor and kth subject
    4. 'results.mat'
        * This mat file contains five variables:
            I. 'level_of_agreement_soa': Agreement values computed using the state of the art
                method. It is a two dimensional matrix (34 x 3), where rows correspond
                to number of commands and columns correspond to the three
                conditions (context, modifier, context+modifier)
            II. 'mean_level_of_agreement_soa' = mean(level_of_agreement_soa, 1)
            III. 'std_level_of_agreement_soa' = std(level_of_agreement_soa, 1)
            IV. 'level_of_agreement_sd': Agreement values computed using the semantic descriptors
                method. It is a two dimensional matrix (34 x 3), where rows correspond
                to number of commands and columns correspond to the three
                conditions (context, modifier, context+modifier)
            V. 'mean_level_of_agreement_sd' = mean(level_of_agreement_sd, 1)
            VI. 'std_level_of_agreement_sd' = std(level_of_agreement_sd, 1)

    5. 'mwwtest_results.txt'
        * This file has the statistical results obtained from the Mann Whittney Wilcoxon test.
        * It contains three tests: context, modifier and context+modifier cases. The comparison is performed between the existing metrics and the proposed metric.

    6. 'ttest_results.txt'
        * This file has the statistical results obtained from the t-test.
        * It contains three tests: context, modifier and context+modifier cases. The comparison is performed between the existing metrics and the proposed metric.
