---
title: .alter table folder - Azure Data Explorer
description: This article describes .alter table folder in Azure Data Explorer.
ms.reviewer: orspodek
ms.topic: reference
ms.date: 02/28/2020
---
# .alter table folder

Alters the folder value of an existing table.

> [!NOTE]
> If the table does not exist, an error is returned. For creating a new table, see [`.create table`](create-table-command.md)

## Permission

You must have at least [Table Admin](access-control/role-based-access-control.md) permissions to run this command.

## Syntax

`.alter` `table` *TableName* `folder` *Folder*

## Parameters

|Name|Type|Required|Description|
|--|--|--|--|
| *TableName* | string | &check; | The name of the table to alter.|
| *Folder* | string | &check; | The new folder for the table.|

## Examples

```kusto
.alter table MyTable folder "Updated folder"
```

```kusto
.alter table MyTable folder @"First Level\Second Level"
```
