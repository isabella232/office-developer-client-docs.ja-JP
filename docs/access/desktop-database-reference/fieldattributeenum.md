---
title: FieldAttributeEnum (Access デスクトップデータベースリファレンス)
TOCTitle: FieldAttributeEnum
ms:assetid: 2d3a541e-a437-6108-ab0e-90c7884b3df7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249071(v=office.15)
ms:contentKeyID: 48543967
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 079c79af3d15a6a5864a7db7f8334393258cfd42
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292602"
---
# <a name="fieldattributeenum"></a>FieldAttributeEnum

**適用先:** Access 2013、Office 2013

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
<td><p><strong>adfldcachedeferred</strong></p></td>
<td><p>0x1000</p></td>
<td><p>プロバイダーでフィールド値がキャッシュされ、その後の読み取りはキャッシュから行われることを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adfldfixed</strong></p></td>
<td><p>0x10</p></td>
<td><p>フィールドが固定長データを含むことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adfldischapter</strong></p></td>
<td><p>0x2000</p></td>
<td><p>フィールドがチャプター値を含み、この親フィールドに関連付けられた特定の子レコードセットを指定していることを示します。通常、チャプター フィールドはデータ シェイプやフィルター用に使います。</p></td>
</tr>
<tr class="even">
<td><p><strong>adfldiscollection</strong></p></td>
<td><p>0x40000</p></td>
<td><p>レコードが示すリソースが、テキスト ファイルなどの単純なリソースではなく、フォルダーなどのように他のリソースのコレクションであることを、フィールドが表していることを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adfldisdefaultstream</strong></p></td>
<td><p>0x20000</p></td>
<td><p>フィールドが、レコードが示すリソースの既定ストリームを含むことを示します。 たとえば、既定のストリームは、web サイトのルートフォルダーの HTML コンテンツにすることができます。これは、ルート URL が指定されたときに自動的に提供されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>adfldisnullable</strong></p></td>
<td><p>0x20</p></td>
<td><p>フィールドに null 値を指定できることを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adfldisrowurl</strong></p></td>
<td><p>「その他」</p></td>
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
<td><p><strong>adfld/defer</strong></p></td>
<td><p>0x2</p></td>
<td><p>フィールドが遅延フィールドであることを示します。フィールド値は、レコード全体のデータ ソースから取得されず、明示的にアクセスした場合のみ取得されます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldNegativeScale</strong></p></td>
<td><p>0x4000</p></td>
<td><p>負のスケール値をサポートする列の数値を、フィールドが表していることを示します。スケールは、<a href="numericscale-property-ado.md">NumericScale</a> プロパティで指定します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adflん wid</strong></p></td>
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
<td><p><strong>adfldunspecified</strong></p></td>
<td><p>-1<br />
0xFFFFFFFF</p></td>
<td><p>プロバイダーがフィールド属性を指定しないことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldUpdatable</strong></p></td>
<td><p>0x4</p></td>
<td><p>フィールドへの書き込みが可能であることを示します。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC と同等

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
<td><p>FieldAttribute の遅延 AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums FieldAttribute</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums FieldAttribute</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums FieldAttribute</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums。 FieldAttribute</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums FieldAttribute</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums FieldAttribute</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums FieldAttribute</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums</p></td>
</tr>
</tbody>
</table>

