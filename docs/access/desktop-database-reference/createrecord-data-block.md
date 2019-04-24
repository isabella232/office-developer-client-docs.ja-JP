---
title: CreateRecord データブロック
TOCTitle: CreateRecord data block
ms:assetid: e18f47f8-2aad-9a14-ad63-ab603a4d5b07
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835671(v=office.15)
ms:contentKeyID: 48548263
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 63e189143e77f9fcc42fa8d48c3ebfb2feda6633
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295353"
---
# <a name="createrecord-data-block"></a>CreateRecord データブロック


**適用先:** Access 2013、Office 2013

You can use the **CreateRecord** data block to create a new record in the specified table.

> [!NOTE]
> **CreateRecord** データ ブロックはデータ マクロでのみ使用できます。

## <a name="setting"></a>Setting

CreateRecord データ ブロックの引数は次のとおりです。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>引数</p></th>
<th><p>必須</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Create a Record In</strong>/レコードの作成先</p></td>
<td><p>はい</p></td>
<td><p>新しいレコードを作成するテーブルの名前。</p></td>
</tr>
<tr class="even">
<td><p><strong>Alias</strong></p></td>
<td><p>いいえ</p></td>
<td><p>レコードを識別する文字列。レコードの別名を使用できます。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

**CreateRecord** で作成したレコードは自動的にカレント レコードになります。

**CreateRecord** ステートメントの後に、新しいレコードの作成を確定する前に実行するコマンドのブロックを挿入できます。 **CreateRecord** データ ブロックで使用できるアクションは次のとおりです。

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


After the **CreateRecord** action creates a record, use the **SetField** action to specify a value of a field in the new record.

You can use an **If...Then...Else** statment to perform operations based on a condition.

To cancel the creation of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **CreateRecord** data block.

新しいレコードの作成を確定すると、 **LastCreateRecordIdentity** ローカル変数を使用してレコードを操作できます。たとえば、次の構文では一番新しく作成したレコードの AssignedTo フィールドを参照します。

`[LastCreateRecordIdentity].[AssignedTo]`

The **CreateRecord** data block can only be used in the **[After Insert](after-insert-macro-event.md)**, **[After Update](after-update-macro-event.md)**, and **[After Update](after-update-macro-event.md)** data macro events.

