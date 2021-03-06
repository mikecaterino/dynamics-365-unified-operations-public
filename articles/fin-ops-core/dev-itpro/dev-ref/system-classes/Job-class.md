---
title: Job class
description: This topic describes the Job class.
author: robinarh
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 

audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
---

# Class Job

[!include [banner](../../includes/banner.md)]


```xpp
class Job extends TreeNode
```

The Job class lets you create, read, update, and delete X++ code and metadata.

## Remarks

Make sure that the user has access to the development security key (SysDevelopment) before this API is called.

## Examples

## Methods

| Method                                                     | Description                                                                                                                                   |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public str AOTgetSource()                                  | Returns the source code of this node.                                                                                                         |
| public str changedBy(\[str value\])                        | Gets or sets the name of the user who last changed the application object.                                                                    |
| public Date changedDate(\[Date value\])                    | Gets or sets the date that an application object was last changed.                                                                            |
| public str changedTime(\[str value\])                      | Gets or sets the time that an application object was last changed.                                                                            |
| public str createdBy(\[str value\])                        | Gets or sets the name of the user who created the application object.                                                                         |
| public Date creationDate(\[Date value\])                   | Gets or sets the date that an application object was created.                                                                                 |
| public str creationTime(\[str value\])                     |                                                                                                                                               |
| public str name(\[str value\])                             | Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object. |
| public Guid origin(\[Guid value\])                         |                                                                                                                                               |
| public void AOTsetSource(str source, \[boolean isStatic\]) | Sets the source code of this node.                                                                                                            |
| public void AOTrun()                                       | Compiles this node and its subtree in the Application Object Tree (AOT).                                                |
| public void AOTedit(\[int Line\], \[int Column\])          | Opens the appropriate editor for this node.                                                                                                   |

## Method AOTgetSource

Returns the source code of this node.

```xpp
public str AOTgetSource()
```

### Return Value - AOTgetSource

A string that contains the source code, if there is any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).

### Remarks - AOTgetSource

This function is overridden by nodes that have source code.

## Method changedBy

Gets or sets the name of the user who last changed the application object.

```xpp
public str changedBy([str value])
```

### Parameters - changedBy

value  

### Return Value - changedBy

The name of the user.

## Method changedDate

Gets or sets the date that an application object was last changed.

```xpp
public Date changedDate([Date value])
```

### Parameters - changedDate

value  

### Return Value - changedDate

The date that an application object was last changed.

## Method changedTime

Gets or sets the time that an application object was last changed.

```xpp
public str changedTime([str value])
```

### Parameters - changedTime

value  

### Return Value - changedTime

The time that an application object was last changed.

## Method createdBy

Gets or sets the name of the user who created the application object.

```xpp
public str createdBy([str value])
```

### Parameters - createdBy

value  

### Return Value - createdBy

The name of the user.

## Method creationDate

Gets or sets the date that an application object was created.

```xpp
public Date creationDate([Date value])
```

### Parameters - creationDate

value  

### Return Value - creationDate

The date that an application object was created.

## Method creationTime

```xpp
public str creationTime([str value])
```

### Parameters - creationTime

value  

### Return Value - creationTime

## Method name

Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.

```xpp
public str name([str value])
```

### Parameters - name

value  

### Return Value - name

The name that is used in the code to identify an application object.

### Remarks - name

The name property value of an object must meet the following criteria to avoid code conflicts:

-   Begins with a letter.
-   Doesn't exceed 250 characters.
-   Can include numbers and underscore characters.
-   Cannot include punctuation or spaces.
-   Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.

## Method origin

```xpp
public Guid origin([Guid value])
```

### Parameters - origin

value  

### Return Value - origin

## Method AOTsetSource

Sets the source code of this node.

```xpp
public void AOTsetSource(str source, [boolean isStatic])
```

### Parameters - AOTsetSource

source  
A value that specifies whether the method is static; optional.

<!-- -->

isStatic  
A value that specifies whether the method is static; optional.

### Remarks - AOTsetSource

This method is overridden by nodes that have source code.

## Method AOTrun

Compiles this node and its subtree in the Application Object Tree (AOT).

```xpp
public void AOTrun()
```

## Method AOTedit

Opens the appropriate editor for this node.

```xpp
public void AOTedit([int Line], [int Column])
```

### Parameters - AOTedit

Line  
The column of the cursor position; optional.

<!-- -->

Column  
The column of the cursor position; optional.

### Remarks - AOTedit

If the node is a method, the code editor opens. If the node is a documentation object, the Help editor opens.


