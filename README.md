# task-9
#include <iostream>

using namespace std;

{
    for (int i = 0; i < rows; ++i) {
        for (int j = 0; j < cols; ++j) {
            cout << m[i][j];
            if (j < cols - 1) {
                cout << " ";
            }
        }
        cout << "\n";
    }
}

{
    for (int i = 0; i < rows; ++i) {
        for (int j = 0; j < cols; ++j) {
            dst[j][i] = src[i][j];
        }
    }
}

int main() {
    ios_base::sync_with_stdio(false);
    cin.tie(NULL);

    int r, c;
    if (!(cin >> r >> c)) return 0;

    int m[10][10];
    for (int i = 0; i < r; ++i) {
        for (int j = 0; j < c; ++j) {
            cin >> m[i][j];
        }
    }

    cout << "ryadky";
    for (int i = 0; i < r; ++i) {
        int row_sum = 0;
        for (int j = 0; j < c; ++j) {
            row_sum += m[i][j];
        }
        cout << " " << row_sum;
    }
    cout << "\n";

    cout << "stovptsi";
    for (int j = 0; j < c; ++j) {
        int col_sum = 0;
        for (int i = 0; i < r; ++i) {
            col_sum += m[i][j];
        }
        cout << " " << col_sum;
    }
    cout << "\n";

    int t[10][10];
    transpose(m, t, r, c);

    cout << "transponovana\n";

    return 0;
}
