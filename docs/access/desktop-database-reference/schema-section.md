---
title: スキーマ セクション (アクセス デスクトップ データベース参照)
TOCTitle: Schema Section
ms:assetid: 59b42ffb-0524-adc3-8bcd-6e4cd2c505ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249304(v=office.15)
ms:contentKeyID: 48545023
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fd1a67ebd992d90abf182c042bd3d68a6d0d4ce2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479028"
---
# <a name="schema-section"></a><span data-ttu-id="99dc8-102">Schema セクション</span><span class="sxs-lookup"><span data-stu-id="99dc8-102">Schema Section</span></span>

<span data-ttu-id="99dc8-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="99dc8-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="schema-section"></a><span data-ttu-id="99dc8-104">Schema セクション</span><span class="sxs-lookup"><span data-stu-id="99dc8-104">Schema Section</span></span>

<span data-ttu-id="99dc8-p101">Schema セクションは必須です。前の例で示したように、ADO は各列に関する詳細なメタデータを書き込んで、データ値の形式を更新用にできる限り多く保持します。ただし、XML で読み込むには、ADO は、列の名前およびその列が属する行セットのみを必要とします。次に、最小のスキーマの例を示します。</span><span class="sxs-lookup"><span data-stu-id="99dc8-p101">The schema section is required. As the previous example shows, ADO writes out detailed metadata about each column to preserve the semantics of the data values as much as possible for updating. However, to load in the XML, ADO only requires the names of the columns and the rowset to which they belong. Here is an example of a minimal schema:</span></span>

```xml 
 
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882" 
    xmlns:rs="urn:schemas-microsoft-com:rowset" 
    xmlns:z="#RowsetSchema"> 
  <s:Schema id="RowsetSchema"> 
    <s:ElementType name="row" content="eltOnly"> 
      <s:AttributeType name="ShipperID"/> 
      <s:AttributeType name="CompanyName"/> 
      <s:AttributeType name="Phone"/> 
      <s:Extends type="rs:rowbase"/> 
    </s:ElementType> 
  </s:Schema> 
  <rs:data> 
... 
  </rs:data> 
</xml> 
```

<span data-ttu-id="99dc8-109">上記の例では、スキーマにデータ型情報が含まれていないため、ADO はデータを可変長文字列として扱います。</span><span class="sxs-lookup"><span data-stu-id="99dc8-109">In the case above, ADO will treat the data as variable length strings because no type information is included in the schema.</span></span>

## <a name="creating-aliases-for-column-names"></a><span data-ttu-id="99dc8-110">列名のエイリアスの作成</span><span class="sxs-lookup"><span data-stu-id="99dc8-110">Creating Aliases for Column Names</span></span>

<span data-ttu-id="99dc8-p102">**rs:name** 属性を使用すると、列名のエイリアスを作成して、行セットに表示される列情報をわかりやすい名前で表示し、データ セクションに短縮名を表示できます。たとえば、上記のスキーマを次のように変更して、ShipperID を s1 に、CompanyName を s2 に、Phone を s3 にマップできます。</span><span class="sxs-lookup"><span data-stu-id="99dc8-p102">The **rs:name** attribute allows you to create an alias for a column name so that a friendly name may appear in the column information exposed by the rowset and a shorter name may be used in the data section. For example, the schema above could be modified to map ShipperID to s1, CompanyName to s2, and Phone to s3 as follows:</span></span>

```xml 
 
<s:Schema id="RowsetSchema">  
<s:ElementType name="row" content="eltOnly" rs:updatable="true">  
<s:AttributeType name="s1" rs:name="ShipperID" rs:number="1" ...>  
... 
</s:AttributeType>  
<s:AttributeType name="s2" rs:name="CompanyName" rs:number="2" ...>  
... 
</s:AttributeType>  
<s:AttributeType name="s3" rs:name="Phone" rs:number="3" ...>  
... 
</s:AttributeType>  
... 
</s:ElementType>  
</s:Schema>  
```

<span data-ttu-id="99dc8-113">次に、データ セクションでは、行は **rs:name** ではなく **name** 属性を使用して列を参照します。</span><span class="sxs-lookup"><span data-stu-id="99dc8-113">Then, in the data section, the row would use the **name** attribute (not **rs:name**) to refer to that column:</span></span>

```xml 
 
"<row s1="1" s2="Speedy Express" s3="(503) 555-9831"/> 
```

<span data-ttu-id="99dc8-p103">列名が有効な属性または XML のタグ名ではない場合は、必ず列名のエイリアスを作成する必要があります。たとえば、スペースが含まれる名前は無効な属性のため、"Last Name" にはエイリアスが必要です。次の行は XML パーサーでは正しく処理されないため、エイリアスを作成して、スペースを含まない他の名前にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="99dc8-p103">Creating aliases for column names is required whenever a column name is not a legal attribute or tag name in XML. For example, "Last Name" must have an alias because names with embedded spaces are illegal attributes. The following line won't be correctly handled by the XML parser, so you must create an alias to some other name that does not have an embedded space:</span></span>

```xml 
 
<row last name="Jones"/> 
```

<span data-ttu-id="99dc8-p104">**name** 属性に使用する値は、XML ドキュメントのスキーマとデータ セクションの両方の列が参照される各箇所で、一貫して使用する必要があります。次の例に、s1 の一貫した使用を示します。</span><span class="sxs-lookup"><span data-stu-id="99dc8-p104">Whatever value you use for the **name** attribute must be used consistently in each place that the column is referenced in both the schema and data sections of the XML document. The following example shows the consistent use of s1:</span></span>

```xml 
 
<s:Schema id="RowsetSchema"> 
  <s:ElementType name="row" content="eltOnly"> 
    <s:attribute type="s1"/> 
    <s:attribute type="CompanyName"/> 
    <s:attribute type="s3"/> 
    <s:extends type="rs:rowbase"/> 
  </s:ElementType> 
  <s:AttributeType name="s1" rs:name="ShipperID" rs:number="1"  
    rs:maydefer="true" rs:writeunknown="true"> 
    <s:datatype dt:type="i4" dt:maxLength="4" rs:precision="10"  
      rs:fixedlength="true" rs:maybenull="true"/> 
  </s:AttributeType> 
</s:Schema> 
<rs:data> 
  <z:row s1="1" CompanyName="Speedy Express" s3="(503) 555-9831"/> 
</rs:data> 
```

<span data-ttu-id="99dc8-119">同様に、上記の CompanyName にはエイリアスが定義されていないため、ドキュメント全体で CompanyName を一貫して使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="99dc8-119">Similarly, because there is no alias defined for CompanyName above, CompanyName must be used consistently throughout the document.</span></span>

## <a name="data-types"></a><span data-ttu-id="99dc8-120">データ型</span><span class="sxs-lookup"><span data-stu-id="99dc8-120">Data Types</span></span>

<span data-ttu-id="99dc8-p105">**dt:type** 属性を使用して、列にデータ型を適用できます。データ型を指定するには、列定義自体で **dt:type** 属性を直接指定するか、列定義の入れ子にされた要素として **s:datatype** コンストラクトを使用します。次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="99dc8-p105">You can apply a data type to a column with the **dt:type** attribute. You can specify a data type in two ways: either specify the **dt:type** attribute directly on the column definition itself or use the **s:datatype** construct as a nested element of the column definition. For example,</span></span>

```xml 
 
<s:AttributeType name="Phone" > 
  <s:datatype dt:type="string"/> 
</s:AttributeType> 
```

<span data-ttu-id="99dc8-124">これは、次と同等です。</span><span class="sxs-lookup"><span data-stu-id="99dc8-124">is equivalent to</span></span>

```xml 
 
<s:AttributeType name="Phone" dt:type="string"/> 
```

<span data-ttu-id="99dc8-125">行定義全体から **dt:type** 属性を省略すると、既定では、列の型は可変長文字列になります。</span><span class="sxs-lookup"><span data-stu-id="99dc8-125">If you omit the **dt:type** attribute entirely from the row definition, by default, the column's type will be a variable length string.</span></span>

<span data-ttu-id="99dc8-p106">型の名前 (**dt:maxLength** など) 以外に、型に関するより詳細な情報があると、**s:datatype** 子要素を使用してさらに読みやすくできます。ただし、これは単なる慣習であり、必要条件ではありません。</span><span class="sxs-lookup"><span data-stu-id="99dc8-p106">If you have more type information than simply the type name (for example, **dt:maxLength**), it makes it more readable to use the **s:datatype** child element. This is merely a convention, however, and not a requirement.</span></span>

<span data-ttu-id="99dc8-128">次の例に、スキーマに型情報を含める方法を詳しく示します。</span><span class="sxs-lookup"><span data-stu-id="99dc8-128">The following examples show further how to include type information in your schema:</span></span>

```xml 
 
<!-- 1. String with no max length --> 
<s:AttributeType name="title_id"/> 
<! — or --> 
<s:AttributeType name="title_id" dt:type="string"/> 
 
<! — 2. Fixed length string with max length of 6 --> 
<s:AttributeType name="title_id"> 
    <s:datatype dt:type="string" dt:maxLength="6" rs:fixedlength="true" /> 
</s:AttributeType> 
 
<! — 3. Variable length string with max length of 6 --> 
<s:AttributeType name="title_id"> 
    <s:datatype dt:type="string" dt:maxLength="6" /> 
</s:AttributeType> 
 
<! — 4. Integer --> 
<s:AttributeType name="title_id" dt:type="int"/> 
```

<span data-ttu-id="99dc8-129">2 番目の例では、 **rs:fixedlength** 属性を細部で使用しています。</span><span class="sxs-lookup"><span data-stu-id="99dc8-129">There is a subtle use of the **rs:fixedlength** attribute in the second example.</span></span> <span data-ttu-id="99dc8-130">**rs:fixedlength** 属性が true に設定されている列は、そのデータにはスキーマで定義されている長さが必要だということを示しています。</span><span class="sxs-lookup"><span data-stu-id="99dc8-130">A column with the **rs:fixedlength** attribute set to true means that the data must have the length defined in the schema.</span></span> <span data-ttu-id="99dc8-131">タイトルの法律がこの例では、値\_id は、"123456 または"「123」</span><span class="sxs-lookup"><span data-stu-id="99dc8-131">In this case, a legal value for title\_id is "123456," as is "123 ."</span></span> <span data-ttu-id="99dc8-132">"123" は長さが 6 ではなく 3 のため有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="99dc8-132">However, "123" would not be valid because its length is 3, not 6.</span></span> <span data-ttu-id="99dc8-133">**fixedlength** プロパティの詳細については、「OLE DB Programmer's Guide」 (英語) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="99dc8-133">See the OLE DB Programmer's Guide for a more complete description of the **fixedlength** property.</span></span>

## <a name="handling-nulls"></a><span data-ttu-id="99dc8-134">Null の処理</span><span class="sxs-lookup"><span data-stu-id="99dc8-134">Handling Nulls</span></span>

<span data-ttu-id="99dc8-p108">Null 値は **rs:maybenull** 属性によって処理されます。この属性が true に設定されている場合、列の内容に null 値を含めることができます。さらに、列がデータの行で見つからない場合、行セットからデータを読み取るユーザーに、 **IRowset::GetData()** から null 状態が返されます。Shippers テーブルの次の列定義を考えてみましょう。</span><span class="sxs-lookup"><span data-stu-id="99dc8-p108">Null values are handled by the **rs:maybenull** attribute. If this attribute is set to true, the contents of the column may contain a null value. Furthermore, if the column is not found in a row of data, the user reading the data back from the rowset will get a null status from **IRowset::GetData()**. Consider the following column definitions from the Shippers table:</span></span>

```xml 
 
<s:AttributeType name="ShipperID"> 
  <s:datatype dt:type="int" dt:maxLength="4"/> 
</s:AttributeType> 
<s:AttributeType name="CompanyName"> 
  <s:datatype dt:type="string" dt:maxLength="40" rs:maybenull="true"/> 
</s:AttributeType> 
```

<span data-ttu-id="99dc8-139">定義により CompanyName を null に設定できますが、ShipperID に null 値を含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="99dc8-139">The definition allows CompanyName to be null, but ShipperID cannot contain a null value.</span></span> <span data-ttu-id="99dc8-140">持続性プロバイダーが OLE DB 状態定数の DBSTATUS を [得意先名] 列のデータの状態を設定はデータ セクションに次の行が含まれている場合\_S\_ISNULL。</span><span class="sxs-lookup"><span data-stu-id="99dc8-140">If the data section contained the following row, the Persistence Provider would set the status of the data for the CompanyName column to the OLE DB status constant DBSTATUS\_S\_ISNULL:</span></span>

```xml 
 
<z:row ShipperID="1"/> 
```

<span data-ttu-id="99dc8-141">持続性プロバイダーが DBSTATUS の OLE DB ステータスを返しますが、行が完全に空で、次のように場合、\_E\_の得意先との DBSTATUS を使用できません\_S\_[得意先名] を ISNULL。</span><span class="sxs-lookup"><span data-stu-id="99dc8-141">If the row was entirely empty, as follows, the Persistence Provider would return an OLE DB status of DBSTATUS\_E\_UNAVAILABLE for ShipperID and DBSTATUS\_S\_ISNULL for CompanyName.</span></span>

```xml 
 
<z:row/>  
```

<span data-ttu-id="99dc8-142">長さがゼロの文字列と null は同じではないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="99dc8-142">Note that a zero-length string is not the same as null.</span></span>

```xml 
 
<z:row ShipperID="1" CompanyName=""/> 
```

<span data-ttu-id="99dc8-143">前の行では、持続性プロバイダーが DBSTATUS の OLE DB ステータスを返します\_S\_の両方の列には、[ok] します。</span><span class="sxs-lookup"><span data-stu-id="99dc8-143">For the preceding row, the Persistence Provider will return an OLE DB status of DBSTATUS\_S\_OK for both columns.</span></span> <span data-ttu-id="99dc8-144">この場合の CompanyName は単に "" (長さがゼロの文字列) です。</span><span class="sxs-lookup"><span data-stu-id="99dc8-144">The CompanyName in this case is simply "" (a zero-length string).</span></span>

<span data-ttu-id="99dc8-145">OLE DB 用の XML ドキュメントのスキーマ内で使用できる OLE DB コンストラクトの詳細については、"urn:schemas-microsoft-com:rowset" の定義および「OLE DB Programmer's Guide」 (英語) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="99dc8-145">For further information about the OLE DB constructs available for use within the schema of an XML document for OLE DB, see the definition of "urn:schemas-microsoft-com:rowset" and the OLE DB Programmer's Guide.</span></span>
