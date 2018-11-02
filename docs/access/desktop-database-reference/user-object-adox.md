---
title: ユーザー オブジェクト (ADOX のデスクトップのデータベース参照のアクセス)
TOCTitle: User object (ADOX)
ms:assetid: e88b9a8a-e70f-c7ca-cb8c-bd274ff24948
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250178(v=office.15)
ms:contentKeyID: 48548426
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 845697f54ea5e37e051836896b84d8a3ff061237
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919880"
---
# <a name="user-object-adox"></a><span data-ttu-id="06405-102">User オブジェクト (ADOX)</span><span class="sxs-lookup"><span data-stu-id="06405-102">User object (ADOX)</span></span>


<span data-ttu-id="06405-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="06405-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="06405-104">保護されているデータベースへの権限を持つユーザー アカウントを表します。</span><span class="sxs-lookup"><span data-stu-id="06405-104">Represents a user account that has access permissions within a secured database.</span></span>

## <a name="remarks"></a><span data-ttu-id="06405-105">解説</span><span class="sxs-lookup"><span data-stu-id="06405-105">Remarks</span></span>

<span data-ttu-id="06405-p101">[Catalog](users-collection-adox.md) の [Users](catalog-object-adox.md) コレクションは、カタログのすべてのユーザーを表します。 **Group** の [Users](group-object-adox.md) コレクションは、特定のグループのユーザーのみを表します。</span><span class="sxs-lookup"><span data-stu-id="06405-p101">The [Users](users-collection-adox.md) collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users. The **Users** collection for a [Group](group-object-adox.md) represents only the users of the specific group.</span></span>

<span data-ttu-id="06405-108">**User** オブジェクトのプロパティ、コレクション、およびメソッドを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="06405-108">With the properties, collections, and methods of a **User** object, you can:</span></span>

  - <span data-ttu-id="06405-109">[Name](name-property-adox.md) プロパティを使用して、ユーザーを識別します。</span><span class="sxs-lookup"><span data-stu-id="06405-109">Identify the user with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="06405-110">[ChangePassword](changepassword-method-adox.md) メソッドを使用して、ユーザーのパスワードを変更します。</span><span class="sxs-lookup"><span data-stu-id="06405-110">Change the password for a user with the [ChangePassword](changepassword-method-adox.md) method.</span></span>

  - <span data-ttu-id="06405-111">[GetPermissions](getpermissions-method-adox.md) メソッドと [SetPermissions](setpermissions-method-adox.md) メソッドを使用して、ユーザーが読み取り、書き込み、および削除の各権限を持っているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="06405-111">Determine whether a user has read, write, or delete permissions with the [GetPermissions](getpermissions-method-adox.md) and [SetPermissions](setpermissions-method-adox.md) methods.</span></span>

  - <span data-ttu-id="06405-112">[Groups](groups-collection-adox.md) コレクションを使用して、ユーザーが属するグループにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="06405-112">Access the groups to which a user belongs with the [Groups](groups-collection-adox.md) collection.</span></span>

  - <span data-ttu-id="06405-113">[Properties](properties-collection-ado.md) コレクションを使用して、プロバイダー固有のプロパティにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="06405-113">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>

