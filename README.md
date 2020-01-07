# UIScrollView
A brief Overview

![Screen Shot 2020-01-07 at 13 03 16](https://user-images.githubusercontent.com/24994818/71921261-23706500-314e-11ea-83ad-502d5e515651.png)
![Nueva nota 2](https://user-images.githubusercontent.com/24994818/71921082-bceb4700-314d-11ea-9c12-5a73264dab27.png)

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

![Screen Shot 2019-12-26 at 0 05 41](https://user-images.githubusercontent.com/24994818/71460927-7bcd5d00-2773-11ea-93c6-6f8bed045ebc.png)

