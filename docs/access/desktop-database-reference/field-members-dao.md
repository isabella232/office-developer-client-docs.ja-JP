---
title: フィールド メンバー (DAO)
TOCTitle: Field Members
ms:assetid: 4b6a587f-1fd0-37fb-db7d-75b587a8dc60
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193511(v=office.15)
ms:contentKeyID: 48544689
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 497c0375496310c27c134792e01bd17e5533a452
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922203"
---
# <a name="field-members-dao"></a><span data-ttu-id="293a6-102">フィールド メンバー (DAO)</span><span class="sxs-lookup"><span data-stu-id="293a6-102">Field members (DAO)</span></span>


<span data-ttu-id="293a6-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="293a6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="293a6-104">Field オブジェクトは、共通のデータ型およびプロパティの共通セットを持つ、データの列を表します。</span><span class="sxs-lookup"><span data-stu-id="293a6-104">A Field object represents a column of data with a common data type and a common set of properties.</span></span>

## <a name="methods"></a><span data-ttu-id="293a6-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="293a6-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="293a6-106">名前</span><span class="sxs-lookup"><span data-stu-id="293a6-106">Name</span></span></p></th>
<th><p><span data-ttu-id="293a6-107">説明</span><span class="sxs-lookup"><span data-stu-id="293a6-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="293a6-108"><strong><a href="field-appendchunk-method-dao.md">AppendChunk</a></strong></span><span class="sxs-lookup"><span data-stu-id="293a6-108"><strong><a href="field-appendchunk-method-dao.md">AppendChunk</a></strong></span></span></p></td>
<td><p><span data-ttu-id="293a6-109">文字列式から <strong><a href="field-object-dao.md">Recordset</a></strong> のメモ型 (Memo) またはロング バイナリ型 (Long Binary) の <strong><a href="recordset-object-dao.md">Field</a></strong> オブジェクトにデータを追加します。</span><span class="sxs-lookup"><span data-stu-id="293a6-109">Appends data from a string expression to a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in a <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="293a6-110"><strong><a href="field-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="293a6-110"><strong><a href="field-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="293a6-111">新しいユーザー定義の <strong><a href="property-object-dao.md">Property</a></strong> オブジェクトを作成します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="293a6-111">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="293a6-112"><strong><a href="field-getchunk-method-dao.md">GetChunk</a></strong></span><span class="sxs-lookup"><span data-stu-id="293a6-112"><strong><a href="field-getchunk-method-dao.md">GetChunk</a></strong></span></span></p></td>
<td><p><span data-ttu-id="293a6-113"><strong><strong>Recordset</strong></strong> オブジェクトの <strong><a href="field-object-dao.md">Fields</a></strong> コレクションに含まれる、メモ型 ( <a href="fields-collection-dao.md">Memo</a>) またはロング バイナリ型 ( <strong>Long Binary</strong>) の <strong><a href="recordset-object-dao.md">Field</a></strong> オブジェクトについて、全部または一部の内容を取得します。</span><span class="sxs-lookup"><span data-stu-id="293a6-113">Returns all or a portion of the contents of a <strong>Memo</strong> or <strong>Long Binary</strong> <strong><a href="field-object-dao.md">Field</a></strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="293a6-114">プロパティ</span><span class="sxs-lookup"><span data-stu-id="293a6-114">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="293a6-115">名前</span><span class="sxs-lookup"><span data-stu-id="293a6-115">Name</span></span></p></th>
<th><p><span data-ttu-id="293a6-116">説明</span><span class="sxs-lookup"><span data-stu-id="293a6-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="293a6-117"><strong><a href="field-allowzerolength-property-dao.md">AllowZeroLength</a></strong></span><span class="sxs-lookup"><span data-stu-id="293a6-117"><strong><a href="field-allowzerolength-property-dao.md">AllowZeroLength</a></strong></span></span></p></td>
<td><p><span data-ttu-id="293a6-118">示す値を取得または設定かどうか、長さ 0 の文字列 (&quot;&quot;) は、テキスト型またはメモ型 (Microsoft Access ワークスペースのみ) の<strong><a href="field-object-dao.md">Field</a></strong>オブジェクトの<strong><a href="field-value-property-dao.md">Value</a></strong>プロパティに有効な設定です。</span><span class="sxs-lookup"><span data-stu-id="293a6-118">Sets or returns a value that indicates whether a zero-length string (&quot;&quot;) is a valid setting for the <strong><a href="field-value-property-dao.md">Value</a></strong> property of the <strong><a href="field-object-dao.md">Field</a></strong> object with a Text or Memo data type (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="293a6-119"><strong><a href="field-attributes-property-dao.md">Attributes</a></strong></span><span class="sxs-lookup"><span data-stu-id="293a6-119"><strong><a href="field-attributes-property-dao.md">Attributes</a></strong></span></span></p></td>
<td><p><span data-ttu-id="293a6-p101"><strong><a href="field-object-dao.md">Field</a></strong> オブジェクトの 1 つまたは複数の特性を示す値を設定または取得します。値の取得および設定が可能です。長整数型 ( <strong>Long</strong> ) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="293a6-p101">Sets or returns a value that indicates one or more characteristics of a <strong><a href="field-object-dao.md">Field</a></strong> object. Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="293a6-122"><strong><a href="field-collatingorder-property-dao.md">照合順序</a></strong></span><span class="sxs-lookup"><span data-stu-id="293a6-122"><strong><a href="field-collatingorder-property-dao.md">CollatingOrder</a></strong></span></span></p></td>
<td><p><span data-ttu-id="293a6-p102">文字列の比較または並べ替えのために、文字列の並べ替え順序を指定する値を返します (Microsoft Access ワークスペースのみ)。値の取得のみ可能です。長整数型 ( <strong>Long</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="293a6-p102">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="293a6-125"><strong><a href="field-dataupdatable-property-dao.md">DataUpdatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="293a6-125"><strong><a href="field-dataupdatable-property-dao.md">DataUpdatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="293a6-126"><strong><a href="field-object-dao.md">Field</a></strong> オブジェクトで表されるフィールドのデータが更新可能かどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="293a6-126">Returns a value that indicates whether the data in the field represented by a <strong><a href="field-object-dao.md">Field</a></strong> object is updatable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="293a6-127"><strong><a href="field-defaultvalue-property-dao.md">DefaultValue</a></strong></span><span class="sxs-lookup"><span data-stu-id="293a6-127"><strong><a href="field-defaultvalue-property-dao.md">DefaultValue</a></strong></span></span></p></td>
<td><p><span data-ttu-id="293a6-p103"><strong><a href="field-object-dao.md">Field</a></strong> オブジェクトの既定値を設定または取得します。 <a href="fields-collection-dao.md"><strong>Fields</strong></a> コレクションにまだ追加されていない <strong>Field</strong> オブジェクトの場合、このプロパティは値の取得および設定が可能です (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="293a6-p103">Sets or returns the default value of a <strong><a href="field-object-dao.md">Field</a></strong> object. For a <strong>Field</strong> object not yet appended to the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection, this property is read/write (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="293a6-130"><strong><a href="field-fieldsize-property-dao.md">フィールド サイズします。</a></strong></span><span class="sxs-lookup"><span data-stu-id="293a6-130"><strong><a href="field-fieldsize-property-dao.md">FieldSize</a></strong></span></span></p></td>
<td><p><span data-ttu-id="293a6-131"><strong><a href="field-object-dao.md">Recordset</a></strong> オブジェクトの <strong><a href="fields-collection-dao.md">Fields</a></strong> コレクション内にあるメモ型 (Memo) またはロング バイナリ型 (Long Binary) の <strong><a href="recordset-object-dao.md">Field</a></strong> オブジェクトを、メモリではなくデータベースで使用する場合のバイト数を取得します。</span><span class="sxs-lookup"><span data-stu-id="293a6-131">Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="293a6-132"><strong><a href="field-foreignname-property-dao.md">ForeignName</a></strong></span><span class="sxs-lookup"><span data-stu-id="293a6-132"><strong><a href="field-foreignname-property-dao.md">ForeignName</a></strong></span></span></p></td>
<td><p><span data-ttu-id="293a6-133">リレーションシップの主テーブルのフィールドに対応する、外部キー側のテーブルの <strong><a href="field-object-dao.md">Field</a></strong> オブジェクトの名前を指定する値を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="293a6-133">Sets or returns a value that specifies the name of the <strong><a href="field-object-dao.md">Field</a></strong> object in a foreign table that corresponds to a field in a primary table for a relationship (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="293a6-134"><strong><a href="field-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="293a6-134"><strong><a href="field-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="293a6-p104">指定したオブジェクトの名前を取得または設定します。オブジェクトがコレクションに追加されていない場合、値の取得および設定が可能です。文字列型 ( <strong>String</strong>) の値を使用します。オブジェクトがコレクションに追加されている場合、値の取得のみ可能です。文字列型 ( <strong>String</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="293a6-p104">Returns or sets the name of the specified object. Read/write <strong>String</strong> if the object has not been appended to a collection. Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="293a6-138"><strong><a href="field-ordinalposition-property-dao.md">OrdinalPosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="293a6-138"><strong><a href="field-ordinalposition-property-dao.md">OrdinalPosition</a></strong></span></span></p></td>
<td><p><span data-ttu-id="293a6-p105"><strong><a href="field-object-dao.md">Fields</a></strong> コレクション内の <strong><a href="fields-collection-dao.md">Field</a></strong> オブジェクトの相対位置を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="293a6-p105">Sets or returns the relative position of a <strong><a href="field-object-dao.md">Field</a></strong> object within a <strong><a href="fields-collection-dao.md">Fields</a></strong> collection. .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="293a6-141"><strong><a href="field-originalvalue-property-dao.md">OriginalValue</a></strong></span><span class="sxs-lookup"><span data-stu-id="293a6-141"><strong><a href="field-originalvalue-property-dao.md">OriginalValue</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <span data-ttu-id="293a6-p106">[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="293a6-p106">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p><span data-ttu-id="293a6-144">最後のバッチ更新を開始したときにデータベース内に存在した <strong>Field</strong> オブジェクトの値を取得します (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="293a6-144">Returns the value of a <strong>Field</strong> in the database that existed when the last batch update began (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="293a6-145"><strong><a href="field-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="293a6-145"><strong><a href="field-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="293a6-p107">指定したオブジェクトの <strong><a href="properties-collection-dao.md">Properties</a></strong> コレクションを取得します。値の取得のみ可能です。  </span><span class="sxs-lookup"><span data-stu-id="293a6-p107">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="293a6-148"><strong><a href="field-required-property-dao.md">必須</a></strong></span><span class="sxs-lookup"><span data-stu-id="293a6-148"><strong><a href="field-required-property-dao.md">Required</a></strong></span></span></p></td>
<td><p><span data-ttu-id="293a6-149"><strong><a href="field-object-dao.md">Field</a></strong> オブジェクトに非 Null 値が必要かどうかを示す値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="293a6-149">Sets or returns a value that indicates whether a <strong><a href="field-object-dao.md">Field</a></strong> object requires a non-Null value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="293a6-150"><strong><a href="field-fieldsize-property-dao.md">サイズ</a></strong></span><span class="sxs-lookup"><span data-stu-id="293a6-150"><strong><a href="field-fieldsize-property-dao.md">Size</a></strong></span></span></p></td>
<td><p><span data-ttu-id="293a6-151"><strong><a href="field-object-dao.md">Recordset</a></strong> オブジェクトの <strong><a href="fields-collection-dao.md">Fields</a></strong> コレクション内にあるメモ型 (Memo) またはロング バイナリ型 (Long Binary) の <strong><a href="recordset-object-dao.md">Field</a></strong> オブジェクトを、メモリではなくデータベースで使用する場合のバイト数を取得します。</span><span class="sxs-lookup"><span data-stu-id="293a6-151">Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="293a6-152"><strong><a href="field-sourcefield-property-dao.md">SourceField</a></strong></span><span class="sxs-lookup"><span data-stu-id="293a6-152"><strong><a href="field-sourcefield-property-dao.md">SourceField</a></strong></span></span></p></td>
<td><p><span data-ttu-id="293a6-p108"><strong>Field</strong> オブジェクトの元のデータ ソースであるフィールド名を示す値を取得します。値の取得のみ可能です。文字列型 ( <strong>String</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="293a6-p108">Returns a value that indicates the name of the field that is the original source of the data for a <strong>Field</strong> object. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="293a6-155"><strong><a href="field-sourcetable-property-dao.md">SourceTable</a></strong></span><span class="sxs-lookup"><span data-stu-id="293a6-155"><strong><a href="field-sourcetable-property-dao.md">SourceTable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="293a6-p109"><strong>Field</strong> オブジェクトの元のデータ ソースとなるテーブルの名前を示す値を取得します。値の取得のみ可能です。文字列型 ( <strong>String</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="293a6-p109">Returns a value that indicates the name of the table that is the original source of the data for a <strong>Field</strong> object. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="293a6-158"><strong><a href="field-type-property-dao.md">型</a></strong></span><span class="sxs-lookup"><span data-stu-id="293a6-158"><strong><a href="field-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="293a6-p110">オブジェクトの操作の種類またはデータ型を示す値を設定または取得します。値の取得および設定が可能です。整数型 ( <strong>Integer</strong> ) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="293a6-p110">Sets or returns a value that indicates the operational type or data type of an object. Read/write <strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="293a6-161"><strong><a href="field-validateonset-property-dao.md">ValidateOnSet</a></strong></span><span class="sxs-lookup"><span data-stu-id="293a6-161"><strong><a href="field-validateonset-property-dao.md">ValidateOnSet</a></strong></span></span></p></td>
<td><p><span data-ttu-id="293a6-162">オブジェクトの <strong><a href="field-object-dao.md">Value</a></strong> プロパティの設定時に、 <strong><a href="field-value-property-dao.md">Field</a></strong> オブジェクトの値を直ちに検証するかどうかを指定する値を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="293a6-162">Sets or returns a value that specifies whether or not the value of a <strong><a href="field-object-dao.md">Field</a></strong> object is immediately validated when the object's <strong><a href="field-value-property-dao.md">Value</a></strong> property is set (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="293a6-163"><strong><a href="field-validationrule-property-dao.md">ValidationRule</a></strong></span><span class="sxs-lookup"><span data-stu-id="293a6-163"><strong><a href="field-validationrule-property-dao.md">ValidationRule</a></strong></span></span></p></td>
<td><p><span data-ttu-id="293a6-p111">データの変更時またはテーブルへの追加時 (Microsoft Access ワークスペースのみ) に、フィールド内のデータを検証する値を設定または取得します。値の取得および設定が可能です。文字列型 ( <strong>String</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="293a6-p111">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only). Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="293a6-166"><strong><a href="field-validationtext-property-dao.md">ValidationText</a></strong></span><span class="sxs-lookup"><span data-stu-id="293a6-166"><strong><a href="field-validationtext-property-dao.md">ValidationText</a></strong></span></span></p></td>
<td><p><span data-ttu-id="293a6-p112"><strong>Field</strong> オブジェクトの値が <strong>ValidationRule</strong> プロパティに設定されている入力規則を満たさない場合に、アプリケーションに表示するメッセージのテキストを指定する値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得および設定が可能です。文字列型 ( <strong>String</strong> ) の値を使用します。  </span><span class="sxs-lookup"><span data-stu-id="293a6-p112">Sets or returns a value that specifies the text of the message that your application displays if the value of a <strong>Field</strong> object doesn't satisfy the validation rule specified by the <strong>ValidationRule</strong> property setting (Microsoft Access workspaces only). Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="293a6-169"><strong><a href="field-value-property-dao.md">Value</a></strong></span><span class="sxs-lookup"><span data-stu-id="293a6-169"><strong><a href="field-value-property-dao.md">Value</a></strong></span></span></p></td>
<td><p><span data-ttu-id="293a6-p113">オブジェクトの値を設定します。値の取得および設定が可能です。バリアント型 ( <strong>Variant</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="293a6-p113">Sets or returns the value of an object. Read/write <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="293a6-172"><strong><a href="field-visiblevalue-property-dao.md">VisibleValue</a></strong></span><span class="sxs-lookup"><span data-stu-id="293a6-172"><strong><a href="field-visiblevalue-property-dao.md">VisibleValue</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <span data-ttu-id="293a6-p114">[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="293a6-p114">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p><span data-ttu-id="293a6-175">現在データベース内にある、バッチ更新の競合によって決まる <strong>OriginalValue</strong> プロパティより新しい値を取得します (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="293a6-175">Returns a value currently in the database that is newer than the <strong>OriginalValue</strong> property as determined by a batch update conflict (ODBCDirect workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>

