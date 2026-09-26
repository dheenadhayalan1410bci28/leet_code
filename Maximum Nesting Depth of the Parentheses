int maxDepth(char* s) {
    int count = 0, max = 0;
    for (int i = 0; s[i] != '\0'; i++) {
        if (s[i] == '(') 
            count++;
        max = (count > max) ? count : max;
        if (s[i] == ')') 
            count--;
    }
    return max;
}
