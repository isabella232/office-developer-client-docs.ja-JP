---
title: Users コレクション (ADOX)
TOCTitle: Users collection (ADOX)
ms:assetid: bc61c862-1637-02e7-4b56-5ad984bdbcb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249905(v=office.15)
ms:contentKeyID: 48547413
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3d91af56dc37cf8719a241a35046d663f7c9d57
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998073"
---
# <a name="users-collection-adox"></a><span data-ttu-id="3620b-102">Users コレクション (ADOX)</span><span class="sxs-lookup"><span data-stu-id="3620b-102">Users collection (ADOX)</span></span>

<span data-ttu-id="3620b-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="3620b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3620b-104">カタログまたはグループのすべての格納された [User](user-object-adox.md) オブジェクトを含みます。</span><span class="sxs-lookup"><span data-stu-id="3620b-104">Contains all stored [User](user-object-adox.md) objects of a catalog or group.</span></span>

## <a name="remarks"></a><span data-ttu-id="3620b-105">解説</span><span class="sxs-lookup"><span data-stu-id="3620b-105">Remarks</span></span>

<span data-ttu-id="3620b-p101">**Catalog** の [Users](catalog-object-adox.md) コレクションは、そのカタログのすべてのユーザーを表します。 **Group** の [Users](group-object-adox.md) コレクションは、特定のグループでメンバーシップを持つユーザーのみを表します。</span><span class="sxs-lookup"><span data-stu-id="3620b-p101">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users. The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="3620b-p102">[Users](append-method-adox-users.md) コレクションの **Append** メソッドは、ADOX に対して一意です。次のことができます。</span><span class="sxs-lookup"><span data-stu-id="3620b-p102">The [Append](append-method-adox-users.md) method for a **Users** collection is unique for ADOX. You can:</span></span>

- <span data-ttu-id="3620b-110">**Append** メソッドを使用して、新しいユーザーをコレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="3620b-110">Add a new user to the collection with the **Append** method.</span></span>

<span data-ttu-id="3620b-p103">残りのプロパティとメソッドは、ADO コレクションに標準で装備されています。次のことができます。</span><span class="sxs-lookup"><span data-stu-id="3620b-p103">The remaining properties and methods are standard to ADO collections. You can:</span></span>

- <span data-ttu-id="3620b-113">[Item](item-property-ado.md) プロパティを使用して、コレクションのユーザーにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="3620b-113">Access a user in the collection with the [Item](item-property-ado.md) property.</span></span>

- <span data-ttu-id="3620b-114">[Count](count-property-ado.md) プロパティを使用して、コレクションに含まれるユーザーの数を返します。</span><span class="sxs-lookup"><span data-stu-id="3620b-114">Return the number of users contained in the collection with the [Count](count-property-ado.md) property.</span></span>

- <span data-ttu-id="3620b-115">[Delete](delete-method-adox-collections.md) メソッドを使用して、コレクションからユーザーを削除します。</span><span class="sxs-lookup"><span data-stu-id="3620b-115">Remove a user from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

- <span data-ttu-id="3620b-116">[Refresh](refresh-method-ado.md) メソッドを使用して、コレクションのオブジェクトを更新し、カレント データベースのスキーマを反映します。</span><span class="sxs-lookup"><span data-stu-id="3620b-116">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>

> [!NOTE]
> <span data-ttu-id="3620b-117">[!メモ] **User** オブジェクトを **Group** オブジェクトの **Users** コレクションに追加する前に、追加するものと同じ **Name プロパティ (ADOX)** を持つ [User](name-property-adox.md) オブジェクトが、あらかじめ **Catalog** の **Users** コレクションに存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="3620b-117">Before appending a **User** object to the **Users** collection of a **Group** object, a **User** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Users** collection of the **Catalog**.</span></span>

