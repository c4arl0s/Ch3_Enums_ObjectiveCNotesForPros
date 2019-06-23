# Ch3_Enums_ObjectiveCNotesForPros
Ch3_Enums_ObjectiveCNotesForPros

``` objective-c
typedef enum {
  Monday = 1,
  Tuesday,
  Wednesday
} WORKDAYS;

WORKDAYS today = Monday; //value 1
```

# defining an enum

for better compiler support and to ensure the size of MyEnum use NS_ENUM

``` objective-c
tydef NS_ENUM(NSUInteger, MyEnum) {
  MyEnumValueA,
  MyEnumValueB,
  MyEnumvalueC,
}
```

for better compiler support and to ensure the size of MyEnum use NS_ENUM


``` objective-c
tydef NS_ENUM(NSUInteger, MyEnum) {
  MyEnumValueA = 0,
  MyEnumValueB = 5,
  MyEnumvalueC = 10,
}
```
for better compiler support and to ensure the size of MyEnum use NS_ENUM


``` objective-c
tydef NS_ENUM(NSUInteger, MyEnum) {
  MyEnumValueA = 0,
  MyEnumValueB,
  MyEnumvalueC
}
```

for better compiler support and to ensure the size of MyEnum use NS_ENUM

typedef NS_ENUM(NSUInteger, PlayerState) {
  playerStateOff,
  playerStatePlaying,
  playerStatePause
};

``` objective-c
MyEnum enumVar = MyEnumValueA;
```



