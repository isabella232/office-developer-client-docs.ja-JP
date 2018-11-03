---
title: Field2 メンバー (DAO)
TOCTitle: Field2 Members
ms:assetid: 27829bbc-8b4e-c7eb-f29b-bcbef341f9fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191913(v=office.15)
ms:contentKeyID: 48543839
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f7d368077e94a24dfd7b3d20dcdaafb0ee7d3c84
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937793"
---
# <a name="field2-members-dao"></a><span data-ttu-id="50b7b-102">Field2 メンバー (DAO)</span><span class="sxs-lookup"><span data-stu-id="50b7b-102">Field2 members (DAO)</span></span>


<span data-ttu-id="50b7b-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="50b7b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="50b7b-104">Field2 オブジェクトは、共通のデータ型およびプロパティの共通セットを持つ、データの列を表します。</span><span class="sxs-lookup"><span data-stu-id="50b7b-104">A Field2 object represents a column of data with a common data type and a common set of properties.</span></span>

## <a name="methods"></a><span data-ttu-id="50b7b-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="50b7b-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="50b7b-106">名前</span><span class="sxs-lookup"><span data-stu-id="50b7b-106">Name</span></span></p></th>
<th><p><span data-ttu-id="50b7b-107">説明</span><span class="sxs-lookup"><span data-stu-id="50b7b-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50b7b-108"><strong><a href="field2-appendchunk-method-dao.md">AppendChunk</a></strong></span><span class="sxs-lookup"><span data-stu-id="50b7b-108"><strong><a href="field2-appendchunk-method-dao.md">AppendChunk</a></strong></span></span></p></td>
<td><p><span data-ttu-id="50b7b-109">文字列式からのデータを <a href="recordset-object-dao.md"><strong>Recordset</strong></a> の、メモ型 (Memo) またはロング バイナリ型 (Long Binary) の <strong>Field2</strong> オブジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="50b7b-109">Appends data from a string expression to a Memo or Long Binary <strong>Field2</strong> object in a <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b7b-110"><strong><a href="field2-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="50b7b-110"><strong><a href="field2-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="50b7b-111">新しいユーザー定義の <strong><a href="property-object-dao.md">Property</a></strong> オブジェクトを作成します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="50b7b-111">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b7b-112"><strong><a href="field2-getchunk-method-dao.md">GetChunk</a></strong></span><span class="sxs-lookup"><span data-stu-id="50b7b-112"><strong><a href="field2-getchunk-method-dao.md">GetChunk</a></strong></span></span></p></td>
<td><p><span data-ttu-id="50b7b-113">すべてを返します。 または<strong><a href="recordset-object-dao.md">Recordset</a></strong>オブジェクトの<strong><a href="fields-collection-dao.md">Fields</a></strong>コレクション内の<strong>メモ</strong>型または<strong>長の BinaryField2</strong>オブジェクトの内容の一部です。</span><span class="sxs-lookup"><span data-stu-id="50b7b-113">Returns all or a portion of the contents of a <strong>Memo</strong> or <strong>Long BinaryField2</strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b7b-114"><strong><a href="field2-loadfromfile-method-dao.md">LoadFromFile</a></strong></span><span class="sxs-lookup"><span data-stu-id="50b7b-114"><strong><a href="field2-loadfromfile-method-dao.md">LoadFromFile</a></strong></span></span></p></td>
<td><p><span data-ttu-id="50b7b-115">指定されたファイルをディスクから読み込みます。</span><span class="sxs-lookup"><span data-stu-id="50b7b-115">Loads the specified file from disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b7b-116"><strong><a href="field2-savetofile-method-dao.md">SaveToFile</a></strong></span><span class="sxs-lookup"><span data-stu-id="50b7b-116"><strong><a href="field2-savetofile-method-dao.md">SaveToFile</a></strong></span></span></p></td>
<td><p><span data-ttu-id="50b7b-p101">添付ファイルをディスクに保存します。</span><span class="sxs-lookup"><span data-stu-id="50b7b-p101">Saves an attachment to disk. .</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="50b7b-119">プロパティ</span><span class="sxs-lookup"><span data-stu-id="50b7b-119">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="50b7b-120">名前</span><span class="sxs-lookup"><span data-stu-id="50b7b-120">Name</span></span></p></th>
<th><p><span data-ttu-id="50b7b-121">説明</span><span class="sxs-lookup"><span data-stu-id="50b7b-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50b7b-122"><strong><a href="field2-allowzerolength-property-dao.md">AllowZeroLength</a></strong></span><span class="sxs-lookup"><span data-stu-id="50b7b-122"><strong><a href="field2-allowzerolength-property-dao.md">AllowZeroLength</a></strong></span></span></p></td>
<td><p><span data-ttu-id="50b7b-123">示す値を取得または設定かどうか、長さ 0 の文字列 (&quot;&quot;) は、テキスト型またはメモ型 (Microsoft Access ワークスペースのみ) の<strong>Field2</strong>オブジェクトの<strong><a href="field-value-property-dao.md">Value</a></strong>プロパティに有効な設定です。</span><span class="sxs-lookup"><span data-stu-id="50b7b-123">Sets or returns a value that indicates whether a zero-length string (&quot;&quot;) is a valid setting for the <strong><a href="field-value-property-dao.md">Value</a></strong> property of the <strong>Field2</strong> object with a Text or Memo data type (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b7b-124"><strong><a href="field2-appendonly-property-dao.md">AppendOnly</a></strong></span><span class="sxs-lookup"><span data-stu-id="50b7b-124"><strong><a href="field2-appendonly-property-dao.md">AppendOnly</a></strong></span></span></p></td>
<td><p><span data-ttu-id="50b7b-p102">指定されたフィールドについて、新しい値が追加されたときにその値をフィールドの既存の内容に付加するように設定されているかどうかを示すブール型 ( <strong>Boolean</strong>) の値を取得または設定します。値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="50b7b-p102">Gets or sets a <strong>Boolean</strong> that indicates whether the spcified field is set to append new values to the existing contents of the field as they are added. Read/write.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b7b-127"><strong><a href="field2-attributes-property-dao.md">Attributes</a></strong></span><span class="sxs-lookup"><span data-stu-id="50b7b-127"><strong><a href="field2-attributes-property-dao.md">Attributes</a></strong></span></span></p></td>
<td><p><span data-ttu-id="50b7b-p103"><strong>Field2</strong> オブジェクトの 1 つまたは複数の特性を示す値を設定または取得します。値の取得および設定が可能です。長整数型 ( <strong>Long</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="50b7b-p103">Sets or returns a value that indicates one or more characteristics of a <strong>Field2</strong> object. Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b7b-130"><strong><a href="field2-collatingorder-property-dao.md">照合順序</a></strong></span><span class="sxs-lookup"><span data-stu-id="50b7b-130"><strong><a href="field2-collatingorder-property-dao.md">CollatingOrder</a></strong></span></span></p></td>
<td><p><span data-ttu-id="50b7b-p104">文字列の比較または並べ替えのために、文字列の並べ替え順序を指定する値を返します (Microsoft Access ワークスペースのみ)。値の取得のみ可能です。長整数型 ( <strong>Long</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="50b7b-p104">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b7b-133"><strong><a href="field2-complextype-property-dao.md">ComplexType</a></strong></span><span class="sxs-lookup"><span data-stu-id="50b7b-133"><strong><a href="field2-complextype-property-dao.md">ComplexType</a></strong></span></span></p></td>
<td><p><span data-ttu-id="50b7b-p105">複数値を持つフィールドを表す <strong><a href="complextype-object-dao.md">ComplexType</a></strong> オブジェクトを返します。値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="50b7b-p105">Returns a <strong><a href="complextype-object-dao.md">ComplexType</a></strong> object that represents a multi-valued field. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b7b-136"><strong><a href="field2-dataupdatable-property-dao.md">DataUpdatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="50b7b-136"><strong><a href="field2-dataupdatable-property-dao.md">DataUpdatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="50b7b-137"><strong>Field2</strong> オブジェクトで表されるフィールドのデータが更新可能かどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="50b7b-137">Returns a value that indicates whether the data in the field represented by a <strong>Field2</strong> object is updatable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b7b-138"><strong><a href="field2-defaultvalue-property-dao.md">DefaultValue</a></strong></span><span class="sxs-lookup"><span data-stu-id="50b7b-138"><strong><a href="field2-defaultvalue-property-dao.md">DefaultValue</a></strong></span></span></p></td>
<td><p><span data-ttu-id="50b7b-p106"><strong>Field2</strong> オブジェクトの既定値を設定または取得します。 <a href="fields-collection-dao.md"><strong>Fields</strong></a> コレクションに追加されていない <strong>Field2</strong> オブジェクトの場合、このプロパティは値の取得および設定が可能です (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="50b7b-p106">Sets or returns the default value of a <strong>Field2</strong> object. For a <strong>Field2</strong> object not yet appended to the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection, this property is read/write (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b7b-141"><strong><a href="field2-expression-property-dao.md">Expression</a></strong></span><span class="sxs-lookup"><span data-stu-id="50b7b-141"><strong><a href="field2-expression-property-dao.md">Expression</a></strong></span></span></p></td>
<td><p><span data-ttu-id="50b7b-142">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="50b7b-142">Read/write</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b7b-143"><strong><a href="field2-fieldsize-property-dao.md">フィールド サイズします。</a></strong></span><span class="sxs-lookup"><span data-stu-id="50b7b-143"><strong><a href="field2-fieldsize-property-dao.md">FieldSize</a></strong></span></span></p></td>
<td><p><span data-ttu-id="50b7b-144">メモリではなくデータベースで使用される、 <a href="fields-collection-dao.md"><strong>Recordset</strong></a> オブジェクトの <a href="recordset-object-dao.md"><strong>Fields</strong></a> コレクションに含まれるメモ型 (Memo) またはロング バイナリ型 (Long Binary) の <strong>Field2</strong> オブジェクトのバイト数を返します。</span><span class="sxs-lookup"><span data-stu-id="50b7b-144">Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary <strong>Field2</strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b7b-145"><strong><a href="field2-foreignname-property-dao.md">ForeignName</a></strong></span><span class="sxs-lookup"><span data-stu-id="50b7b-145"><strong><a href="field2-foreignname-property-dao.md">ForeignName</a></strong></span></span></p></td>
<td><p><span data-ttu-id="50b7b-146">あるリレーションシップにおいて、主テーブルのフィールドに対応する外部キー側のテーブルの <strong>Field2</strong> オブジェクトの名前を指定する値を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="50b7b-146">Sets or returns a value that specifies the name of the <strong>Field2</strong> object in a foreign table that corresponds to a field in a primary table for a relationship (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b7b-147"><strong><a href="field2-iscomplex-property-dao.md">IsComplex</a></strong></span><span class="sxs-lookup"><span data-stu-id="50b7b-147"><strong><a href="field2-iscomplex-property-dao.md">IsComplex</a></strong></span></span></p></td>
<td><p><span data-ttu-id="50b7b-p107">指定されたフィールドが複数値データ型かどうかを示すブール型 ( <strong>Boolean</strong>) の値を返します。値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="50b7b-p107">Returns <strong>Boolean</strong> that indicates whether the specified field is a multi-valued data type. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b7b-150"><strong><a href="field2-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="50b7b-150"><strong><a href="field2-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="50b7b-p108">指定したオブジェクトの名前を取得または設定します。オブジェクトがコレクションに追加されていない場合、値の取得および設定が可能です。文字列型 ( <strong>String</strong>) の値を使用します。オブジェクトがコレクションに追加されている場合、値の取得のみ可能です。文字列型 ( <strong>String</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="50b7b-p108">Returns or sets the name of the specified object. Read/write <strong>String</strong> if the object has not been appended to a collection. Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b7b-154"><strong><a href="field2-ordinalposition-property-dao.md">OrdinalPosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="50b7b-154"><strong><a href="field2-ordinalposition-property-dao.md">OrdinalPosition</a></strong></span></span></p></td>
<td><p><span data-ttu-id="50b7b-p109"><a href="fields-collection-dao.md"><strong>Fields</strong></a> コレクション内の <strong>Field2</strong> オブジェクトの相対位置を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="50b7b-p109">Sets or returns the relative position of a <strong>Field2</strong> object within a <strong><a href="fields-collection-dao.md">Fields</a></strong> collection. .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b7b-157"><strong><a href="field2-originalvalue-property-dao.md">OriginalValue</a></strong></span><span class="sxs-lookup"><span data-stu-id="50b7b-157"><strong><a href="field2-originalvalue-property-dao.md">OriginalValue</a></strong></span></span></p></td>
<td><p><span data-ttu-id="50b7b-158"><strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> 値の 1 つ。</span><span class="sxs-lookup"><span data-stu-id="50b7b-158">One of the <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> values.</span></span></p>
<td><p><span data-ttu-id="50b7b-159"><strong>注</strong>: Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="50b7b-159"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="50b7b-160">Microsoft Office Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="50b7b-160">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="50b7b-161">最後のバッチ更新が開始されたときに存在したデータベースの <strong>Field2</strong> の値を返します (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="50b7b-161">Returns the value of a <strong>Field2</strong> in the database that existed when the last batch update began (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b7b-162"><strong><a href="field2-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="50b7b-162"><strong><a href="field2-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="50b7b-p111">指定したオブジェクトの <strong><a href="properties-collection-dao.md">Properties</a></strong> コレクションを取得します。値の取得のみ可能です。  </span><span class="sxs-lookup"><span data-stu-id="50b7b-p111">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b7b-165"><strong><a href="field2-required-property-dao.md">必須</a></strong></span><span class="sxs-lookup"><span data-stu-id="50b7b-165"><strong><a href="field2-required-property-dao.md">Required</a></strong></span></span></p></td>
<td><p><span data-ttu-id="50b7b-166"><strong>Field2</strong> オブジェクトに非 Null 値が必須かどうかを示す値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="50b7b-166">Sets or returns a value that indicates whether a <strong>Field2</strong> object requires a non-Null value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b7b-167"><strong><a href="field2-size-property-dao.md">サイズ</a></strong></span><span class="sxs-lookup"><span data-stu-id="50b7b-167"><strong><a href="field2-size-property-dao.md">Size</a></strong></span></span></p></td>
<td><p><span data-ttu-id="50b7b-168"><strong>Field2</strong> オブジェクトの最大サイズをバイト数で示す値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="50b7b-168">Sets or returns a value that indicates the maximum size, in bytes, of a <strong>Field2</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b7b-169"><strong><a href="field2-sourcefield-property-dao.md">SourceField</a></strong></span><span class="sxs-lookup"><span data-stu-id="50b7b-169"><strong><a href="field2-sourcefield-property-dao.md">SourceField</a></strong></span></span></p></td>
<td><p><span data-ttu-id="50b7b-p112"><strong>Field2</strong> オブジェクトのデータの元のソースであるフィールドの名前を示す値を返します。値の取得のみ可能です。文字列型 ( <strong>String</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="50b7b-p112">Returns a value that indicates the name of the field that is the original source of the data for a <strong>Field2</strong> object. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b7b-172"><strong><a href="field2-sourcetable-property-dao.md">SourceTable</a></strong></span><span class="sxs-lookup"><span data-stu-id="50b7b-172"><strong><a href="field2-sourcetable-property-dao.md">SourceTable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="50b7b-p113"><strong>Field2</strong> オブジェクトのデータの元のソースであるテーブルの名前を示す値を返します。値の取得のみ可能です。文字列型 ( <strong>String</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="50b7b-p113">Returns a value that indicates the name of the table that is the original source of the data for a <strong>Field2</strong> object. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b7b-175"><strong><a href="field2-type-property-dao.md">型</a></strong></span><span class="sxs-lookup"><span data-stu-id="50b7b-175"><strong><a href="field2-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="50b7b-p114">オブジェクトの操作の種類またはデータ型を示す値を設定または取得します。値の取得および設定が可能です。整数型 ( <strong>Integer</strong> ) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="50b7b-p114">Sets or returns a value that indicates the operational type or data type of an object. Read/write <strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b7b-178"><strong><a href="field2-validateonset-property-dao.md">ValidateOnSet</a></strong></span><span class="sxs-lookup"><span data-stu-id="50b7b-178"><strong><a href="field2-validateonset-property-dao.md">ValidateOnSet</a></strong></span></span></p></td>
<td><p><span data-ttu-id="50b7b-179"><strong>Field2</strong> オブジェクトの <strong>Value</strong> プロパティを設定するときに、このオブジェクトの値をすぐに検証するかどうかを指定する値を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="50b7b-179">Sets or returns a value that specifies whether or not the value of a <strong>Field2</strong> object is immediately validated when the object's <strong>Value</strong> property is set (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b7b-180"><strong><a href="field2-validationrule-property-dao.md">ValidationRule</a></strong></span><span class="sxs-lookup"><span data-stu-id="50b7b-180"><strong><a href="field2-validationrule-property-dao.md">ValidationRule</a></strong></span></span></p></td>
<td><p><span data-ttu-id="50b7b-p115">データの変更時またはテーブルへの追加時 (Microsoft Access ワークスペースのみ) に、フィールド内のデータを検証する値を設定または取得します。値の取得および設定が可能です。文字列型 ( <strong>String</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="50b7b-p115">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only). Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b7b-183"><strong><a href="field2-validationtext-property-dao.md">ValidationText</a></strong></span><span class="sxs-lookup"><span data-stu-id="50b7b-183"><strong><a href="field2-validationtext-property-dao.md">ValidationText</a></strong></span></span></p></td>
<td><p><span data-ttu-id="50b7b-p116"><strong>Field2</strong> オブジェクトの値が <strong>ValidationRule</strong> プロパティに設定されている入力規則を満たさない場合に、アプリケーションに表示するメッセージのテキストを指定する値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得および設定が可能です。文字列型 ( <strong>String</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="50b7b-p116">Sets or returns a value that specifies the text of the message that your application displays if the value of a <strong>Field2</strong> object doesn't satisfy the validation rule specified by the <strong>ValidationRule</strong> property setting (Microsoft Access workspaces only). Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50b7b-186"><strong><a href="field2-value-property-dao.md">Value</a></strong></span><span class="sxs-lookup"><span data-stu-id="50b7b-186"><strong><a href="field2-value-property-dao.md">Value</a></strong></span></span></p></td>
<td><p><span data-ttu-id="50b7b-p117">オブジェクトの値を設定します。値の取得および設定が可能です。バリアント型 ( <strong>Variant</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="50b7b-p117">Sets or returns the value of an object. Read/write <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50b7b-189"><strong><a href="field2-visiblevalue-property-dao.md">VisibleValue</a></strong></span><span class="sxs-lookup"><span data-stu-id="50b7b-189"><strong><a href="field2-visiblevalue-property-dao.md">VisibleValue</a></strong></span></span></p></td>
<td><p><span data-ttu-id="50b7b-190"><strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> 値の 1 つ。</span><span class="sxs-lookup"><span data-stu-id="50b7b-190">One of the <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> values.</span></span></p>
<td><p><span data-ttu-id="50b7b-191"><strong>注</strong>: Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="50b7b-191"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="50b7b-192">Microsoft Office Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="50b7b-192">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="50b7b-193">現在データベース内にある、バッチ更新の競合によって決まる <strong>OriginalValue</strong> プロパティより新しい値を取得します (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="50b7b-193">Returns a value currently in the database that is newer than the <strong>OriginalValue</strong> property as determined by a batch update conflict (ODBCDirect workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>

