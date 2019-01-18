---
title: Keys コレクション (ADOX)
TOCTitle: Keys collection (ADOX)
ms:assetid: 0d480c01-1b36-28b9-9135-51958f313995
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248854(v=office.15)
ms:contentKeyID: 48543215
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f43e6643e585ed8c28cd710e0674523b84d12d89
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711400"
---
# <a name="keys-collection-adox"></a><span data-ttu-id="27353-102">Keys コレクション (ADOX)</span><span class="sxs-lookup"><span data-stu-id="27353-102">Keys collection (ADOX)</span></span>


<span data-ttu-id="27353-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="27353-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="27353-104">テーブルのすべての [Key](key-object-adox.md) オブジェクトを含みます。</span><span class="sxs-lookup"><span data-stu-id="27353-104">Contains all [Key](key-object-adox.md) objects of a table.</span></span>

## <a name="remarks"></a><span data-ttu-id="27353-105">解説</span><span class="sxs-lookup"><span data-stu-id="27353-105">Remarks</span></span>

<span data-ttu-id="27353-p101">[Keys](append-method-adox-keys.md) コレクションの **Append** メソッドは、ADOX に対して一意です。次のことができます。</span><span class="sxs-lookup"><span data-stu-id="27353-p101">The [Append](append-method-adox-keys.md) method for a **Keys** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="27353-108">**Append** メソッドを使用して、新しいキーをコレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="27353-108">Add a new key to the collection with the **Append** method.</span></span>

<span data-ttu-id="27353-p102">残りのプロパティとメソッドは、ADO コレクションに標準で装備されています。次のことができます。</span><span class="sxs-lookup"><span data-stu-id="27353-p102">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="27353-111">[Item](item-property-ado.md) プロパティを使用して、コレクションのキーにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="27353-111">Access a key in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="27353-112">[Count](count-property-ado.md) プロパティを使用して、コレクションに含まれるキーの数を返します。</span><span class="sxs-lookup"><span data-stu-id="27353-112">Return the number of keys contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="27353-113">[Delete](delete-method-adox-collections.md) メソッドを使用して、コレクションからキーを削除します。</span><span class="sxs-lookup"><span data-stu-id="27353-113">Remove a key from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="27353-114">[Refresh](refresh-method-ado.md) メソッドを使用して、コレクションのオブジェクトを更新し、カレント データベースのスキーマを反映します。</span><span class="sxs-lookup"><span data-stu-id="27353-114">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>

