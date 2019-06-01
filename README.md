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

``` objective-c
tydef NS_ENUM(NSUInteger, MyEnum) {
  MyEnumValueA,
  MyEnumValueB,
  MyEnumvalueC,
}
```

``` objective-c
tydef NS_ENUM(NSUInteger, MyEnum) {
  MyEnumValueA = 0,
  MyEnumValueB = 5,
  MyEnumvalueC = 10,
}
```

``` objective-c
tydef NS_ENUM(NSUInteger, MyEnum) {
  MyEnumValueA = 0,
  MyEnumValueB,
  MyEnumvalueC
}
```

``` objective-c
MyEnum enumVar = MyEnumValueA;
```



