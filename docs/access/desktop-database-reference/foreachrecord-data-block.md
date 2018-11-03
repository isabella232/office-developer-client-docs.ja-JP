---
title: ForEachRecord データ ブロック
TOCTitle: ForEachRecord data block
ms:assetid: be369196-230e-1f92-e36b-667048eef2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822743(v=office.15)
ms:contentKeyID: 48547455
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 09a09a80773adecf760ae4610df30bbd5f36f3d6
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937527"
---
# <a name="foreachrecord-data-block"></a>ForEachRecord データ ブロック


**適用されます**Access 2013、Office 2013。

**ForEachRecord** データ ブロックは、ドメイン内のレコードごとにステートメントのセットを繰り返します。

> [!NOTE]
> [!メモ] **ForEachRecord** データ ブロックは、データ マクロでのみ使用できます。

## <a name="setting"></a>設定

" **ForEachRecord** /レコードごと" アクションの引数は次のとおりです。

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
<td><p><strong>で</strong></p></td>
<td><p>はい</p></td>
<td><p>ステートメントを実行するレコードのドメインを識別する文字列を指定します。<em>In</em> 引数には、テーブル名、選択クエリ、または SQL ステートメントを含めることができます。</p>

> [!NOTE]
> 指定したドメインには、リンク テーブルまたは ODBC データ ソース内のデータを含めることはできません。


<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Where Condition</strong></p></td>
<td><p>いいえ</p></td>
<td><p><strong>ForEachRecord</strong> データ ブロックを適用するデータの範囲を制限するための文字列式を指定します。たとえば、多くの場合、抽出条件は SQL 式の WHERE 句と同じ役割を果たします (ただし WHERE という語は使用しません)。抽出条件を省略すると、<strong>ForEachRecord</strong> データ ブロックは In<em></em> 引数で指定したドメイン全体に適用されます。抽出条件に含めるフィールドは、In<em></em> にも含まれている必要があります。</p></td>
</tr>
<tr class="odd">
<td><p><strong>エイリアス</strong></p></td>
<td><p>いいえ</p></td>
<td><p><em></em>引数で指定されたドメインの代替名を提供する文字列です。 あいまいな参照を防ぐへの参照のテーブル名を短くには、よく使用されます。<em>エイリアス</em>が指定されていない場合、テーブルまたはクエリの名前がエイリアスとして使用します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>備考

[ForEachRecord](exitforeachrecord-macro-action.md) データ ブロックを即座に終了するには、" ****ExitForEachRecord/レコードごとに終了**** " アクションを使用します。

