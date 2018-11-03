---
title: データ セクション (アクセス デスクトップ データベース参照)
TOCTitle: Data section
ms:assetid: fd8d31aa-af13-a52f-5e91-20225b8df175
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250303(v=office.15)
ms:contentKeyID: 48548920
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 98215394af89df30a95fcb9c5a757368cb64d4f1
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946378"
---
# <a name="data-section"></a><span data-ttu-id="9c72f-102">データ セクション</span><span class="sxs-lookup"><span data-stu-id="9c72f-102">Data section</span></span>

<span data-ttu-id="9c72f-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="9c72f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9c72f-p101">データ セクションは、行セットのデータ、および保留中の更新、挿入、または削除を定義します。データ セクションには、行が含まれない場合と、1 つ以上の行が含まれる場合があります。スキーマによって行が定義されている単一の行セットからのデータだけを含む場合もあります。また、前述したとおり、データを含まない列は省略される場合があります。属性やサブ要素がデータ セクションで使用されており、その構成体がスキーマ セクションで定義されていない場合、その構成体は自動的に無視されます。</span><span class="sxs-lookup"><span data-stu-id="9c72f-p101">The data section defines the data of the rowset along with any pending updates, insertions, or deletions. The data section may contain zero or more rows. It may only contain data from one rowset where the row is defined by the schema. Also, as noted before, columns without any data may be omitted. If an attribute or subelement is used in the data section and that construct has not been defined in the schema section, it is silently ignored.</span></span>

## <a name="string"></a><span data-ttu-id="9c72f-109">文字列型 (String)</span><span class="sxs-lookup"><span data-stu-id="9c72f-109">String</span></span>

<span data-ttu-id="9c72f-p102">テキスト データ内にある XML の予約文字は、適切な文字エンティティに置き換える必要があります。たとえば、"Joe's Garage" という会社名の場合、一重引用符文字をエンティティに置き換える必要があります。実際の行は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="9c72f-p102">Reserved XML characters in text data must be replaced with appropriate character entities. For example, in the company name "Joe's Garage," the single quote character must be replaced by an entity. The actual row would look like:</span></span>

```xml  
<z:row CompanyName="Joe&apos;s Garage"/> 
```

<span data-ttu-id="9c72f-113">次の文字は、XML で予約されているし、文字エン ティティに置き換える必要があります: {'、"、および、\<、\>} です。</span><span class="sxs-lookup"><span data-stu-id="9c72f-113">The following characters are reserved in XML and must be replaced by character entities: {',",&,\<,\>}.</span></span>

## <a name="binary"></a><span data-ttu-id="9c72f-114">バイナリ型 (Binary)</span><span class="sxs-lookup"><span data-stu-id="9c72f-114">Binary</span></span>

<span data-ttu-id="9c72f-115">バイナリ データは、bin.hex 方式でエンコードされます。つまり、2 文字に 1 バイト (1/2 バイトにつき 1 文字) が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="9c72f-115">Binary data is bin.hex encoded (that is, one byte maps to two characters, one character per nibble).</span></span>

## <a name="datetime"></a><span data-ttu-id="9c72f-116">DateTime</span><span class="sxs-lookup"><span data-stu-id="9c72f-116">DateTime</span></span>

<span data-ttu-id="9c72f-117">バリアント VT\_日付の形式が XML データのデータ型によって直接サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="9c72f-117">The variant VT\_DATE format is not directly supported by XML-Data data types.</span></span> <span data-ttu-id="9c72f-118">データと時刻の両方のコンポーネントを使用して日付の正しい形式は、年年年年-月月-日日**T**hh:mm:ss です。</span><span class="sxs-lookup"><span data-stu-id="9c72f-118">The correct format for dates with both a data and time component is yyyy-mm-dd**T**hh:mm:ss.</span></span>

<span data-ttu-id="9c72f-119">XML で指定された日付の形式の詳細については、 [W3C の XMLData 注](https://www.w3.org/TR/1998/NOTE-XML-data-0105/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9c72f-119">For more information about date formats specified by XML, see [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).</span></span>

<span data-ttu-id="9c72f-120">XML-Data の仕様で 2 つの等価なデータ型が定義されている場合 (i4 == int など)、ADO ではフレンドリ名で記述されますが、読み取りは両方に対して行われます。</span><span class="sxs-lookup"><span data-stu-id="9c72f-120">When the XML-Data specification defines two equivalent data types (for example, i4 == int), ADO will write out the friendly name but read in both.</span></span>

## <a name="managing-pending-changes"></a><span data-ttu-id="9c72f-121">保留中の変更を管理します。</span><span class="sxs-lookup"><span data-stu-id="9c72f-121">Managing pending changes</span></span>

<span data-ttu-id="9c72f-p104">**Recordset** は、イミディエイト更新モードまたはバッチ更新モードで開くことができます。クライアント側カーソルを使用してバッチ更新モードで開かれた場合、 **Recordset** に対して加えられるすべての変更は、 **UpdateBatch** メソッドが呼び出されるまで保留状態となります。 **Recordset** が保存されると、保留中の変更も保存されます。XML では、これらの変更は、urn:schemas-microsoft-com:rowset 内で定義された "update" 要素を使用して表されます。さらに、行セットを更新できる場合は、行の定義で updatable プロパティが true に設定されている必要があります。たとえば、Shippers テーブルに保留中の変更が含まれることを定義する場合、行の定義は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="9c72f-p104">A **Recordset** can be opened in immediate or batch update mode. When opened in batch update mode with client-side cursors, all changes made to the **Recordset** are in a pending state until the **UpdateBatch** method is called. Pending changes are also persisted when the **Recordset** is saved. In XML, they are represented by the use of the "update" elements defined in urn:schemas-microsoft-com:rowset. In addition, if a rowset can be updated, the updatable property must be set to true in the definition of the row. For example, to define that the Shippers table contains pending changes, the row definition would look like the following:</span></span>

```xml 
<s:ElementType name="row" content="eltOnly" updatable="true"> 
  <s:attribute type="ShipperID"/> 
  <s:attribute type="CompanyName"/> 
  <s:attribute type="Phone"/> 
  <s:extends type="rs:rowbase"/> 
</s:ElementType> 
```

<span data-ttu-id="9c72f-128">これにより、ADO が更新可能な **Recordset** オブジェクトを作成できるよう、Persistence Provider に対し、データを公開するよう指示されます。</span><span class="sxs-lookup"><span data-stu-id="9c72f-128">This tells the Persistence Provider to surface data so that ADO can construct an updatable **Recordset** object.</span></span>

<span data-ttu-id="9c72f-129">次のサンプル コードは、挿入、変更、および削除が、保存ファイルでどのように表現されるのかを示しています。</span><span class="sxs-lookup"><span data-stu-id="9c72f-129">The following sample data shows how insertions, changes, and deletions look in the persisted file:</span></span>

```xml 
<rs:data> 
  <z:row ShipperID="2" CompanyName="United Package"  
    Phone="(503) 555-3199"/> 
<rs:update> 
  <rs:original> 
    <z:row ShipperID="3" CompanyName="Federal Shipping"  
      Phone="(503) 555-9931"/> 
  </rs:original> 
  <z:row Phone="(503) 552-7134"/> 
</rs:update> 
<rs:insert> 
  <z:row ShipperID="12" CompanyName="Lightning Shipping"  
    Phone="(505) 111-2222"/> 
  <z:row ShipperID="13" CompanyName="Thunder Overnight"  
    Phone="(505) 111-2222"/> 
  <z:row ShipperID="14" CompanyName="Blue Angel Air Delivery"  
    Phone="(505) 111-2222"/> 
</rs:insert> 
<rs:delete> 
  <z:row ShipperID="1" CompanyName="Speedy Express" Phone="(503) 555-9831"/> 
</rs:delete> 
</rs:data> 
```

<span data-ttu-id="9c72f-p105">更新は、必ず元の行データ全体の後に、変更された行のデータが続くという形式で表されます。変更された行には、すべての列が含まれる場合と、実際に変更された列のみが含まれる場合があります。前の例では、Shipper 2 の行が変更されていないのに対し、Shipper 3 では Phone 列の値だけが変更されているため、変更された行に含まれる列はこれだけです。挿入行である Shippers 12、13、および 14 は、rs:insert タグの下でバッチ処理されます。前の例では示されていませんが、削除行もバッチ処理される場合があります。</span><span class="sxs-lookup"><span data-stu-id="9c72f-p105">An update always contains the entire original row data followed by the changed row data. The changed row may contain all of the columns or only those columns that have actually changed. In the previous example, the row for Shipper 2 is not changed, while only the Phone column has changed values for Shipper 3 and is therefore the only column included in the changed row. The inserted rows for Shippers 12, 13, and 14 are batched together under one rs:insert tag. Note that deleted rows may also be batched together, although this is not shown above.</span></span>

