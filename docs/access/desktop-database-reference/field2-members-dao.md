---
title: Field2 メンバー (DAO)
TOCTitle: Field2 Members
ms:assetid: 27829bbc-8b4e-c7eb-f29b-bcbef341f9fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191913(v=office.15)
ms:contentKeyID: 48543839
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 915a733d59d938e77f32a051b267b5e26bddf6a0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877122"
---
# <a name="field2-members-dao"></a>Field2 メンバー (DAO)


**適用されます**Access 2013、Office 2013。

Field2 オブジェクトは、共通のデータ型およびプロパティの共通セットを持つ、データの列を表します。

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
<td><p><strong><a href="field2-appendchunk-method-dao.md">AppendChunk</a></strong></p></td>
<td><p>文字列式からのデータを <a href="recordset-object-dao.md"><strong>Recordset</strong></a> の、メモ型 (Memo) またはロング バイナリ型 (Long Binary) の <strong>Field2</strong> オブジェクトに追加します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>新しいユーザー定義の <strong><a href="property-object-dao.md">Property</a></strong> オブジェクトを作成します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-getchunk-method-dao.md">GetChunk</a></strong></p></td>
<td><p>すべてを返します。 または<strong><a href="recordset-object-dao.md">Recordset</a></strong>オブジェクトの<strong><a href="fields-collection-dao.md">Fields</a></strong>コレクション内の<strong>メモ</strong>型または<strong>長の BinaryField2</strong>オブジェクトの内容の一部です。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-loadfromfile-method-dao.md">LoadFromFile</a></strong></p></td>
<td><p>指定されたファイルをディスクから読み込みます。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-savetofile-method-dao.md">SaveToFile</a></strong></p></td>
<td><p>添付ファイルをディスクに保存します。</p></td>
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
<td><p><strong><a href="field2-allowzerolength-property-dao.md">AllowZeroLength</a></strong></p></td>
<td><p>示す値を取得または設定かどうか、長さ 0 の文字列 (&quot;&quot;) は、テキスト型またはメモ型 (Microsoft Access ワークスペースのみ) の<strong>Field2</strong>オブジェクトの<strong><a href="field-value-property-dao.md">Value</a></strong>プロパティに有効な設定です。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-appendonly-property-dao.md">AppendOnly</a></strong></p></td>
<td><p>指定されたフィールドについて、新しい値が追加されたときにその値をフィールドの既存の内容に付加するように設定されているかどうかを示すブール型 ( <strong>Boolean</strong>) の値を取得または設定します。値の取得および設定が可能です。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-attributes-property-dao.md">Attributes</a></strong></p></td>
<td><p><strong>Field2</strong> オブジェクトの 1 つまたは複数の特性を示す値を設定または取得します。値の取得および設定が可能です。長整数型 ( <strong>Long</strong>) の値を使用します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-collatingorder-property-dao.md">照合順序</a></strong></p></td>
<td><p>文字列の比較または並べ替えのために、文字列の並べ替え順序を指定する値を返します (Microsoft Access ワークスペースのみ)。値の取得のみ可能です。長整数型 ( <strong>Long</strong>) の値を使用します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-complextype-property-dao.md">ComplexType</a></strong></p></td>
<td><p>複数値を持つフィールドを表す <strong><a href="complextype-object-dao.md">ComplexType</a></strong> オブジェクトを返します。値の取得および設定が可能です。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-dataupdatable-property-dao.md">DataUpdatable</a></strong></p></td>
<td><p><strong>Field2</strong> オブジェクトで表されるフィールドのデータが更新可能かどうかを示す値を返します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-defaultvalue-property-dao.md">DefaultValue</a></strong></p></td>
<td><p><strong>Field2</strong> オブジェクトの既定値を設定または取得します。 <a href="fields-collection-dao.md"><strong>Fields</strong></a> コレクションに追加されていない <strong>Field2</strong> オブジェクトの場合、このプロパティは値の取得および設定が可能です (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-expression-property-dao.md">Expression</a></strong></p></td>
<td><p>値の取得および設定が可能です。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-fieldsize-property-dao.md">フィールド サイズします。</a></strong></p></td>
<td><p>メモリではなくデータベースで使用される、 <a href="fields-collection-dao.md"><strong>Recordset</strong></a> オブジェクトの <a href="recordset-object-dao.md"><strong>Fields</strong></a> コレクションに含まれるメモ型 (Memo) またはロング バイナリ型 (Long Binary) の <strong>Field2</strong> オブジェクトのバイト数を返します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-foreignname-property-dao.md">ForeignName</a></strong></p></td>
<td><p>あるリレーションシップにおいて、主テーブルのフィールドに対応する外部キー側のテーブルの <strong>Field2</strong> オブジェクトの名前を指定する値を設定または取得します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-iscomplex-property-dao.md">IsComplex</a></strong></p></td>
<td><p>指定されたフィールドが複数値データ型かどうかを示すブール型 ( <strong>Boolean</strong>) の値を返します。値の取得および設定が可能です。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-name-property-dao.md">Name</a></strong></p></td>
<td><p>指定したオブジェクトの名前を取得または設定します。オブジェクトがコレクションに追加されていない場合、値の取得および設定が可能です。文字列型 ( <strong>String</strong>) の値を使用します。オブジェクトがコレクションに追加されている場合、値の取得のみ可能です。文字列型 ( <strong>String</strong>) の値を使用します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-ordinalposition-property-dao.md">OrdinalPosition</a></strong></p></td>
<td><p><a href="fields-collection-dao.md"><strong>Fields</strong></a> コレクション内の <strong>Field2</strong> オブジェクトの相対位置を設定または取得します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-originalvalue-property-dao.md">OriginalValue</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</P>


<p>最後のバッチ更新が開始されたときに存在したデータベースの <strong>Field2</strong> の値を返します (ODBCDirect ワークスペースのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>指定したオブジェクトの <strong><a href="properties-collection-dao.md">Properties</a></strong> コレクションを取得します。値の取得のみ可能です。  </p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-required-property-dao.md">必須</a></strong></p></td>
<td><p><strong>Field2</strong> オブジェクトに非 Null 値が必須かどうかを示す値を設定または取得します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-size-property-dao.md">サイズ</a></strong></p></td>
<td><p><strong>Field2</strong> オブジェクトの最大サイズをバイト数で示す値を設定または取得します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-sourcefield-property-dao.md">SourceField</a></strong></p></td>
<td><p><strong>Field2</strong> オブジェクトのデータの元のソースであるフィールドの名前を示す値を返します。値の取得のみ可能です。文字列型 ( <strong>String</strong>) の値を使用します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-sourcetable-property-dao.md">SourceTable</a></strong></p></td>
<td><p><strong>Field2</strong> オブジェクトのデータの元のソースであるテーブルの名前を示す値を返します。値の取得のみ可能です。文字列型 ( <strong>String</strong>) の値を使用します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-type-property-dao.md">型</a></strong></p></td>
<td><p>オブジェクトの操作の種類またはデータ型を示す値を設定または取得します。値の取得および設定が可能です。整数型 ( <strong>Integer</strong> ) の値を使用します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-validateonset-property-dao.md">ValidateOnSet</a></strong></p></td>
<td><p><strong>Field2</strong> オブジェクトの <strong>Value</strong> プロパティを設定するときに、このオブジェクトの値をすぐに検証するかどうかを指定する値を設定または取得します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-validationrule-property-dao.md">ValidationRule</a></strong></p></td>
<td><p>データの変更時またはテーブルへの追加時 (Microsoft Access ワークスペースのみ) に、フィールド内のデータを検証する値を設定または取得します。値の取得および設定が可能です。文字列型 ( <strong>String</strong>) の値を使用します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-validationtext-property-dao.md">ValidationText</a></strong></p></td>
<td><p><strong>Field2</strong> オブジェクトの値が <strong>ValidationRule</strong> プロパティに設定されている入力規則を満たさない場合に、アプリケーションに表示するメッセージのテキストを指定する値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得および設定が可能です。文字列型 ( <strong>String</strong>) の値を使用します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-value-property-dao.md">Value</a></strong></p></td>
<td><p>オブジェクトの値を設定します。値の取得および設定が可能です。バリアント型 ( <strong>Variant</strong>) の値を使用します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-visiblevalue-property-dao.md">VisibleValue</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</P>


<p>現在データベース内にある、バッチ更新の競合によって決まる <strong>OriginalValue</strong> プロパティより新しい値を取得します (ODBCDirect ワークスペースのみ)。</p></td>
</tr>
</tbody>
</table>

