---
title: FieldAttributeEnum (デスクトップ データベース参照のアクセス)
TOCTitle: FieldAttributeEnum
ms:assetid: 2d3a541e-a437-6108-ab0e-90c7884b3df7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249071(v=office.15)
ms:contentKeyID: 48543967
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 4a99bf18207b6bd1744fb0ee2b1a2dc10254c604
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874385"
---
# <a name="fieldattributeenum"></a>FieldAttributeEnum

**適用されます**Access 2013、Office 2013。

[Field](field-object-ado.md) オブジェクトの 1 つ以上の属性を表します。

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>値</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adFldCacheDeferred</strong></p></td>
<td><p>0x1000</p></td>
<td><p>プロバイダーでフィールド値がキャッシュされ、その後の読み取りはキャッシュから行われることを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldFixed</strong></p></td>
<td><p>0x10</p></td>
<td><p>フィールドが固定長データを含むことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldIsChapter</strong></p></td>
<td><p>0x2000</p></td>
<td><p>フィールドがチャプター値を含み、この親フィールドに関連付けられた特定の子レコードセットを指定していることを示します。通常、チャプター フィールドはデータ シェイプやフィルター用に使います。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldIsCollection</strong></p></td>
<td><p>0x40000</p></td>
<td><p>レコードが示すリソースが、テキスト ファイルなどの単純なリソースではなく、フォルダーなどのように他のリソースのコレクションであることを、フィールドが表していることを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldIsDefaultStream</strong></p></td>
<td><p>0x20000</p></td>
<td><p>フィールドにレコードが示すリソースの既定のストリームが含まれていることを示します。 たとえば、既定のストリームには、ルート URL を指定すると自動的に提供される web サイトのルート フォルダーの HTML コンテンツができます。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldIsNullable</strong></p></td>
<td><p>0x20</p></td>
<td><p>フィールドに null 値を指定できることを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldIsRowURL</strong></p></td>
<td><p>0x10000</p></td>
<td><p>フィールドが、レコードが示すデータ ストアのリソースを指定する URL を含むことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldLong</strong></p></td>
<td><p>0x80</p></td>
<td><p>フィールドがロング バイナリ型のフィールドであることを示します。また、<a href="appendchunk-method-ado.md">AppendChunk</a> メソッドと <a href="getchunk-method-ado.md">GetChunk</a> メソッドを使用できることを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldMayBeNull</strong></p></td>
<td><p>0x40</p></td>
<td><p>フィールドからの null 値の読み取りが可能であることを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldMayDefer</strong></p></td>
<td><p>0x2</p></td>
<td><p>フィールドが遅延フィールドであることを示します。フィールド値は、レコード全体のデータ ソースから取得されず、明示的にアクセスした場合のみ取得されます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldNegativeScale</strong></p></td>
<td><p>0x4000</p></td>
<td><p>負のスケール値をサポートする列の数値を、フィールドが表していることを示します。スケールは、<a href="numericscale-property-ado.md">NumericScale</a> プロパティで指定します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldRowID</strong></p></td>
<td><p>0x100</p></td>
<td><p>フィールドが書き込み禁止の永続化された行識別子を含み、行を識別するもの (レコード番号、一意識別子など) 以外に有効な値は持たないことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldRowVersion</strong></p></td>
<td><p>0x200</p></td>
<td><p>フィールドが更新を記録するための時刻または日付スタンプを含むことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldUnknownUpdatable</strong></p></td>
<td><p>0x8</p></td>
<td><p>フィールドへの書き込みが可能かどうかをプロバイダーが確認できないことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldUnspecified</strong></p></td>
<td><p>-1<br />
0 xffffffff</p></td>
<td><p>プロバイダーがフィールド属性を指定しないことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldUpdatable</strong></p></td>
<td><p>0x4</p></td>
<td><p>フィールドへの書き込みが可能であることを示します。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC に相当

パッケージ: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.FieldAttribute.CACHEDEFERRED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.FieldAttribute.FIXED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.FieldAttribute.ISNULLABLE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.FieldAttribute.LONG</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.FieldAttribute.MAYBENULL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.FieldAttribute.MAYDEFER</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.FieldAttribute.NEGATIVESCALE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.FieldAttribute.ROWID</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.FieldAttribute.ROWVERSION</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.FieldAttribute.UNKNOWNUPDATABLE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.FieldAttribute.UNSPECIFIED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.FieldAttribute.UPDATABLE</p></td>
</tr>
</tbody>
</table>

