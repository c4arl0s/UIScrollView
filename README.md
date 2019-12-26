# UIScrollView
A brief Overview

![Sin título 2](https://user-images.githubusercontent.com/24994818/71460714-b1257b00-2772-11ea-8235-ea0c4af9e2ed.jpg)

![Sin título 1](https://user-images.githubusercontent.com/24994818/71460651-5ee45a00-2772-11ea-9179-8e952ae34522.jpg)

```objective-c
//
//  ViewController.m
//  CatUIScrollView
//
//  Created by Carlos Santiago Cruz on 24/12/19.
//  Copyright © 2019 Carlos Santiago Cruz. All rights reserved.
//

#import "ViewController.h"

@interface ViewController ()

@end

@implementation ViewController

- (void)viewDidLoad {
    [super viewDidLoad];
    
    // create an image to display.
    // drag and drop and image to Assets.
    UIImage *image = [UIImage imageNamed:@"cat.jpeg"];
    
    // create and image view to display
    UIImageView *imageView = [[UIImageView alloc] initWithImage:image];
    imageView.frame = CGRectMake(0, 0, image.size.width, image.size.height);
    
    // create an scrollview object
    // scrollview's frame has to be equal to view's bounds
    UIScrollView *scrollView = [[UIScrollView alloc] initWithFrame:self.view.bounds];
    
    // make the scrollView intance scroll - Pretty important !
    scrollView.contentSize = image.size;
    
    // get rotation
    scrollView.autoresizingMask = UIViewAutoresizingFlexibleWidth | UIViewAutoresizingFlexibleHeight;
    
    // set up view hierarchy
    [scrollView addSubview:imageView];
    [self.view addSubview:scrollView];
}


@end
```



