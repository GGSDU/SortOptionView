# [SortOptionView](https://github.com/GGSDU/SortOptionView)

|Version|Commit Data|New In Version|
|---|---|---|
|1.0|2017.03.28|The first Version|
|1.1|2017.03.31|-imageShowStatusArrayForSortOptionView:|
|1.2|2017.07.13|-setCurrentSelectedItem:|

## Style
![guide](https://github.com/GGSDU/SortOptionView/blob/master/SortOptionView/SortOptionView/guide.gif)

## Usage

### 1.Init and Show
```
SortOptionView  *sortOptionView = [[SortOptionView alloc] init];
sortOptionView.dataSource = self;
sortOptionView.delegate = self;
[aSuperView addSubview: sortOptionView];
[sortOptionView show];
```
### 2. Implement the method of 'SortOptionViewDataSource' protocol

#### (1)Return the every button's title
```
- (NSArray *)titleArrayForSortOptionView:(SortOptionView *)sortOptionView
{
    return @[@"SortTitle1",@"SortTitle2",@"SortTitle3"];
}

```
#### (2)Return the every button's image show status to determine show the image or not
```
- (NSArray *)imageShowStatusArrayForSortOptionView:(SortOptionView *)sortOptionView
{
    return @[@"0",@"1",@"1"];
}
```

### 3.Implement the method of 'SortOptionViewDelegate' protocol
```
- (void)sortOptionView:(SortOptionView *)sortOptionView didClickedItemAtIndex:(NSUInteger)index sortOption:(SortOptionType)sortOption
{
    switch (sortOption) {
        case SortOptionNormal:
            NSLog(@"SortOptionNormal");
            break;
        case SortOptionUp:
            NSLog(@"SortOptionUp");
            break;
        case SortOptionDown:
            NSLog(@"SortOptionDown");
            break;
        default:
            break;
    }

    NSLog(@"index : %lu",index);

    // do something by judge the index and sortOption
}
```
### 4.Set default selected item
```
[sortOptionView setCurrentSelectedItem:0];
```

## Installation
1.**Run 'git clone'**

```
git clone https://github.com/GGSDU/SortOptionView
```

2.**Import the `SortOptionView` folder to your project.**

## Code with Us together
If you'd like to code with us and make the project better,contact me and join
 us.

- QQ : 337995545
- Email : story5@yeah.net
- [CSDN Blog](http://blog.csdn.net/story51314)
