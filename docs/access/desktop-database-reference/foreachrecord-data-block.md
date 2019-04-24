---
title: ForEachRecord データブロック
TOCTitle: ForEachRecord data block
ms:assetid: be369196-230e-1f92-e36b-667048eef2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822743(v=office.15)
ms:contentKeyID: 48547455
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84ab685b946e390645027790e5b1402561527ab6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292329"
---
# <a name="foreachrecord-data-block"></a>ForEachRecord データブロック

**適用先:** Access 2013、Office 2013

**ForEachRecord** データ ブロックは、ドメイン内のレコードごとにステートメントのセットを繰り返します。

> [!NOTE]
> **ForEachRecord** データ ブロックは、データ マクロでのみ使用できます。

## <a name="setting"></a>Setting

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
<td><p><strong>順番</strong></p></td>
<td><p>はい</p></td>
<td><p>実行するステートメントの対象レコードのドメインを識別する文字列。In<em></em> 引数には、テーブル名、選択クエリ、または SQL ステートメントを含めることができます。</p><p><strong>注</strong>: 指定されたドメインには、リンクテーブルまたは ODBC データソースに格納されているデータを含めることはできません。</p></td>
</tr>
<tr class="even">
<td><p>Where Condition/Where 条件式</p></td>
<td><p>いいえ</p></td>
<td><p><strong>ForEachRecord</strong> データ ブロックを適用するデータの範囲を制限するための文字列式を指定します。たとえば、多くの場合、抽出条件は SQL 式の WHERE 句と同じ役割を果たします (ただし WHERE という語は使用しません)。抽出条件を省略すると、<strong>ForEachRecord</strong> データ ブロックは In<em></em> 引数で指定したドメイン全体に適用されます。抽出条件に含めるフィールドは、In<em></em> にも含まれている必要があります。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Alias</strong></p></td>
<td><p>いいえ</p></td>
<td><p>In<em></em> 引数で指定したドメインの別名となる文字列。 多くの場合、あいまいな参照を防ぐために、後で参照するためにテーブル名を短くするために使用されます。<em>alias</em>が指定されていない場合は、テーブル名またはクエリ名がエイリアスとして使用されます。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

Use the **[ExitForEachRecord](exitforeachrecord-macro-action.md)** action to exit a **ForEachRecord** data block immediately.

