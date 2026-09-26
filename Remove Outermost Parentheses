
char* removeOuterParentheses(char* s) {
    int n = strlen(s);
    char* result = (char*)malloc(n + 1);
    int idx = 0, count = 0;

    for (int i = 0; i < n; i++) {
        if (s[i] == '(') {
            if (count > 0)
                result[idx++] = s[i];
            count++;
        } else {
            count--;
            if (count > 0)
                result[idx++] = s[i];
        }
    }
    result[idx] = '\0';
    return result;
}
