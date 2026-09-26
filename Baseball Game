

int calPoints(char** operations, int operationsSize) {
    int score[operationsSize], j = 0, sum = 0;
    while (operationsSize--) {
        char c = **operations++;
        if (c == '+')
            score[j] = score[j - 1] + score[j - 2];
        else if (c == 'D')
            score[j] = score[j - 1] * 2;
        else if (c != 'C')
            score[j] = atoi(operations[-1]);
        sum += c == 'C' ? -score[--j] :  score[j++];
    }
    return sum;
}
