---
title: Field メンバー (DAO)
TOCTitle: Field Members
ms:assetid: 4b6a587f-1fd0-37fb-db7d-75b587a8dc60
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193511(v=office.15)
ms:contentKeyID: 48544689
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a89ed019d9ab725ddcaa420679f4fcf4b9362e0c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552983"
---
# <a name="field-members-dao"></a>Field メンバー (DAO)


**適用先:** Access 2013、Office 2013

Field オブジェクトは、共通のデータ型およびプロパティの共通セットを持つ、データの列を表します。

## <a name="methods"></a>メソッド

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="field-appendchunk-method-dao.md">AppendChunk</a></strong></p></td>
<td><p>文字列式から <strong><a href="field-object-dao.md">Recordset</a></strong> のメモ型 (Memo) またはロング バイナリ型 (Long Binary) の <strong><a href="recordset-object-dao.md">Field</a></strong> オブジェクトにデータを追加します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>新しいユーザー定義の <strong><a href="property-object-dao.md">Property</a></strong> オブジェクトを作成します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-getchunk-method-dao.md">GetChunk</a></strong></p></td>
<td><p>Recordset オブジェクトの Fields コレクション内の<strong></strong>Memo オブジェクトまたは<strong>Long</strong> Binary <strong><a href="fields-collection-dao.md"></a></strong> <strong><a href="field-object-dao.md">Field</a></strong>オブジェクトの内容のすべてまたは一部を<strong><a href="recordset-object-dao.md">返</a></strong>します。</p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a>プロパティ

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="field-allowzerolength-property-dao.md">AllowZeroLength</a></strong></p></td>
<td><p>長さ 0 の文字列 ( ) が、Text または Memo データ型 (Microsoft Access ワークスペースのみ) を持つ Field オブジェクトの Value プロパティに対して有効な設定であるかどうかを示す値を設定または返 &quot; &quot; します。 <strong><a href="field-value-property-dao.md"></a></strong> <strong><a href="field-object-dao.md"></a></strong></p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-attributes-property-dao.md">Attributes</a></strong></p></td>
<td><p><strong><a href="field-object-dao.md">Field</a></strong> オブジェクトの 1 つまたは複数の特性を示す値を設定または取得します。値の取得および設定が可能です。長整数型 ( <strong>Long</strong> ) の値を使用します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-collatingorder-property-dao.md">CollatingOrder</a></strong></p></td>
<td><p>文字列の比較または並べ替えのために、文字列の並べ替え順序を指定する値を返します (Microsoft Access ワークスペースのみ)。値の取得のみ可能です。長整数型 ( <strong>Long</strong>) の値を使用します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-dataupdatable-property-dao.md">DataUpdatable</a></strong></p></td>
<td><p><strong><a href="field-object-dao.md">Field</a></strong> オブジェクトで表されるフィールドのデータが更新可能かどうかを示す値を返します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-defaultvalue-property-dao.md">DefaultValue</a></strong></p></td>
<td><p><strong><a href="field-object-dao.md">Field</a></strong> オブジェクトの既定値を設定または取得します。 <a href="fields-collection-dao.md"><strong>Fields</strong></a> コレクションにまだ追加されていない <strong>Field</strong> オブジェクトの場合、このプロパティは値の取得および設定が可能です (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-fieldsize-property-dao.md">FieldSize</a></strong></p></td>
<td><p><strong><a href="field-object-dao.md">Recordset</a></strong> オブジェクトの <strong><a href="fields-collection-dao.md">Fields</a></strong> コレクション内にあるメモ型 (Memo) またはロング バイナリ型 (Long Binary) の <strong><a href="recordset-object-dao.md">Field</a></strong> オブジェクトを、メモリではなくデータベースで使用する場合のバイト数を取得します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-foreignname-property-dao.md">ForeignName</a></strong></p></td>
<td><p>リレーションシップの主テーブルのフィールドに対応する、外部キー側のテーブルの <strong><a href="field-object-dao.md">Field</a></strong> オブジェクトの名前を指定する値を設定または取得します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-name-property-dao.md">Name</a></strong></p></td>
<td><p>指定したオブジェクトの名前を取得または設定します。オブジェクトがコレクションに追加されていない場合、値の取得および設定が可能です。文字列型 ( <strong>String</strong>) の値を使用します。オブジェクトがコレクションに追加されている場合、値の取得のみ可能です。文字列型 ( <strong>String</strong>) の値を使用します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-ordinalposition-property-dao.md">OrdinalPosition</a></strong></p></td>
<td><p><strong><a href="field-object-dao.md">Fields</a></strong> コレクション内の <strong><a href="fields-collection-dao.md">Field</a></strong> オブジェクトの相対位置を設定または取得します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-originalvalue-property-dao.md">OriginalValue</a></strong></p></td>
<td><p><strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong>の値の 1 つ。</p>
<td><p><strong>注</strong>: Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。 Microsoft Access データベース エンジンを使用せずに外部データ ソースにアクセスする場合は、ADO を使用してください。</p>
<p>最後のバッチ更新を開始したときにデータベース内に存在した <strong>Field</strong> オブジェクトの値を取得します (ODBCDirect ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>指定したオブジェクトの <strong><a href="properties-collection-dao.md">Properties</a></strong> コレクションを取得します。値の取得のみ可能です。  </p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-required-property-dao.md">必須</a></strong></p></td>
<td><p><strong><a href="field-object-dao.md">Field</a></strong> オブジェクトに非 Null 値が必要かどうかを示す値を設定または取得します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-fieldsize-property-dao.md">サイズ</a></strong></p></td>
<td><p><strong><a href="field-object-dao.md">Recordset</a></strong> オブジェクトの <strong><a href="fields-collection-dao.md">Fields</a></strong> コレクション内にあるメモ型 (Memo) またはロング バイナリ型 (Long Binary) の <strong><a href="recordset-object-dao.md">Field</a></strong> オブジェクトを、メモリではなくデータベースで使用する場合のバイト数を取得します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-sourcefield-property-dao.md">SourceField</a></strong></p></td>
<td><p><strong>Field</strong> オブジェクトの元のデータ ソースであるフィールド名を示す値を取得します。値の取得のみ可能です。文字列型 ( <strong>String</strong>) の値を使用します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-sourcetable-property-dao.md">SourceTable</a></strong></p></td>
<td><p><strong>Field</strong> オブジェクトの元のデータ ソースとなるテーブルの名前を示す値を取得します。値の取得のみ可能です。文字列型 ( <strong>String</strong>) の値を使用します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-type-property-dao.md">種類</a></strong></p></td>
<td><p>オブジェクトの操作の種類またはデータ型を示す値を設定または取得します。値の取得および設定が可能です。整数型 (<strong>Integer</strong>) の値を使用します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-validateonset-property-dao.md">ValidateOnSet</a></strong></p></td>
<td><p>オブジェクトの <strong><a href="field-object-dao.md">Value</a></strong> プロパティの設定時に、 <strong><a href="field-value-property-dao.md">Field</a></strong> オブジェクトの値を直ちに検証するかどうかを指定する値を設定または取得します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-validationrule-property-dao.md">ValidationRule</a></strong></p></td>
<td><p>テーブルのフィールドを変更するかテーブルにフィールドを追加するときに、フィールド内のデータを検証する値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得および設定が可能です。文字列型 ( <strong>String</strong>) の値を使用します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-validationtext-property-dao.md">ValidationText</a></strong></p></td>
<td><p><strong>Field</strong> オブジェクトの値が <strong>ValidationRule</strong> プロパティに設定されている入力規則を満たさない場合に、アプリケーションに表示するメッセージのテキストを指定する値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得および設定が可能です。文字列型 ( <strong>String</strong> ) の値を使用します。  </p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-value-property-dao.md">Value</a></strong></p></td>
<td><p>オブジェクトの値を設定します。値の取得および設定が可能です。バリアント型 ( <strong>Variant</strong>) の値を使用します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-visiblevalue-property-dao.md">VisibleValue</a></strong></p></td>
<td><p><strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong>の値の 1 つ。</p>
<td><p><strong>注</strong>: Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。 Microsoft Access データベース エンジンを使用せずに外部データ ソースにアクセスする場合は、ADO を使用してください。</p>
<p>現在データベース内にある、バッチ更新の競合によって決まる <strong>OriginalValue</strong> プロパティより新しい値を取得します (ODBCDirect ワークスペースのみ)。</p></td>
</tr>
</tbody>
</table>

