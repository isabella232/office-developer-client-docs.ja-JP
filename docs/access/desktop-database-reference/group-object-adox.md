---
title: Group オブジェクト (ADOX)
TOCTitle: Group object (ADOX)
ms:assetid: 91cf1b87-c928-1d89-2731-138f6299cc60
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249642(v=office.15)
ms:contentKeyID: 48546359
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b7196fd6a57292cb335f164d25807f19544076aa
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925956"
---
# <a name="group-object-adox"></a><span data-ttu-id="fa080-102">Group オブジェクト (ADOX)</span><span class="sxs-lookup"><span data-stu-id="fa080-102">Group object (ADOX)</span></span>


<span data-ttu-id="fa080-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="fa080-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fa080-104">保護されているデータベースへの権限を持つグループ アカウントを表します。</span><span class="sxs-lookup"><span data-stu-id="fa080-104">Represents a group account that has access permissions within a secured database.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa080-105">解説</span><span class="sxs-lookup"><span data-stu-id="fa080-105">Remarks</span></span>

<span data-ttu-id="fa080-p101">[Catalog](groups-collection-adox.md) の [Groups](catalog-object-adox.md) コレクションは、カタログのすべてのグループ アカウントを表します。 **User** の [Groups](user-object-adox.md) コレクションは、ユーザーが属するグループのみを表します。</span><span class="sxs-lookup"><span data-stu-id="fa080-p101">The [Groups](groups-collection-adox.md) collection of a [Catalog](catalog-object-adox.md) represents all the catalog's group accounts. The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="fa080-108">**Group** オブジェクトのプロパティ、コレクション、およびメソッドを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="fa080-108">With the properties, collections, and methods of a **Group** object, you can:</span></span>

  - <span data-ttu-id="fa080-109">[Name](name-property-adox.md) プロパティを使用して、グループを識別します。</span><span class="sxs-lookup"><span data-stu-id="fa080-109">Identify the group with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="fa080-110">[GetPermissions](getpermissions-method-adox.md) メソッドと [SetPermissions](setpermissions-method-adox.md) メソッドを使用して、グループが読み取り、書き込み、および削除の各権限を持っているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="fa080-110">Determine whether a group has read, write, or delete permissions with the [GetPermissions](getpermissions-method-adox.md) and [SetPermissions](setpermissions-method-adox.md) methods.</span></span>

  - <span data-ttu-id="fa080-111">[Users](users-collection-adox.md) コレクションを使用して、グループのメンバーシップを持っているユーザー アカウントにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="fa080-111">Access the user accounts that have memberships in the group with the [Users](users-collection-adox.md) collection.</span></span>

  - <span data-ttu-id="fa080-112">[Properties](properties-collection-ado.md) コレクションを使用して、プロバイダー固有のプロパティにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="fa080-112">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>

