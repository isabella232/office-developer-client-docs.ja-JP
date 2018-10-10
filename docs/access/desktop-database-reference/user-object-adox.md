---
title: ユーザー オブジェクト (ADOX のデスクトップのデータベース参照のアクセス)
TOCTitle: User Object (ADOX)
ms:assetid: e88b9a8a-e70f-c7ca-cb8c-bd274ff24948
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250178(v=office.15)
ms:contentKeyID: 48548426
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ab5d92a67737774d817046538200d0ebd4337e74
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478248"
---
# <a name="user-object-adox"></a><span data-ttu-id="5ce5c-102">User オブジェクト (ADOX)</span><span class="sxs-lookup"><span data-stu-id="5ce5c-102">User Object (ADOX)</span></span>


<span data-ttu-id="5ce5c-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="5ce5c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5ce5c-104">保護されているデータベースへの権限を持つユーザー アカウントを表します。</span><span class="sxs-lookup"><span data-stu-id="5ce5c-104">Represents a user account that has access permissions within a secured database.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ce5c-105">解説</span><span class="sxs-lookup"><span data-stu-id="5ce5c-105">Remarks</span></span>

<span data-ttu-id="5ce5c-p101">[Catalog](users-collection-adox.md) の [Users](catalog-object-adox.md) コレクションは、カタログのすべてのユーザーを表します。 **Group** の [Users](group-object-adox.md) コレクションは、特定のグループのユーザーのみを表します。</span><span class="sxs-lookup"><span data-stu-id="5ce5c-p101">The [Users](users-collection-adox.md) collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users. The **Users** collection for a [Group](group-object-adox.md) represents only the users of the specific group.</span></span>

<span data-ttu-id="5ce5c-108">**User** オブジェクトのプロパティ、コレクション、およびメソッドを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="5ce5c-108">With the properties, collections, and methods of a **User** object, you can:</span></span>

  - <span data-ttu-id="5ce5c-109">[Name](name-property-adox.md) プロパティを使用して、ユーザーを識別します。</span><span class="sxs-lookup"><span data-stu-id="5ce5c-109">Identify the user with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="5ce5c-110">[ChangePassword](changepassword-method-adox.md) メソッドを使用して、ユーザーのパスワードを変更します。</span><span class="sxs-lookup"><span data-stu-id="5ce5c-110">Change the password for a user with the [ChangePassword](changepassword-method-adox.md) method.</span></span>

  - <span data-ttu-id="5ce5c-111">[GetPermissions](getpermissions-method-adox.md) メソッドと [SetPermissions](setpermissions-method-adox.md) メソッドを使用して、ユーザーが読み取り、書き込み、および削除の各権限を持っているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="5ce5c-111">Determine whether a user has read, write, or delete permissions with the [GetPermissions](getpermissions-method-adox.md) and [SetPermissions](setpermissions-method-adox.md) methods.</span></span>

  - <span data-ttu-id="5ce5c-112">[Groups](groups-collection-adox.md) コレクションを使用して、ユーザーが属するグループにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="5ce5c-112">Access the groups to which a user belongs with the [Groups](groups-collection-adox.md) collection.</span></span>

  - <span data-ttu-id="5ce5c-113">[Properties](properties-collection-ado.md) コレクションを使用して、プロバイダー固有のプロパティにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="5ce5c-113">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>

