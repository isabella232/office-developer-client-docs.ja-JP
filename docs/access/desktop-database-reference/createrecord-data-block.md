---
title: CreateRecord データ ブロック
TOCTitle: CreateRecord data block
ms:assetid: e18f47f8-2aad-9a14-ad63-ab603a4d5b07
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835671(v=office.15)
ms:contentKeyID: 48548263
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 63e189143e77f9fcc42fa8d48c3ebfb2feda6633
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719819"
---
# <a name="createrecord-data-block"></a>CreateRecord データ ブロック


**適用されます**Access 2013、Office 2013。

**CreateRecord** データ ブロックを使用して、指定したテーブルに新しいレコードを作成できます。

> [!NOTE]
> [!メモ] **CreateRecord** データ ブロックはデータ マクロでのみ使用できます。

## <a name="setting"></a>設定

**CreateRecord** データ ブロックの引数は次のとおりです。

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
<td><p><strong>内のレコードを作成します。</strong></p></td>
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
<td><p><a href="if-then-else-macro-block.md">もし。。。そうしたら。。。マクロ ステートメントはその他</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="setfield-macro-action.md">SetField マクロ アクション</a></p></td>
</tr>
<tr class="even">
<td><p><a href="setlocalvar-macro-action.md">SetLocalVar マクロ アクション</a></p></td>
</tr>
</tbody>
</table>


" **CreateRecord** /レコードの作成" アクションでレコードを作成した後、" **SetField** /フィールドの設定" アクションを使用して、新しいレコードのフィールド値を指定します。

場合、**を使用することができます.そうしたら。。。他**の条件に基づいて、ステートメントを使用して操作を実行します。

レコードの作成を取り消すには " **CancelRecordChange** /レコードの変更の取り消し" アクションを使用します。これにより、変更は確定されずに、 **CreateRecord** データ ブロックが終了します。

新しいレコードの作成を確定すると、 **LastCreateRecordIdentity** ローカル変数を使用してレコードを操作できます。たとえば、次の構文では一番新しく作成したレコードの AssignedTo フィールドを参照します。

`[LastCreateRecordIdentity].[AssignedTo]`

**CreateRecord**データ ブロックは、**[後に挿入](after-insert-macro-event.md)**、**[更新した後](after-update-macro-event.md)**、および**[更新後](after-update-macro-event.md)** のデータ マクロのイベントでのみ使用できます。

