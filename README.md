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

# for better compiler support and to ensure the size of MyEnum use NS_ENUM

``` objective-c
tydef NS_ENUM(NSUInteger, MyEnum) {
  MyEnumValueA,
  MyEnumValueB,
  MyEnumvalueC,
}
```

# for better compiler support and to ensure the size of MyEnum use NS_ENUM


``` objective-c
tydef NS_ENUM(NSUInteger, MyEnum) {
  MyEnumValueA = 0,
  MyEnumValueB = 5,
  MyEnumvalueC = 10,
}
```

# for better compiler support and to ensure the size of MyEnum use NS_ENUM


``` objective-c
tydef NS_ENUM(NSUInteger, MyEnum) {
  MyEnumValueA = 0,
  MyEnumValueB,
  MyEnumvalueC
}
```

# for better compiler support and to ensure the size of MyEnum use NS_ENUM

``` objective-c
typedef NS_ENUM(NSUInteger, PlayerState) {
  playerStateOff,
  playerStatePlaying,
  playerStatePause
};
```

``` objective-c
MyEnum enumVar = MyEnumValueA;
```

# Example of an Enumeration 

``` objective-c
//
//  AppDelegate.m
//  DefiningAnEnum_ObjectiveC
//
//  Created by Carlos Santiago Cruz on 8/15/19.
//  Copyright © 2019 Carlos Santiago Cruz. All rights reserved.
//

#import "AppDelegate.h"
#import "ViewController.h"

@interface AppDelegate ()
{
    ViewController *viewController;
}
@end

@implementation AppDelegate


- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
    self.window = [[UIWindow alloc] initWithFrame:[[UIScreen mainScreen] bounds]];
    viewController = [[ViewController alloc] initWithNibName:@"ViewController" bundle:nil];
    self.window.rootViewController = viewController;
    [self.window makeKeyAndVisible];
    return YES;
}


- (void)applicationWillResignActive:(UIApplication *)application {
    // Sent when the application is about to move from active to inactive state. This can occur for certain types of temporary interruptions (such as an incoming phone call or SMS message) or when the user quits the application and it begins the transition to the background state.
    // Use this method to pause ongoing tasks, disable timers, and invalidate graphics rendering callbacks. Games should use this method to pause the game.
}


- (void)applicationDidEnterBackground:(UIApplication *)application {
    // Use this method to release shared resources, save user data, invalidate timers, and store enough application state information to restore your application to its current state in case it is terminated later.
    // If your application supports background execution, this method is called instead of applicationWillTerminate: when the user quits.
}


- (void)applicationWillEnterForeground:(UIApplication *)application {
    // Called as part of the transition from the background to the active state; here you can undo many of the changes made on entering the background.
}


- (void)applicationDidBecomeActive:(UIApplication *)application {
    // Restart any tasks that were paused (or not yet started) while the application was inactive. If the application was previously in the background, optionally refresh the user interface.
}


- (void)applicationWillTerminate:(UIApplication *)application {
    // Called when the application is about to terminate. Save data if appropriate. See also applicationDidEnterBackground:.
}


@end
```

# declare the enum in h file.

``` objective-c
//
//  ViewController.h
//  DefiningAnEnum_ObjectiveC
//
//  Created by Carlos Santiago Cruz on 8/15/19.
//  Copyright © 2019 Carlos Santiago Cruz. All rights reserved.
//

#import <UIKit/UIKit.h>

typedef NS_ENUM(NSUInteger, PlayerState) {
    playerStateOff,
    playerStatePlaying,
    playerStatePause
};

@interface ViewController : UIViewController


@end
```

# Use the enumeration in m file.

``` objective-c
//
//  ViewController.m
//  DefiningAnEnum_ObjectiveC
//
//  Created by Carlos Santiago Cruz on 8/15/19.
//  Copyright © 2019 Carlos Santiago Cruz. All rights reserved.
//

#import "ViewController.h"

@interface ViewController ()

@end

@implementation ViewController

- (void)viewDidLoad {
    [super viewDidLoad];
    
    PlayerState playerState = playerStateOff;
    
    switch (playerState) {
        case playerStateOff:
            NSLog(@"The player state is off");
            break;
        case playerStatePause:
            NSLog(@"The player state is pause");
        case playerStatePlaying:
            NSLog(@"The player state is playing");
        default:
            break;
    }
    
    // Now use it with a method
    [self checkAvailability:playerState];
    
}

-(void)checkAvailability:(PlayerState)playerState
{
    switch (playerState) {
        case playerStateOff:
            NSLog(@"The player state is off");
            break;
        case playerStatePause:
            NSLog(@"The player state is pause");
        case playerStatePlaying:
            NSLog(@"The player state is playing");
        default:
            break;
    }
}

@end
```

# This is what the console retrieves

``` console
2019-08-15 21:41:38.225761-0500 DefiningAnEnum_ObjectiveC[12862:922139] The player state is off
2019-08-15 21:41:38.225973-0500 DefiningAnEnum_ObjectiveC[12862:922139] The player state is off
```





