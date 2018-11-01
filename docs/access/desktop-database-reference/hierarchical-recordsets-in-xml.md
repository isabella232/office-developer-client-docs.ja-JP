---
title: XML の階層 Recordset
TOCTitle: Hierarchical Recordsets in XML
ms:assetid: 606dee87-8762-6cc2-a151-94d34031b35f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249351(v=office.15)
ms:contentKeyID: 48545181
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5276dd011ec8b7c6190ab35f5417009510875e15
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877171"
---
# <a name="hierarchical-recordsets-in-xml"></a><span data-ttu-id="6fbcd-102">XML の階層 Recordset</span><span class="sxs-lookup"><span data-stu-id="6fbcd-102">Hierarchical Recordsets in XML</span></span>


<span data-ttu-id="6fbcd-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="6fbcd-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="hierarchical-recordsets-in-xml"></a><span data-ttu-id="6fbcd-104">XML での階層レコードセット</span><span class="sxs-lookup"><span data-stu-id="6fbcd-104">Hierarchical Recordsets in XML</span></span>

<span data-ttu-id="6fbcd-p101">ADO では、階層構造の **Recordset** オブジェクトを XML で保存できます。階層構造の **Recordset** オブジェクトでは、親 **Recordset** のフィールドの値が、別の **Recordset** になります。このようなフィールドは、XML ストリームでは、属性ではなく子要素として表されます。次の例は、このような状態を示しています。</span><span class="sxs-lookup"><span data-stu-id="6fbcd-p101">ADO allows persistence of hierarchical **Recordset** objects into XML. With hierarchical **Recordset** objects, the value of a field in the parent **Recordset** is another **Recordset**. Such fields are represented as child elements in the XML stream rather than an attribute. The following example demonstrates this case:</span></span>

```vb 
 
Rs.Open "SHAPE {select stor_id, stor_name, state from stores} APPEND ({select stor_id, ord_num, ord_date, qty from sales} AS rsSales RELATE stor_id TO stor_id)", "Provider=MSDataShape;DSN=pubs;UID=MyUserId;PWD=MyPassword;" 
```

<span data-ttu-id="6fbcd-109">保存された XML 形式の **Recordset** を次に示します。</span><span class="sxs-lookup"><span data-stu-id="6fbcd-109">The following is the XML format of the persisted **Recordset**:</span></span>

```xml 
 
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882"     xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"     xmlns:rs="urn:schemas-microsoft-com:rowset"  
    xmlns:z="#RowsetSchema">  
  <s:Schema id="RowsetSchema">  
    <s:ElementType name="row" content="eltOnly" rs:updatable="true">  
      <s:AttributeType name="stor_id" rs:number="1"  
        rs:writeunknown="true">  
        <s:datatype dt:type="string" dt:maxLength="4"  
          rs:fixedlength="true" rs:maybenull="false"/>  
      </s:AttributeType>  
      <s:AttributeType name="stor_name" rs:number="2" rs:nullable="true"  
        rs:writeunknown="true">  
          <s:datatype dt:type="string" dt:maxLength="40"/>  
      </s:AttributeType>  
      <s:AttributeType name="state" rs:number="3" rs:nullable="true"  
        rs:writeunknown="true">  
        <s:datatype dt:type="string" dt:maxLength="2"  
          rs:fixedlength="true"/>  
      </s:AttributeType>  
      <s:ElementType name="rsSales" content="eltOnly"  
        rs:updatable="true" rs:relation="010000000100000000000000">  
        <s:AttributeType name="stor_id" rs:number="1"  
          rs:writeunknown="true">  
          <s:datatype dt:type="string" dt:maxLength="4"  
            rs:fixedlength="true" rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:AttributeType name="ord_num" rs:number="2"  
          rs:writeunknown="true">  
          <s:datatype dt:type="string" dt:maxLength="20"  
            rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:AttributeType name="ord_date" rs:number="3"  
          rs:writeunknown="true">  
            <s:datatype dt:type="dateTime" dt:maxLength="16"  
              rs:scale="3" rs:precision="23" rs:fixedlength="true"  
              rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:AttributeType name="qty" rs:number="4" rs:writeunknown="true">  
          <s:datatype dt:type="i2" dt:maxLength="2" rs:precision="5"  
            rs:fixedlength="true" rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:extends type="rs:rowbase"/>  
      </s:ElementType>  
      <s:extends type="rs:rowbase"/>  
    </s:ElementType>  
  </s:Schema>  
  <rs:data>  
    <z:row stor_id="6380" stor_name="Eric the Read Books" state="WA">  
      <rsSales stor_id="6380" ord_num="6871"  
        ord_date="1994-09-14T00:00:00" qty="5"/>  
      <rsSales stor_id="6380" ord_num="722a"  
        ord_date="1994-09-13T00:00:00" qty="3"/>  
    </z:row>  
    <z:row stor_id="7066" stor_name="Barnum's" state="CA">  
      <rsSales stor_id="7066" ord_num="A2976"  
        ord_date="1993-05-24T00:00:00" qty="50"/>  
      <rsSales stor_id="7066" ord_num="QA7442.3"  
        ord_date="1994-09-13T00:00:00" qty="75"/>  
    </z:row>  
    <z:row stor_id="7067" stor_name="News & Brews" state="CA">  
      <rsSales stor_id="7067" ord_num="D4482"  
        ord_date="1994-09-14T00:00:00" qty="10"/>  
      <rsSales stor_id="7067" ord_num="P2121"  
        ord_date="1992-06-15T00:00:00" qty="40"/>  
      <rsSales stor_id="7067" ord_num="P2121"  
        ord_date="1992-06-15T00:00:00" qty="20"/>  
      <rsSales stor_id="7067" ord_num="P2121"  
        ord_date="1992-06-15T00:00:00" qty="20"/>  
    </z:row>  
... 
  </rs:data>  
</xml>  
```

<span data-ttu-id="6fbcd-p102">この方法で保存すると、親 **Recordset** 内の列の正確な順序が明確に示されません。親のすべてのフィールドには、子 **Recordset** を含めることができます。Persistence Provider は、まずすべてのスカラー列を属性として保存してから、子 **Recordset** のすべての "列" を親行の子要素として保存します。親 **Recordset** におけるフィールドの序数位置は、 **Recordset** のスキーマ定義を確認することで取得できます。すべてのフィールドには、OLE DB プロパティである **rs:number** があります。これは、 **Recordset** のスキーマ名前空間で定義されており、そのフィールドの序数値を格納します。</span><span class="sxs-lookup"><span data-stu-id="6fbcd-p102">The exact order of the columns in the parent **Recordset** is not obvious when it is persisted in this manner. Any field in the parent may contain a child **Recordset**. The Persistence Provider persists out all scalar columns first as attributes and then persists out all child **Recordset** "columns" as child elements of the parent row. The ordinal position of the field in the parent **Recordset** can be obtained by looking at the schema definition of the **Recordset**. Every field has an OLE DB property, **rs:number**, defined in the **Recordset** schema namespace that contains the ordinal number for that field.</span></span>

<span data-ttu-id="6fbcd-p103">子 **Recordset** のすべてのフィールドの名前は、その子を格納する親 **Recordset** のフィールドの名前と連結されます。これは、親および子 **Recordset** の両方に、別の 2 つのテーブルから取得した同じ名前のフィールドが含まれている場合に、名前の競合が発生しないようにするためです。</span><span class="sxs-lookup"><span data-stu-id="6fbcd-p103">The names of all fields in the child **Recordset** are concatenated with the name of the field in the parent **Recordset** that contains this child. This is to ensure that there are no name collisions in cases where parent and child **Recordsets** both contain a field that is obtained from two different tables but is named singularly.</span></span>

<span data-ttu-id="6fbcd-117">階層 **Recordset** を XML で保存するときは、次に挙げる ADO の制約に注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fbcd-117">When saving hierarchical **Recordsets** into XML, you should be aware of the following restrictions in ADO:</span></span>

  - <span data-ttu-id="6fbcd-118">保留中の更新を含む階層 **Recordset** は、XML で保存できません。</span><span class="sxs-lookup"><span data-stu-id="6fbcd-118">A hierarchical **Recordset** with pending updates cannot be persisted into XML.</span></span>

  - <span data-ttu-id="6fbcd-119">パラメーター化されたシェイプ コマンドで作成された階層 **Recordset** は、XML 形式と ADTG 形式のどちらでも保存できません。</span><span class="sxs-lookup"><span data-stu-id="6fbcd-119">A hierarchical **Recordset** created with a parameterized shape command cannot be persisted (in either XML or ADTG format).</span></span>

  - <span data-ttu-id="6fbcd-p104">ADO では、現在、親および子 **Recordset** の関係を BLOB (Binary Large Object) として保存しています。この関係を記述するための XML タグは、行セットのスキーマ名前空間ではまだ定義されていません。</span><span class="sxs-lookup"><span data-stu-id="6fbcd-p104">ADO currently saves the relationship between the parent and the child **Recordsets** as a binary large object (BLOB). XML tags to describe this relationship have not yet been defined in the rowset schema namespace.</span></span>

  - <span data-ttu-id="6fbcd-p105">階層 **Recordset** が保存されるときに、すべての子 **Recordset** も一緒に保存されます。現在の **Recordset** が別の **Recordset** の子である場合、その親は保存されません。現在の **Recordset** のサブツリーを形成するすべての子 **Recordset** は保存されます。</span><span class="sxs-lookup"><span data-stu-id="6fbcd-p105">When a hierarchical **Recordset** is saved, all child **Recordsets** are saved along with it. If the current **Recordset** is a child of another **Recordset**, its parent is not saved. All child **Recordsets** that form the subtree of the current **Recordset** are saved.</span></span>

<span data-ttu-id="6fbcd-125">階層 **Recordset** を XML 保存形式から再度開くときは、次の制限事項に注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fbcd-125">When a hierarchical **Recordset** is reopened from its XML-persisted format, you must be aware of the following limitations:</span></span>

  - <span data-ttu-id="6fbcd-p106">子レコードに、対応する親レコードが存在しないレコードが含まれる場合、これらの行は、XML 形式の階層 **Recordset** には記述されません。このため、これらの行は、その **Recordset** を保存場所から再度開いたときには失われています。</span><span class="sxs-lookup"><span data-stu-id="6fbcd-p106">If the child record contains records for which there are no corresponding parent records, these rows are not written out in the XML representation of the hierarchical **Recordset**. Thus, these rows will be lost when the **Recordset** is reopened from its persisted location.</span></span>

  - <span data-ttu-id="6fbcd-p107">子レコードが複数の親レコードを参照している場合、 **Recordset** を再度開いたときに、その子 **Recordset** に重複するレコードが含まれる場合があります。しかし、これらの重複は、基になる子行セットを直接操作しない限り、ユーザーにはわかりません。ADO による唯一の移動手段であるチャプターを使用して子 **Recordset** を移動する場合、重複があることはユーザーにはわかりません。</span><span class="sxs-lookup"><span data-stu-id="6fbcd-p107">If a child record has references to more than one parent record, then on reopening the **Recordset**, the child **Recordset** may contain duplicate records. However, these duplicates will only be visible if the user works directly with the underlying child rowset. If a chapter is used to navigate the child **Recordset** (that is the only way to navigate through ADO), the duplicates are not visible.</span></span>

