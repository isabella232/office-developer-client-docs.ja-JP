---
title: Before Delete マクロ イベント
TOCTitle: Before Delete Macro Event
ms:assetid: 1a8d3457-5c59-d13e-ada9-6ecd33dfd5b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845672(v=office.15)
ms:contentKeyID: 48543520
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm186077
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0ee4878a742454eb1b02f4b9a45c14ad79097c46
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876261"
---
# <a name="before-delete-macro-event"></a>Before Delete マクロ イベント

**適用されます**Access 2013、Office 2013。

**削除する前に**イベントは、レコードが削除されると、変更がコミットされる前に発生します。

> [!NOTE]
> **前に Delete**イベントは、データ マクロでのみ使用可能です。

## <a name="remarks"></a>備考

使用して、レコードの前に発生する操作を実行**する前に削除**イベントが削除されます。 **変更**する前に、検証を実行して、カスタム エラー メッセージが発生する通常使用されます。

次の構文を使用して、削除するレコードの値にアクセスすることができます。

`[Old].[Field Name]`

など、削除するレコードの QuantityInStock フィールドの値にアクセスするには、次の構文を使用します。

`[Old].[QuantityInStock]`

**削除する前に**イベントが終了したとき、削除するレコードに含まれる値が完全に削除します。

**RaiseError**アクションを使用して、**削除する前に**イベントをキャンセルできます。 エラーが発生すると**する前に Delete**イベントに含まれる変更は破棄されます。

**削除する前に**イベントで使用できるマクロのコマンドを次の表に一覧します。

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
<td><p><a href="lookuprecord-data-block.md">不一致のマクロ アクション</a></p></td>
</tr>
<tr class="odd">
<td><p>データ アクション</p></td>
<td><p><a href="clearmacroerror-macro-action.md">"ClearMacroError/マクロエラーのクリア" マクロ アクション</a></p></td>
</tr>
<tr class="even">
<td><p>データ アクション</p></td>
<td><p><a href="onerror-macro-action.md">OnError マクロ アクション</a></p></td>
</tr>
<tr class="odd">
<td><p>データ アクション</p></td>
<td><p><a href="raiseerror-macro-action.md">"RaiseError/エラーの生成" マクロ アクション</a></p></td>
</tr>
<tr class="even">
<td><p>データ アクション</p></td>
<td><p><a href="setlocalvar-macro-action.md">"SetLocalVar/ローカル変数の設定" マクロ アクション</a></p></td>
</tr>
<tr class="odd">
<td><p>データ アクション</p></td>
<td><p><a href="stopmacro-macro-action.md">StopMacro マクロ アクション</a></p></td>
</tr>
</tbody>
</table>


**削除する前に**イベントをキャプチャするデータ マクロを作成するには、次の手順を使用します。

1.  **削除する前に**イベントをキャプチャするテーブルを開きます。

2.  [**表**] タブで、[**前に、のイベント**] を選択**する前に削除**します。

