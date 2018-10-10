---
title: Indexes コレクション (ADOX)
TOCTitle: Indexes Collection (ADOX)
ms:assetid: ab04bdd1-7c4a-44cb-dfc6-add3a52f502f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249793(v=office.15)
ms:contentKeyID: 48546963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a3dbc32da7580aa4e4c222c20131cda2adefdb50
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476232"
---
# <a name="indexes-collection-adox"></a><span data-ttu-id="18ada-102">Indexes コレクション (ADOX)</span><span class="sxs-lookup"><span data-stu-id="18ada-102">Indexes Collection (ADOX)</span></span>


<span data-ttu-id="18ada-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="18ada-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="18ada-104">テーブルのすべての [Index](index-object-adox.md) オブジェクトを含みます。</span><span class="sxs-lookup"><span data-stu-id="18ada-104">Contains all [Index](index-object-adox.md) objects of a table.</span></span>

## <a name="remarks"></a><span data-ttu-id="18ada-105">解説</span><span class="sxs-lookup"><span data-stu-id="18ada-105">Remarks</span></span>

<span data-ttu-id="18ada-p101">[Indexes](append-method-adox-indexes.md) コレクションの **Append** メソッドは、ADOX に対して一意です。次のことができます。</span><span class="sxs-lookup"><span data-stu-id="18ada-p101">The [Append](append-method-adox-indexes.md) method for an **Indexes** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="18ada-108">**Append** メソッドを使用して、新しいインデックスをコレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="18ada-108">Add a new index to the collection with the **Append** method.</span></span>

<span data-ttu-id="18ada-p102">残りのプロパティとメソッドは、ADO コレクションに標準で装備されています。次のことができます。</span><span class="sxs-lookup"><span data-stu-id="18ada-p102">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="18ada-111">[Item](item-property-ado.md) プロパティを使用して、コレクションのインデックスにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="18ada-111">Access an index in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="18ada-112">[Count](count-property-ado.md) プロパティを使用して、コレクションに含まれるインデックスの数を返します。</span><span class="sxs-lookup"><span data-stu-id="18ada-112">Return the number of indexes contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="18ada-113">[Delete](delete-method-adox-collections.md) メソッドを使用して、コレクションからインデックスを削除します。</span><span class="sxs-lookup"><span data-stu-id="18ada-113">Remove an index from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="18ada-114">[Refresh](refresh-method-ado.md) メソッドを使用して、コレクションのオブジェクトを更新し、カレント データベースのスキーマを反映します。</span><span class="sxs-lookup"><span data-stu-id="18ada-114">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>

