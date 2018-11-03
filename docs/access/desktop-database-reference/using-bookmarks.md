---
title: ブックマーク (デスクトップ データベース参照のアクセス) を使用してください。
TOCTitle: Using Bookmarks
ms:assetid: fe6333ef-c9d9-1e84-2252-d27edc676e97
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250306(v=office.15)
ms:contentKeyID: 48548935
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 76c8cc793c3956ea0db0f01c7b33ba5740118e42
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947736"
---
# <a name="using-bookmarks"></a><span data-ttu-id="43607-102">ブックマークを使用してください。</span><span class="sxs-lookup"><span data-stu-id="43607-102">Using bookmarks</span></span>


<span data-ttu-id="43607-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="43607-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="43607-p101">**Recordset** 内を移動した後、各レコードをスクロールして値を比較しなくても特定のレコードに直接戻ることができると便利な場合があります。たとえば、 **Find** メソッドでレコードを検索して見つからなかった場合、 **Recordset** のいずれかの端に自動的に戻ります。プロバイダーがブックマークをサポートしている場合、ブックマークを使用すると、 **Find** メソッドを使用する前の位置をマークし、その位置に戻ることができます。ブックマークはバリアント ( **Variant** ) 型の値で、 **Recordset** オブジェクト内のレコードを一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="43607-p101">It is often useful to return directly to a specific record after having moved around in the **Recordset** without having to scroll through every record and compare values. For example, if you attempt to search for a record using the **Find** method but the search returns no records, you are automatically placed at either end of the **Recordset**. If your provider supports them, bookmarks can be used to mark your place before using the **Find** method so you can return to your location. A bookmark is a **Variant** type value that uniquely identifies a record in a **Recordset** object.</span></span>

<span data-ttu-id="43607-p102">**Recordset** **Filter** メソッドでブックマークのバリアント型配列を使用して、選択したレコードセットをフィルターすることもできます。この方法の詳細については、この章の後半の「 [レコードセットを使用する](working-with-recordsets.md)」の「結果のフィルター処理」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="43607-p102">You can also use a variant array of bookmarks with the **Recordset** **Filter** method to filter on a selected set of records. For details about this technique, see Filtering the Results in the topic, [Working with Recordsets](working-with-recordsets.md), later in this chapter.</span></span>

<span data-ttu-id="43607-p103">**Bookmark** プロパティを使用すると、レコードのブックマークを取得したり、 **Recordset** オブジェクト内の現在のレコードを、有効なブックマークで識別されたレコードに設定したりできます。次のコードでは、 **Bookmark** プロパティを使用してブックマークを設定し、他のレコードに移動した後にブックマークが設定されたレコードに戻ります。 **Recordset** がブックマークをサポートしているかどうかを判断するには、 **Supports** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="43607-p103">You can use the **Bookmark** property to get a bookmark for a record, or set the current record in a **Recordset** object to the record identified by a valid bookmark. The following code uses the **Bookmark** property to set a bookmark and then return to the bookmarked record after moving on to other records. To determine if your **Recordset** supports bookmarks, use the **Supports** method.</span></span>

```vb 
 
'BeginBookmarkEg 
 Dim varBookmark As Variant 
 Dim blnCanBkmrk As Boolean 
 
 objRs.Open strSQL, strConnStr, adOpenStatic, adLockOptimistic, adCmdText 
 
 If objRs.RecordCount > 4 Then 
 objRs.Move 4 ' move to the fifth record 
 blnCanBkmrk = objRs.Supports(adBookmark) 
 If blnCanBkmrk = True Then 
 varBookmark = objRs.Bookmark ' record the bookmark 
 objRs.MoveLast ' move to a different record 
 objRs.Bookmark = varBookmark ' return to the bookmarked (sixth) record 
 End If 
 End If 
'EndBookmarkEg 
```

<span data-ttu-id="43607-113">[Supports](supports-method-ado.md) メソッドの詳細については、後で説明します。</span><span class="sxs-lookup"><span data-stu-id="43607-113">The [Supports](supports-method-ado.md) method is covered in more detail later.</span></span>

<span data-ttu-id="43607-p104">複製された **Recordset** の場合を除いて、同じコマンドを使用した場合でも、ブックマークが一意なのは作成された **Recordset** 内です。つまり、ある **Recordset** から取得した **Bookmark** を使用して、同じコマンドで開いた別の **Recordset** 内の同じレコードに移動することはできません。</span><span class="sxs-lookup"><span data-stu-id="43607-p104">Except for the case of cloned **Recordsets**, bookmarks are unique to the **Recordset** in which they were created, even if the same command is used. This means that you cannot use a **Bookmark** obtained from one **Recordset** to move to the same record in a second **Recordset** opened with the same command.</span></span>

