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
# <a name="data-section"></a>データ セクション

**適用されます**Access 2013、Office 2013。

データ セクションは、行セットのデータ、および保留中の更新、挿入、または削除を定義します。データ セクションには、行が含まれない場合と、1 つ以上の行が含まれる場合があります。スキーマによって行が定義されている単一の行セットからのデータだけを含む場合もあります。また、前述したとおり、データを含まない列は省略される場合があります。属性やサブ要素がデータ セクションで使用されており、その構成体がスキーマ セクションで定義されていない場合、その構成体は自動的に無視されます。

## <a name="string"></a>文字列型 (String)

テキスト データ内にある XML の予約文字は、適切な文字エンティティに置き換える必要があります。たとえば、"Joe's Garage" という会社名の場合、一重引用符文字をエンティティに置き換える必要があります。実際の行は次のようになります。

```xml  
<z:row CompanyName="Joe&apos;s Garage"/> 
```

次の文字は、XML で予約されているし、文字エン ティティに置き換える必要があります: {'、"、および、\<、\>} です。

## <a name="binary"></a>バイナリ型 (Binary)

バイナリ データは、bin.hex 方式でエンコードされます。つまり、2 文字に 1 バイト (1/2 バイトにつき 1 文字) が割り当てられます。

## <a name="datetime"></a>DateTime

バリアント VT\_日付の形式が XML データのデータ型によって直接サポートされていません。 データと時刻の両方のコンポーネントを使用して日付の正しい形式は、年年年年-月月-日日**T**hh:mm:ss です。

XML で指定された日付の形式の詳細については、 [W3C の XMLData 注](https://www.w3.org/TR/1998/NOTE-XML-data-0105/)を参照してください。

XML-Data の仕様で 2 つの等価なデータ型が定義されている場合 (i4 == int など)、ADO ではフレンドリ名で記述されますが、読み取りは両方に対して行われます。

## <a name="managing-pending-changes"></a>保留中の変更を管理します。

**Recordset** は、イミディエイト更新モードまたはバッチ更新モードで開くことができます。クライアント側カーソルを使用してバッチ更新モードで開かれた場合、 **Recordset** に対して加えられるすべての変更は、 **UpdateBatch** メソッドが呼び出されるまで保留状態となります。 **Recordset** が保存されると、保留中の変更も保存されます。XML では、これらの変更は、urn:schemas-microsoft-com:rowset 内で定義された "update" 要素を使用して表されます。さらに、行セットを更新できる場合は、行の定義で updatable プロパティが true に設定されている必要があります。たとえば、Shippers テーブルに保留中の変更が含まれることを定義する場合、行の定義は次のようになります。

```xml 
<s:ElementType name="row" content="eltOnly" updatable="true"> 
  <s:attribute type="ShipperID"/> 
  <s:attribute type="CompanyName"/> 
  <s:attribute type="Phone"/> 
  <s:extends type="rs:rowbase"/> 
</s:ElementType> 
```

これにより、ADO が更新可能な **Recordset** オブジェクトを作成できるよう、Persistence Provider に対し、データを公開するよう指示されます。

次のサンプル コードは、挿入、変更、および削除が、保存ファイルでどのように表現されるのかを示しています。

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

更新は、必ず元の行データ全体の後に、変更された行のデータが続くという形式で表されます。変更された行には、すべての列が含まれる場合と、実際に変更された列のみが含まれる場合があります。前の例では、Shipper 2 の行が変更されていないのに対し、Shipper 3 では Phone 列の値だけが変更されているため、変更された行に含まれる列はこれだけです。挿入行である Shippers 12、13、および 14 は、rs:insert タグの下でバッチ処理されます。前の例では示されていませんが、削除行もバッチ処理される場合があります。

