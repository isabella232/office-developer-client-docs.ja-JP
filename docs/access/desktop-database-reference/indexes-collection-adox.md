---
title: Indexes コレクション (ADOX)
TOCTitle: Indexes collection (ADOX)
ms:assetid: ab04bdd1-7c4a-44cb-dfc6-add3a52f502f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249793(v=office.15)
ms:contentKeyID: 48546963
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6eac0d1b73e0380f582ce0bc69cdb358c67d185e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712058"
---
# <a name="indexes-collection-adox"></a><span data-ttu-id="a35ca-102">Indexes コレクション (ADOX)</span><span class="sxs-lookup"><span data-stu-id="a35ca-102">Indexes collection (ADOX)</span></span>


<span data-ttu-id="a35ca-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="a35ca-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a35ca-104">テーブルのすべての [Index](index-object-adox.md) オブジェクトを含みます。</span><span class="sxs-lookup"><span data-stu-id="a35ca-104">Contains all [Index](index-object-adox.md) objects of a table.</span></span>

## <a name="remarks"></a><span data-ttu-id="a35ca-105">解説</span><span class="sxs-lookup"><span data-stu-id="a35ca-105">Remarks</span></span>

<span data-ttu-id="a35ca-p101">[Indexes](append-method-adox-indexes.md) コレクションの **Append** メソッドは、ADOX に対して一意です。次のことができます。</span><span class="sxs-lookup"><span data-stu-id="a35ca-p101">The [Append](append-method-adox-indexes.md) method for an **Indexes** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="a35ca-108">**Append** メソッドを使用して、新しいインデックスをコレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="a35ca-108">Add a new index to the collection with the **Append** method.</span></span>

<span data-ttu-id="a35ca-p102">残りのプロパティとメソッドは、ADO コレクションに標準で装備されています。次のことができます。</span><span class="sxs-lookup"><span data-stu-id="a35ca-p102">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="a35ca-111">[Item](item-property-ado.md) プロパティを使用して、コレクションのインデックスにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="a35ca-111">Access an index in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="a35ca-112">[Count](count-property-ado.md) プロパティを使用して、コレクションに含まれるインデックスの数を返します。</span><span class="sxs-lookup"><span data-stu-id="a35ca-112">Return the number of indexes contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="a35ca-113">[Delete](delete-method-adox-collections.md) メソッドを使用して、コレクションからインデックスを削除します。</span><span class="sxs-lookup"><span data-stu-id="a35ca-113">Remove an index from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="a35ca-114">[Refresh](refresh-method-ado.md) メソッドを使用して、コレクションのオブジェクトを更新し、カレント データベースのスキーマを反映します。</span><span class="sxs-lookup"><span data-stu-id="a35ca-114">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>

