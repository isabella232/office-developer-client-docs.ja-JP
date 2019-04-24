---
title: Fields コレクション
TOCTitle: The Fields Collection
ms:assetid: 3bda8e5d-eceb-9605-c4d7-c1f4cc00ce6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249154(v=office.15)
ms:contentKeyID: 48544297
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ce08ac5952151471ce74afd9a8a49600d8e8f633
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314134"
---
# <a name="fields-collection"></a><span data-ttu-id="58bae-102">Fields コレクション</span><span class="sxs-lookup"><span data-stu-id="58bae-102">Fields collection</span></span>


<span data-ttu-id="58bae-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="58bae-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="58bae-p101">**Fields** コレクションは、ADO に組み込まれたコレクションの 1 つです。コレクションは、並べ替えられた項目のセットで、単位と呼ばれることもあります。</span><span class="sxs-lookup"><span data-stu-id="58bae-p101">The **Fields** collection is one of ADO's intrinsic collections. A collection is an ordered set of items that can be referred to as a unit.</span></span>

<span data-ttu-id="58bae-p102">**Fields** コレクションには、 **Recordset** 内の各フィールド (列) に対応する **Field** オブジェクトが含まれています。すべての ADO コレクションと同様に、 **Append** メソッドおよび **Refresh** メソッド以外に、 **Count** プロパティおよび **Item** プロパティも使用できます。他の ADO コレクションでは使用できない、 **CancelUpdate** 、 **Delete** 、 **Resync** 、および **Update** の各メソッドも使用できます。</span><span class="sxs-lookup"><span data-stu-id="58bae-p102">The **Fields** collection contains a **Field** object for every field (column) in the **Recordset**. Like all ADO collections, it has **Count** and **Item** properties, as well as **Append** and **Refresh** methods. It also has **CancelUpdate**, **Delete**, **Resync**, and **Update** methods, which are not available to other ADO collections.</span></span>

## <a name="examining-the-fields-collection"></a><span data-ttu-id="58bae-109">Fields コレクションを検査する</span><span class="sxs-lookup"><span data-stu-id="58bae-109">Examining the Fields Collection</span></span>

<span data-ttu-id="58bae-p103">この章で説明したサンプル **Recordset** の **Fields** コレクションについて考えてみましょう。サンプル **Recordset** は、SQL ステートメントから導出されました。</span><span class="sxs-lookup"><span data-stu-id="58bae-p103">Consider the **Fields** collection of the sample **Recordset** introduced in this chapter. The sample **Recordset** was derived from the SQL statement</span></span>

```sql 
 
SELECT ProductID, ProductName, UnitPrice FROM Products WHERE CategoryID = 7 
```

<span data-ttu-id="58bae-112">このように、 **Recordset** **Fields** コレクションには、3 つのフィールドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="58bae-112">Thus, you should find that the **Recordset** **Fields** collection contains three fields.</span></span>

```vb 
 
'BeginWalkFields 
 Dim objFields As ADODB.Fields 
 
 objRs.Open strSQL, strConnStr, adOpenForwardOnly, adLockReadOnly, adCmdText 
 
 Set objFields = objRs.Fields 
 
 For intLoop = 0 To (objFields.Count - 1) 
 Debug.Print objFields.Item(intLoop).Name 
 Next 
'EndWalkFields 
```

<span data-ttu-id="58bae-p104">このコードでは、単に **Count** プロパティを使用して **Fields** コレクション内の **Field** オブジェクトの数を調べ、コレクション内をループし、 **Field** オブジェクトごとに **Name** プロパティの値を返します。さらに多くの **Field** プロパティを使用すると、フィールドに関する情報を取得できます。 **Field** の照会の詳細については、「 [Field オブジェクト](the-field-object.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="58bae-p104">This code simply determines the number of **Field** objects in the **Fields** collection using the **Count** property and loops through the collection, returning the value of the **Name** property for each **Field** object. You can use many more **Field** properties to get information about a field. For more information about querying a **Field**, see [The Field Object](the-field-object.md).</span></span>

## <a name="counting-columns"></a><span data-ttu-id="58bae-116">列をカウントする</span><span class="sxs-lookup"><span data-stu-id="58bae-116">Counting Columns</span></span>

<span data-ttu-id="58bae-p105">**Count** プロパティは、名前のとおり、 **Fields** コレクション内にある **Field** オブジェクトの実際の数を返します。コレクションのメンバーの番号はゼロから始まるため、常にゼロ番のメンバーからループを開始し、 **Count** プロパティの値から 1 を引いた値で終了するようにコードを記述する必要があります。Microsoft Visual Basic を使用して、 **Count** プロパティをチェックせずにコレクションのメンバーをループする場合は、 **For** **Each...Next** コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="58bae-p105">As you might expect, the **Count** property returns the actual number of **Field** objects in the **Fields** collection. Because numbering for members of a collection begins with zero, you should always code loops starting with the zero member and ending with the value of the **Count** property minus 1. If you are using Microsoft Visual Basic and want to loop through the members of a collection without checking the **Count** property, use the **For** **Each...Next** command.</span></span>

<span data-ttu-id="58bae-120">**Count** プロパティがゼロの場合、コレクション内にはオブジェクトはありません。</span><span class="sxs-lookup"><span data-stu-id="58bae-120">If the **Count** property is zero, there are no objects in the collection.</span></span>

## <a name="getting-to-the-field"></a><span data-ttu-id="58bae-121">Field にアクセスする</span><span class="sxs-lookup"><span data-stu-id="58bae-121">Getting to the Field</span></span>

<span data-ttu-id="58bae-p106">ADO コレクションと同様に、 **Item** プロパティはコレクションの既定のプロパティです。このプロパティは、渡された名前またはインデックスで指定された個別の **Field** オブジェクトを返します。したがって、次のステートメントは、サンプル **Recordset** と同じになります。</span><span class="sxs-lookup"><span data-stu-id="58bae-p106">As with any ADO collection, the **Item** property is the default property of the collection. It returns the individual **Field** object specified by the name or index passed to it. Therefore, the following statements are equivalent for the sample **Recordset**:</span></span>

```vb 
 
objField = objRecordset.Fields.Item("ProductID") 
objField = objRecordset.Fields("ProductID") 
objField = objRecordset.Fields.Item(0) 
objField = objRecordset.Fields(0) 
```

<span data-ttu-id="58bae-p107">これらのメソッドが同等の場合、どのメソッドが最適でしょうか。それは、時と場合によります。インデックスを使用してコレクションから **Field** を取得する方が、文字列検索を実行しなくても **Field** に直接アクセスできるため、高速です。一方、コレクション内の **Fields** の順序を把握しておく必要があり、順序が変わった場合、常に **Field** のインデックスへの参照を変更する必要があります。若干遅くなりますが、 **Field** の名前を使用する方が、コレクション内の **Fields** の順序に依存しないため、柔軟性があります。</span><span class="sxs-lookup"><span data-stu-id="58bae-p107">If these methods are equivalent, which is best? It depends. Using an index to retrieve a **Field** from the collection is faster because it accesses the **Field** directly without having to perform a string lookup. On the other hand, the order of **Fields** within the collection must be known, and if the order changes, the reference to the **Field's** index will have to be changed wherever it occurs. Although slightly slower, using the name of the **Field** is more flexible because it doesn't depend on the order of the **Fields** in the collection.</span></span>

## <a name="using-the-refresh-method"></a><span data-ttu-id="58bae-130">Refresh メソッドを使用する</span><span class="sxs-lookup"><span data-stu-id="58bae-130">Using the Refresh Method</span></span>

<span data-ttu-id="58bae-p108">他のいくつかの ADO コレクションと異なり、**Fields** コレクションで **Refresh** メソッドを使用しても目に見える効果はありません。基になるデータベース構造から変更を取得するには、**Requery** メソッドを使用するか、**Recordset** オブジェクトがブックマークをサポートしていない場合は、**MoveFirst** メソッドを使用する必要があります。このメソッドにより、コマンドがプロバイダーに対して再実行されます。</span><span class="sxs-lookup"><span data-stu-id="58bae-p108">Unlike some other ADO collections, using the **Refresh** method on the **Fields** collection has no visible effect. To retrieve changes from the underlying database structure, you must use either the **Requery** method, or if the **Recordset** object does not support bookmarks, the **MoveFirst** method, which will cause the command to be executed against the provider again.</span></span>

## <a name="adding-fields-to-a-recordset"></a><span data-ttu-id="58bae-133">Recordset にフィールドを追加する</span><span class="sxs-lookup"><span data-stu-id="58bae-133">Adding Fields to a Recordset</span></span>

<span data-ttu-id="58bae-134">**Append** メソッドは、**Recordset** にフィールドを追加するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="58bae-134">The **Append** method is used to add fields to a **Recordset**.</span></span>

<span data-ttu-id="58bae-p109">**Append** メソッドを使用すると、データ ソースへの接続を開かなくても、 **Recordset** をプログラムによって製造できます。開いている **Recordset** 、または **ActiveConnection** プロパティが設定されている **Recordset** の **Fields** コレクションで **Append** メソッドを呼び出すと、実行時エラーが発生します。フィールドを追加できるのは、開いていない状態で、データ ソースにも接続されていない **Recordset** のみです。ただし、新しく追加された **Fields** に値を指定するには、 **Recordset** をまず開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="58bae-p109">You can use the **Append** method to fabricate a **Recordset** programmatically without opening a connection to a data source. A run-time error will occur if the **Append** method is called on the **Fields** collection of an open **Recordset** or on a **Recordset** where the **ActiveConnection** property has been set. You can append fields only to a **Recordset** that is not open and has not yet been connected to a data source. However, to specify values for the newly appended **Fields**, the **Recordset** must first be opened.</span></span>

<span data-ttu-id="58bae-p110">開発者は、データを一時的に保存する場所を必要とすることや、データをサーバーから発生したかのように処理して、ユーザー インターフェイスのデータ バインドに参加できるようにすることがあります。ADO と [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) を組み合わせて使用すると、開発者は、列情報を指定して **Open** を呼び出すことにより、空の **Recordset** オブジェクトを作成できます。次の例では、新しい **Recordset** オブジェクトに 3 つの新規フィールドが追加されます。次に **Recordset** が開かれ、2 つの新規レコードが追加され、 **Recordset** がファイルに保存されます。 **Recordset** の保存の詳細については、「 [5 章: データを更新し、保存する](chapter-5-updating-and-persisting-data.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="58bae-p110">Developers often need a place to temporarily store some data, or want some data to act as if it came from a server so it can participate in data binding in a user interface. ADO (in conjunction with the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md)) enables the developer to build an empty **Recordset** object by specifying column information and calling **Open**. In the following example, three new fields are appended to a new **Recordset** object. Then the **Recordset** is opened, two new records are added, and the **Recordset** is persisted to a file. (For more information about **Recordset** persistence, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).)</span></span>

```vb 
 
 'BeginFabricate 
 Dim objRs As New ADODB.Recordset 
 
 With objRs.Fields 
 .Append "StudentID", adChar, 11, adFldUpdatable 
 .Append "FullName", adVarChar, 50, adFldUpdatable 
 .Append "PhoneNmbr", adVarChar, 20, adFldUpdatable 
 End With 
 
 With objRs 
 .Open 
 
 .AddNew 
 .Fields(0) = "123-45-6789" 
 .Fields(1) = "John Doe" 
 .Fields(2) = "(425) 555-5555" 
 .Update 
 
 .AddNew 
 .Fields(0) = "123-45-6780" 
 .Fields(1) = "Jane Doe" 
 .Fields(2) = "(615) 555-1212" 
 .Update 
 End With 
 
 objRs.Save App.Path & "\FabriTest.adtg", adPersistADTG 
 
 objRs.Close 
 'EndFabricate 
```

<span data-ttu-id="58bae-p111">**Fields** **Append** メソッドの使用方法は、 **Recordset** オブジェクトの場合と **Record** オブジェクトの場合とで異なります。 **Record** オブジェクトの詳細については、「 [10 章: レコードとストリーム](chapter-10-records-and-streams.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="58bae-p111">The usage of the **Fields** **Append** method differs between the **Recordset** object and the **Record** object. For more information about the **Record** object, see [Chapter 10: Records and Streams](chapter-10-records-and-streams.md).</span></span>

