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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291581"
---
# <a name="indexes-collection-adox"></a><span data-ttu-id="f5520-102">Indexes コレクション (ADOX)</span><span class="sxs-lookup"><span data-stu-id="f5520-102">Indexes collection (ADOX)</span></span>


<span data-ttu-id="f5520-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="f5520-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f5520-104">テーブルのすべての [Index](index-object-adox.md) オブジェクトを含みます。</span><span class="sxs-lookup"><span data-stu-id="f5520-104">Contains all [Index](index-object-adox.md) objects of a table.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5520-105">注釈</span><span class="sxs-lookup"><span data-stu-id="f5520-105">Remarks</span></span>

<span data-ttu-id="f5520-p101">[Indexes](append-method-adox-indexes.md) コレクションの **Append** メソッドは、ADOX に対して一意です。次のことができます。</span><span class="sxs-lookup"><span data-stu-id="f5520-p101">The [Append](append-method-adox-indexes.md) method for an **Indexes** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="f5520-108">**Append** メソッドを使用して、新しいインデックスをコレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="f5520-108">Add a new index to the collection with the **Append** method.</span></span>

<span data-ttu-id="f5520-p102">残りのプロパティとメソッドは、ADO コレクションに標準で装備されています。次のことができます。</span><span class="sxs-lookup"><span data-stu-id="f5520-p102">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="f5520-111">[Item](item-property-ado.md) プロパティを使用して、コレクションのインデックスにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="f5520-111">Access an index in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="f5520-112">[Count](count-property-ado.md) プロパティを使用して、コレクションに含まれるインデックスの数を返します。</span><span class="sxs-lookup"><span data-stu-id="f5520-112">Return the number of indexes contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="f5520-113">[Delete](delete-method-adox-collections.md) メソッドを使用して、コレクションからインデックスを削除します。</span><span class="sxs-lookup"><span data-stu-id="f5520-113">Remove an index from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="f5520-114">[Refresh](refresh-method-ado.md) メソッドを使用して、コレクションのオブジェクトを更新し、カレント データベースのスキーマを反映します。</span><span class="sxs-lookup"><span data-stu-id="f5520-114">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>

