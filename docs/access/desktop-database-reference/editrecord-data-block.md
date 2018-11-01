---
title: EditRecord データ ブロック
TOCTitle: EditRecord Data Block
ms:assetid: fe9f55eb-d7ed-1914-65a9-fa2fcb332b98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837277(v=office.15)
ms:contentKeyID: 48548940
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9c4d5a5a1565aeda41e5a52127e9f82b5304e686
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876884"
---
# <a name="editrecord-data-block"></a>EditRecord データ ブロック

**適用されます**Access 2013、Office 2013。

**EditRecord** データ ブロックを使用して、既存のレコード内の値を変更できます。

> [!NOTE]
> [!メモ] **EditRecord** データ ブロックは、データ マクロでのみ使用できます。


## <a name="setting"></a>設定

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
<td><p><strong>エイリアス</strong></p></td>
<td><p>編集するレコードを識別する文字列です。 <em>別名</em>引数を指定しない場合、現在のレコードを編集します。</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>備考

**EditRecord**ステートメントの後に、レコードに対する変更は、コミットされていない前に実行するコマンドのブロックを挿入できます。 **EditRecord**データ ブロックに次の操作を利用できます。

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="cancelrecordchange-macro-action.md">"CancelRecordChange/レコードの変更の取り消し" マクロ アクション</a></p></td>
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
<td><p><a href="setfield-macro-action.md">"SetField/フィールドの設定" マクロ アクション</a></p></td>
</tr>
<tr class="even">
<td><p><a href="setlocalvar-macro-action.md">"SetLocalVar/ローカル変数の設定" マクロ アクション</a></p></td>
</tr>
</tbody>
</table>

" **SetField** /フィールドの設定" アクションを使用して、編集するレコードの新しいフィールド値を指定します。

場合、**を使用することができます.そうしたら。。。他**の条件に基づいて、ステートメントを使用して操作を実行します。

レコードの編集を取り消すには、" **CancelRecordChange** /レコードの変更の取り消し" アクションを使用します。これにより、変更は確定されずに、 **EditRecord** データ ブロックが終了します。

**LastCreateRecordIdentity** ローカル変数を使用して、 **CreateRecord** データ ブロックで一番新しく作成したレコードを操作できます。たとえば、次の構文では一番新しく作成したレコードの AssignedTo フィールドを参照します。

`[LastCreateRecordIdentity].[AssignedTo]`

CreateRecord データ ブロックは、**[後に挿入](after-insert-macro-event.md)**、**[更新した後](after-update-macro-event.md)**、および**[更新後](after-update-macro-event.md)** のデータ マクロのイベントでのみ使用できます。

