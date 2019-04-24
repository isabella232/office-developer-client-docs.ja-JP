---
title: データのレコードの禁止
TOCTitle: EditRecord data block
ms:assetid: fe9f55eb-d7ed-1914-65a9-fa2fcb332b98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837277(v=office.15)
ms:contentKeyID: 48548940
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 32ddfbbf21e62d5967fa1f2f31bab0222664eb39
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293596"
---
# <a name="editrecord-data-block"></a>データのレコードの禁止

**適用先:** Access 2013、Office 2013

You can use the **EditRecord** data block to change the values contained in an existing record.

> [!NOTE]
> EditRecord データ ブロックは、データ マクロでのみ使用できます。


## <a name="setting"></a>Setting

**EditRecord** データ ブロックの引数は次のとおりです。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>引数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Alias</strong></p></td>
<td><p>編集するレコードを識別する文字列。"Alias/別名" 引数を指定しない場合、カレント レコードが編集されます。</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>注釈

After **EditRecord** statement, you can insert a block of commands that will execute before the changes to the record are comitted. The following actions are available in a **EditRecord** data block.

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="cancelrecordchange-macro-action.md">CancelRecordChange マクロ アクション</a></p></td>
</tr>
<tr class="even">
<td><p><a href="comment-macro-statement.md">Comment マクロ ステートメント</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="group-macro-statement.md">Group マクロ ステートメント</a></p></td>
</tr>
<tr class="even">
<td><p><a href="if-then-else-macro-block.md">もし。。。そうしたら。。。Else マクロステートメント</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="setfield-macro-action.md">SetField マクロ アクション</a></p></td>
</tr>
<tr class="even">
<td><p><a href="setlocalvar-macro-action.md">SetLocalVar マクロ アクション</a></p></td>
</tr>
</tbody>
</table>

Use the **SetField** action to specify the new values of a field in the edited record.

You can use an **If...Then...Else** statment to perform operations based on a condition.

To cancel the editing of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **EditRecord** data block.

**LastCreateRecordIdentity** ローカル変数を使用して、 **CreateRecord** データ ブロックで一番新しく作成したレコードを操作できます。たとえば、次の構文では一番新しく作成したレコードの AssignedTo フィールドを参照します。

`[LastCreateRecordIdentity].[AssignedTo]`

The CreateRecord data block can only be used in the **[After Insert](after-insert-macro-event.md)**, **[After Update](after-update-macro-event.md)**, and **[After Update](after-update-macro-event.md)** data macro events.

