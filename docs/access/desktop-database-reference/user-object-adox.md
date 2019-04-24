---
title: User オブジェクト (ADOX-Access デスクトップデータベースリファレンス)
TOCTitle: User object (ADOX)
ms:assetid: e88b9a8a-e70f-c7ca-cb8c-bd274ff24948
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250178(v=office.15)
ms:contentKeyID: 48548426
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3299a6c0742e7fcbbd26532f3522fdc96b7956b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313161"
---
# <a name="user-object-adox"></a><span data-ttu-id="ee034-102">User オブジェクト (ADOX)</span><span class="sxs-lookup"><span data-stu-id="ee034-102">User object (ADOX)</span></span>


<span data-ttu-id="ee034-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee034-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ee034-104">保護されているデータベースへの権限を持つユーザー アカウントを表します。</span><span class="sxs-lookup"><span data-stu-id="ee034-104">Represents a user account that has access permissions within a secured database.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee034-105">注釈</span><span class="sxs-lookup"><span data-stu-id="ee034-105">Remarks</span></span>

<span data-ttu-id="ee034-p101">[Catalog](users-collection-adox.md) の [Users](catalog-object-adox.md) コレクションは、カタログのすべてのユーザーを表します。 **Group** の [Users](group-object-adox.md) コレクションは、特定のグループのユーザーのみを表します。</span><span class="sxs-lookup"><span data-stu-id="ee034-p101">The [Users](users-collection-adox.md) collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users. The **Users** collection for a [Group](group-object-adox.md) represents only the users of the specific group.</span></span>

<span data-ttu-id="ee034-108">**User** オブジェクトのプロパティ、コレクション、およびメソッドを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="ee034-108">With the properties, collections, and methods of a **User** object, you can:</span></span>

  - <span data-ttu-id="ee034-109">[Name](name-property-adox.md) プロパティを使用して、ユーザーを識別します。</span><span class="sxs-lookup"><span data-stu-id="ee034-109">Identify the user with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="ee034-110">[ChangePassword](changepassword-method-adox.md) メソッドを使用して、ユーザーのパスワードを変更します。</span><span class="sxs-lookup"><span data-stu-id="ee034-110">Change the password for a user with the [ChangePassword](changepassword-method-adox.md) method.</span></span>

  - <span data-ttu-id="ee034-111">[GetPermissions](getpermissions-method-adox.md) メソッドと [SetPermissions](setpermissions-method-adox.md) メソッドを使用して、ユーザーが読み取り、書き込み、および削除の各権限を持っているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="ee034-111">Determine whether a user has read, write, or delete permissions with the [GetPermissions](getpermissions-method-adox.md) and [SetPermissions](setpermissions-method-adox.md) methods.</span></span>

  - <span data-ttu-id="ee034-112">[Groups](groups-collection-adox.md) コレクションを使用して、ユーザーが属するグループにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="ee034-112">Access the groups to which a user belongs with the [Groups](groups-collection-adox.md) collection.</span></span>

  - <span data-ttu-id="ee034-113">[Properties](properties-collection-ado.md) コレクションを使用して、プロバイダー固有のプロパティにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="ee034-113">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>

