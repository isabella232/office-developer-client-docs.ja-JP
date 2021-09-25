---
title: ForEachRecord データ ブロック
TOCTitle: ForEachRecord data block
ms:assetid: be369196-230e-1f92-e36b-667048eef2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822743(v=office.15)
ms:contentKeyID: 48547455
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d4c451d54b5cf7f2e5d85fed2d74bec4266d5d82
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602529"
---
# <a name="foreachrecord-data-block"></a>ForEachRecord データ ブロック

**適用先**: Access 2013、Office 2013

**ForEachRecord** データ ブロックは、ドメイン内のレコードごとにステートメントのセットを繰り返します。

> [!NOTE]
> **ForEachRecord** データ ブロックは、データ マクロでのみ使用できます。

## <a name="setting"></a>設定

ForEachRecord アクションの引数は次のとおりです。

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
<td><p><strong>In</strong></p></td>
<td><p>必要</p></td>
<td><p>実行するステートメントの対象レコードのドメインを識別する文字列。In<em></em> 引数には、テーブル名、選択クエリ、または SQL ステートメントを含めることができます。</p><p><strong>注</strong>: 指定したドメインには、リンク テーブルまたは ODBC データ ソースに格納されているデータを含めできません。</p></td>
</tr>
<tr class="even">
<td><p>Where Condition/Where 条件式</p></td>
<td><p>いいえ</p></td>
<td><p><strong>ForEachRecord</strong> データ ブロックを適用するデータの範囲を制限するための文字列式を指定します。たとえば、多くの場合、抽出条件は SQL 式の WHERE 句と同じ役割を果たします (ただし WHERE という語は使用しません)。抽出条件を省略すると、<strong>ForEachRecord</strong> データ ブロックは In<em></em> 引数で指定したドメイン全体に適用されます。抽出条件に含めるフィールドは、In<em></em> にも含まれている必要があります。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Alias</strong></p></td>
<td><p>いいえ</p></td>
<td><p>In<em></em> 引数で指定したドメインの別名となる文字列。 多くの場合、あいまいな参照を防ぐために、後続の参照のテーブル名を短くするために使用されます。Alias <em>を</em> 指定しない場合、テーブル名またはクエリ名がエイリアスとして使用されます。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

Use the **[ExitForEachRecord](exitforeachrecord-macro-action.md)** action to exit a **ForEachRecord** data block immediately.

