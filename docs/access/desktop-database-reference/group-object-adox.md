---
title: Group オブジェクト (ADOX)
TOCTitle: Group Object (ADOX)
ms:assetid: 91cf1b87-c928-1d89-2731-138f6299cc60
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249642(v=office.15)
ms:contentKeyID: 48546359
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 21caab66c16c4ca9f77c49f33bf99f4df7be79c7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478612"
---
# <a name="group-object-adox"></a><span data-ttu-id="2286a-102">Group オブジェクト (ADOX)</span><span class="sxs-lookup"><span data-stu-id="2286a-102">Group Object (ADOX)</span></span>


<span data-ttu-id="2286a-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="2286a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2286a-104">保護されているデータベースへの権限を持つグループ アカウントを表します。</span><span class="sxs-lookup"><span data-stu-id="2286a-104">Represents a group account that has access permissions within a secured database.</span></span>

## <a name="remarks"></a><span data-ttu-id="2286a-105">解説</span><span class="sxs-lookup"><span data-stu-id="2286a-105">Remarks</span></span>

<span data-ttu-id="2286a-p101">[Catalog](groups-collection-adox.md) の [Groups](catalog-object-adox.md) コレクションは、カタログのすべてのグループ アカウントを表します。 **User** の [Groups](user-object-adox.md) コレクションは、ユーザーが属するグループのみを表します。</span><span class="sxs-lookup"><span data-stu-id="2286a-p101">The [Groups](groups-collection-adox.md) collection of a [Catalog](catalog-object-adox.md) represents all the catalog's group accounts. The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="2286a-108">**Group** オブジェクトのプロパティ、コレクション、およびメソッドを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="2286a-108">With the properties, collections, and methods of a **Group** object, you can:</span></span>

  - <span data-ttu-id="2286a-109">[Name](name-property-adox.md) プロパティを使用して、グループを識別します。</span><span class="sxs-lookup"><span data-stu-id="2286a-109">Identify the group with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="2286a-110">[GetPermissions](getpermissions-method-adox.md) メソッドと [SetPermissions](setpermissions-method-adox.md) メソッドを使用して、グループが読み取り、書き込み、および削除の各権限を持っているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="2286a-110">Determine whether a group has read, write, or delete permissions with the [GetPermissions](getpermissions-method-adox.md) and [SetPermissions](setpermissions-method-adox.md) methods.</span></span>

  - <span data-ttu-id="2286a-111">[Users](users-collection-adox.md) コレクションを使用して、グループのメンバーシップを持っているユーザー アカウントにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="2286a-111">Access the user accounts that have memberships in the group with the [Users](users-collection-adox.md) collection.</span></span>

  - <span data-ttu-id="2286a-112">[Properties](properties-collection-ado.md) コレクションを使用して、プロバイダー固有のプロパティにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="2286a-112">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>

