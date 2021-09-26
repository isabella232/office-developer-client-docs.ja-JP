---
title: Before Delete マクロ イベント
TOCTitle: Before Delete macro event
ms:assetid: 1a8d3457-5c59-d13e-ada9-6ecd33dfd5b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845672(v=office.15)
ms:contentKeyID: 48543520
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm186077
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: d8f4f44ae2acdfe5f20b5ee8a95314f518be07f8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607123"
---
# <a name="before-delete-macro-event"></a>Before Delete マクロ イベント

**適用先**: Access 2013、Office 2013

The **Before Delete** event occurs when a record is deleted, but before the change is committed.

> [!NOTE]
> Before Delete イベントは、データ マクロでのみ使用できます。

## <a name="remarks"></a>注釈

Use the **Before Delete** event to perform any actions that you want to occur before a record is deleted. The **Before Change** is commonly used to perform validation and to raise custom error messages.

削除するレコードの値にアクセスするには、次の構文を使用します。

`[Old].[Field Name]`

たとえば、削除するレコードの QuantityInStock フィールドの値にアクセスするには、次の構文を使用します。

`[Old].[QuantityInStock]`

The values contained in the record to be deleted are deleted permanently when the **Before Delete** event ends.

You can cancel the **Before Delete** event by using the **RaiseError** action. エラーが発生すると、Before **Delete** イベントに含まれる変更は破棄されます。

The following table lists macro commands that can be used in the **Before Delete** event.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>コマンドの種類</p></th>
<th><p>コマンド</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>プログラム フロー</p></td>
<td><p><a href="comment-macro-statement.md">Comment マクロ ステートメント</a></p></td>
</tr>
<tr class="even">
<td><p>プログラム フロー</p></td>
<td><p><a href="group-macro-statement.md">Group マクロ ステートメント</a></p></td>
</tr>
<tr class="odd">
<td><p>プログラム フロー</p></td>
<td><p><a href="if-then-else-macro-block.md">If...Then...Else マクロ ブロック</a></p></td>
</tr>
<tr class="even">
<td><p>データ ブロック</p></td>
<td><p><a href="lookuprecord-data-block.md">LookupRecord マクロ アクション</a></p></td>
</tr>
<tr class="odd">
<td><p>データ アクション</p></td>
<td><p><a href="clearmacroerror-macro-action.md">ClearMacroError マクロ アクション</a></p></td>
</tr>
<tr class="even">
<td><p>データ アクション</p></td>
<td><p><a href="onerror-macro-action.md">OnError マクロ アクション</a></p></td>
</tr>
<tr class="odd">
<td><p>データ アクション</p></td>
<td><p><a href="raiseerror-macro-action.md">RaiseError マクロ アクション</a></p></td>
</tr>
<tr class="even">
<td><p>データ アクション</p></td>
<td><p><a href="setlocalvar-macro-action.md">SetLocalVar マクロ アクション</a></p></td>
</tr>
<tr class="odd">
<td><p>データ アクション</p></td>
<td><p><a href="stopmacro-macro-action.md">StopMacro マクロ アクション</a></p></td>
</tr>
</tbody>
</table>


To create a Data macro that captures the **Before Delete** event, use the following steps.

1.  Open the table for which you want to capture the **Before Delete** event.

2.  [テーブル] **タブの** [Before **Events] グループで** 、[削除前] **を選択します**。

