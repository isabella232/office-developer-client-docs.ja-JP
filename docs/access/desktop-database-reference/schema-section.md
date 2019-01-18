---
title: スキーマ セクション (アクセス デスクトップ データベース参照)
TOCTitle: Schema Section
ms:assetid: 59b42ffb-0524-adc3-8bcd-6e4cd2c505ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249304(v=office.15)
ms:contentKeyID: 48545023
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f8c479c430dd6d0ca742fefb4948544d31ba2e61
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709867"
---
# <a name="schema-section"></a>スキーマ セクション

**適用されます**Access 2013、Office 2013。

## <a name="schema-section"></a>Schema セクション

Schema セクションは必須です。前の例で示したように、ADO は各列に関する詳細なメタデータを書き込んで、データ値の形式を更新用にできる限り多く保持します。ただし、XML で読み込むには、ADO は、列の名前およびその列が属する行セットのみを必要とします。次に、最小のスキーマの例を示します。

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

上記の例では、スキーマにデータ型情報が含まれていないため、ADO はデータを可変長文字列として扱います。

## <a name="creating-aliases-for-column-names"></a>列名のエイリアスの作成

**rs:name** 属性を使用すると、列名のエイリアスを作成して、行セットに表示される列情報をわかりやすい名前で表示し、データ セクションに短縮名を表示できます。たとえば、上記のスキーマを次のように変更して、ShipperID を s1 に、CompanyName を s2 に、Phone を s3 にマップできます。

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

次に、データ セクションでは、行は **rs:name** ではなく **name** 属性を使用して列を参照します。

```xml 
 
"<row s1="1" s2="Speedy Express" s3="(503) 555-9831"/> 
```

列名が有効な属性または XML のタグ名ではない場合は、必ず列名のエイリアスを作成する必要があります。たとえば、スペースが含まれる名前は無効な属性のため、"Last Name" にはエイリアスが必要です。次の行は XML パーサーでは正しく処理されないため、エイリアスを作成して、スペースを含まない他の名前にする必要があります。

```xml 
 
<row last name="Jones"/> 
```

**name** 属性に使用する値は、XML ドキュメントのスキーマとデータ セクションの両方の列が参照される各箇所で、一貫して使用する必要があります。次の例に、s1 の一貫した使用を示します。

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

同様に、上記の CompanyName にはエイリアスが定義されていないため、ドキュメント全体で CompanyName を一貫して使用する必要があります。

## <a name="data-types"></a>データ型

**dt:type** 属性を使用して、列にデータ型を適用できます。データ型を指定するには、列定義自体で **dt:type** 属性を直接指定するか、列定義の入れ子にされた要素として **s:datatype** コンストラクトを使用します。次に例を示します。

```xml 
 
<s:AttributeType name="Phone" > 
  <s:datatype dt:type="string"/> 
</s:AttributeType> 
```

これは、次と同等です。

```xml 
 
<s:AttributeType name="Phone" dt:type="string"/> 
```

行定義全体から **dt:type** 属性を省略すると、既定では、列の型は可変長文字列になります。

型の名前 (**dt:maxLength** など) 以外に、型に関するより詳細な情報があると、**s:datatype** 子要素を使用してさらに読みやすくできます。ただし、これは単なる慣習であり、必要条件ではありません。

次の例に、スキーマに型情報を含める方法を詳しく示します。

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

2 番目の例では、 **rs:fixedlength** 属性を細部で使用しています。 **rs:fixedlength** 属性が true に設定されている列は、そのデータにはスキーマで定義されている長さが必要だということを示しています。 タイトルの法律がこの例では、値\_id は、"123456 または"「123」 "123" は長さが 6 ではなく 3 のため有効ではありません。 **fixedlength** プロパティの詳細については、「OLE DB Programmer's Guide」 (英語) を参照してください。

## <a name="handling-nulls"></a>Null の処理

Null 値は **rs:maybenull** 属性によって処理されます。この属性が true に設定されている場合、列の内容に null 値を含めることができます。さらに、列がデータの行で見つからない場合、行セットからデータを読み取るユーザーに、 **IRowset::GetData()** から null 状態が返されます。Shippers テーブルの次の列定義を考えてみましょう。

```xml 
 
<s:AttributeType name="ShipperID"> 
  <s:datatype dt:type="int" dt:maxLength="4"/> 
</s:AttributeType> 
<s:AttributeType name="CompanyName"> 
  <s:datatype dt:type="string" dt:maxLength="40" rs:maybenull="true"/> 
</s:AttributeType> 
```

定義により CompanyName を null に設定できますが、ShipperID に null 値を含めることはできません。 持続性プロバイダーが OLE DB 状態定数の DBSTATUS を [得意先名] 列のデータの状態を設定はデータ セクションに次の行が含まれている場合\_S\_ISNULL。

```xml 
 
<z:row ShipperID="1"/> 
```

持続性プロバイダーが DBSTATUS の OLE DB ステータスを返しますが、行が完全に空で、次のように場合、\_E\_の得意先との DBSTATUS を使用できません\_S\_[得意先名] を ISNULL。

```xml 
 
<z:row/>  
```

長さがゼロの文字列と null は同じではないことに注意してください。

```xml 
 
<z:row ShipperID="1" CompanyName=""/> 
```

前の行では、持続性プロバイダーが DBSTATUS の OLE DB ステータスを返します\_S\_の両方の列には、[ok] します。 この場合の CompanyName は単に "" (長さがゼロの文字列) です。

OLE DB 用の XML ドキュメントのスキーマ内で使用できる OLE DB コンストラクトの詳細については、"urn:schemas-microsoft-com:rowset" の定義および「OLE DB Programmer's Guide」 (英語) を参照してください。

