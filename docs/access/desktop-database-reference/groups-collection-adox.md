---
title: Groups コレクション (ADOX)
TOCTitle: Groups collection (ADOX)
ms:assetid: 9aec57df-bc5c-f9b3-5aec-e7e7efa47ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249702(v=office.15)
ms:contentKeyID: 48546553
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b7bd2519af3ea3c35d8cc32ef1ec31ea4f9efa1e
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936673"
---
# <a name="groups-collection-adox"></a><span data-ttu-id="cfb37-102">Groups コレクション (ADOX)</span><span class="sxs-lookup"><span data-stu-id="cfb37-102">Groups collection (ADOX)</span></span>

<span data-ttu-id="cfb37-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="cfb37-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cfb37-104">カタログまたはユーザーのすべての格納された [Group](group-object-adox.md) オブジェクトを含みます。</span><span class="sxs-lookup"><span data-stu-id="cfb37-104">Contains all stored [Group](group-object-adox.md) objects of a catalog or user.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfb37-105">解説</span><span class="sxs-lookup"><span data-stu-id="cfb37-105">Remarks</span></span>

<span data-ttu-id="cfb37-p101">**Catalog** の [Groups](catalog-object-adox.md) コレクションは、そのカタログのすべてのグループ アカウントを表します。 **User** の [Groups](user-object-adox.md) コレクションは、ユーザーが属するグループのみを表します。</span><span class="sxs-lookup"><span data-stu-id="cfb37-p101">The **Groups** collection of a [Catalog](catalog-object-adox.md) represents all of the catalog's group accounts. The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="cfb37-p102">[Groups](append-method-adox-groups.md) コレクションの **Append** メソッドは、ADOX に対して一意です。次のことができます。</span><span class="sxs-lookup"><span data-stu-id="cfb37-p102">The [Append](append-method-adox-groups.md) method for a **Groups** collection is unique for ADOX. You can:</span></span>

- <span data-ttu-id="cfb37-110">**Append** メソッドを使用して、新しいセキュリティ グループをコレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="cfb37-110">Add a new security group to the collection with the **Append** method.</span></span>

<span data-ttu-id="cfb37-p103">残りのプロパティとメソッドは、ADO コレクションに標準で装備されています。次のことができます。</span><span class="sxs-lookup"><span data-stu-id="cfb37-p103">The remaining properties and methods are standard to ADO collections. You can:</span></span>

- <span data-ttu-id="cfb37-113">[Item](item-property-ado.md) プロパティを使用して、コレクションのグループにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="cfb37-113">Access a group in the collection with the [Item](item-property-ado.md) property.</span></span>

- <span data-ttu-id="cfb37-114">[Count](count-property-ado.md) プロパティを使用して、コレクションに含まれるグループの数を返します。</span><span class="sxs-lookup"><span data-stu-id="cfb37-114">Return the number of groups contained in the collection with the [Count](count-property-ado.md) property.</span></span>

- <span data-ttu-id="cfb37-115">[Delete](delete-method-adox-collections.md) メソッドを使用して、コレクションからグループを削除します。</span><span class="sxs-lookup"><span data-stu-id="cfb37-115">Remove a group from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

- <span data-ttu-id="cfb37-116">[Refresh](refresh-method-ado.md) メソッドを使用して、コレクションのオブジェクトを更新し、カレント データベースのスキーマを反映します。</span><span class="sxs-lookup"><span data-stu-id="cfb37-116">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>

> [!NOTE]
> <span data-ttu-id="cfb37-117">[!メモ] **Group** オブジェクトを **User** オブジェクトの **Groups** コレクションに追加する前に、追加するものと同じ **Name プロパティ (ADOX)** を持つ [Group](name-property-adox.md) オブジェクトが、あらかじめ **Catalog** の **Groups** コレクションに存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="cfb37-117">Before appending a **Group** object to the **Groups** collection of a **User** object, a **Group** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Groups** collection of the **Catalog**.</span></span>


