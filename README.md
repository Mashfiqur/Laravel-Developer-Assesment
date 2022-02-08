## Introduction

Our project goal is to make a simple form builder package, which will have only four types of input: (i) text, (ii)Checkbox, (iii)radio, (iv) dropdown. Your package must be able to pass style(s), value(s) and type to the helpers.

If you don't understand instruction, please contact this email `mashfiqur@shapla.io` and follow example section.

## We Love

1. Clean code
2. Easy to understand codebase
3. Proper git usage
4. Clear and easily understandable commit messages
5. To answer any question you have

## Form Builder

### Instructions

1. It should be able to run on laravel 5.3 to 8
2. Create meaningful name for the package and file structure
3. Upload your package to git and packagist
4. Create documentation
5. Sample code for its usage

### Deliverable

Codebase should be in a git based repository (Github, Bitbucket, Gitlab etc.).

### Submission

Write an email to `mashfiqur@shapla.io` and cc `tasnim@shapla.io` with your deliverables and request for a code review. Mention
that you were asked to complete this and seek information about the next step for you.

## Helper

### Step by Step Work Breakdown

1. Install Laravel
2. Create a Folder Structure
3. Create the Composer File
4. Load the Package from the Main Composer.JSON File
5. Create a Service Provider for Package
6. Create the Views
7. Update the Service Provider to Load the Package
8. Update the Composer File

### Data Passing and tag usage

This section is to help you understand how the data should be passed to the helpers and how the helpers will be used.

##### Input tag:

We will be using this template as follows

```
@include(“path.file-name”, [“data” => $data])
```

Where data is a key value array in the following structure:

```
$data = [
    “ids” => [“id1”],
    “classes => [“class1”, “class2”, … “classN”],
    “type” => “type”,
    “name” => “name”,
    “values” => [
        “prev_value” => “value” //(this is the previous posted value)
    ],
    “required” => true/false
];
```

##### Select tag:

We will be using this template as follows

```
@include(“path.file-name”, [“data” => $data])
```

Where data is a key value array in the following structure:

```
$data = [
    “ids” => [“id1”],
    “classes => [“class1”, “class2”, … “classN”],
    “name” => “name”,
    “values” => [
        “value1” => “value1_name”,
        “value2” => “value2_name”,
        …
         “valueN” => “valueN_name”
    ],
    “active” => “valueX” or “null”,
    “required” => true/false
];
```

In the case of the active value being “null”, a default value has to be generated and put at the top of the options list, otherwise the “active” value is to be placed at the top of the options list.

##### Radio

We will be using this template as follows

```
@include(“path.file-name”, [“data” => $data])
```

Where data is a key value array in the following structure:

```
$data = [
    “ids” => [“id1”],
    “classes => [“class1”, “class2”, … “classN”],
    “name” => “name”,
    “values” => [
        “value1” => “value1_name”,
        “value2” => “value2_name”,
        …
         “valueN” => “valueN_name”
    ],
    “active” => “valueX” or “null”,
    “required” => true/false
];
```

In the case of the active value not being “null”, the active value has to be selected.

##### Checkbox

We will be using this template as follows

```
@include(“path.file-name”, [“data” => $data])
```

Where data is a key value array in the following structure:

```
$data = [
    “ids” => [“id1”],
    “classes => [“class1”, “class2”, … “classN”],
    “name” => “name”,
    “values” => [
        “value1” => “value1_name”,
        “value2” => “value2_name”,
        …
         “valueN” => “valueN_name”
    ],
    “required” => true/false
];
```
