bool isPalindrome(char* s) {
    int len = strlen(s);
    char* new = (char*)malloc(len + 1);
    int idx = 0;
    for (int i = 0; i < len; i++) {
        if (isalnum(s[i])) {
            new[idx++] = tolower(s[i]);
        }
    }
    new[idx] = '\0';
    for (int i = 0, j = idx - 1; i < j; i++, j--) {
        if (new[i] != new[j]) {
            free(new);
            return false;
        }
    }
    free(new);
    return true;
}
