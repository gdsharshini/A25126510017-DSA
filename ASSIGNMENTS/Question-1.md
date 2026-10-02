#include <stdio.h>
int main() {
    int n, i, key;
    int low, high, mid;
    int comparisons = 0, found = 0;
    printf("Enter number of employees: ");
    scanf("%d", &n);
    int ids[n];
    printf("Enter %d employee IDs in ascending order:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", &ids[i]);
    }
    printf("Enter the employee ID to search: ");
    scanf("%d", &key);
    low = 0;
    high = n - 1;
    while (low <= high) {
        mid = (low + high) / 2;
        comparisons++;
        if (ids[mid] == key) {
            printf("Employee ID %d found at position %d (index %d)\n",
                   key, mid + 1, mid);
            found = 1;
            break;
        } else if (key < ids[mid]) {
            high = mid - 1;
        } else {
            low = mid + 1;
        }
    }
    if (!found) {
        printf("Employee ID %d not found in the list.\n", key);
    }
    printf("Number of comparisons: %d\n", comparisons);
    return 0;
}


<img width="428" height="183" alt="image" src="https://github.com/user-attachments/assets/84bc66ca-cc83-475a-8eb9-66de571cddc8" />
<img width="401" height="171" alt="dsa1 2" src="https://github.com/user-attachments/assets/56249485-f21b-45e8-a5fe-cd158637ce0a" />

