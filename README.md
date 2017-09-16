# anticode

```
int main()
{
    using namespace std;
    char ch;
    int count = 0;
    cout << "Enter characters; enter # to quit:\n";
    cin >> ch;
    while (ch != '#')
    {
        cout << ch;
        ++count;
        cin >> ch;
    }
    
    cout << endl << count << " characters read\n";
    return 0;
}
```
vs
```
int main()
{
    std::cout << "Enter characters; enter # to quit:\n";
    
    unsigned int count = 0;
    for (char ch; std::cin >> ch && ch != '#'; ++count) {
        std::cout << ch;
    }
    
    std::cout << std::endl << count << " characters read\n";
    
    return 0;
}
```
