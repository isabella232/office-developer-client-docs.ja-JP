---
title: Append メソッド (ADOX Users)
TOCTitle: Append Method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b8bce151e800b58e9c99c6dd6591114c53208a5c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477008"
---
# <a name="append-method-adox-users"></a><span data-ttu-id="6b2fc-102">Append メソッド (ADOX Users)</span><span class="sxs-lookup"><span data-stu-id="6b2fc-102">Append Method (ADOX Users)</span></span>


<span data-ttu-id="6b2fc-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="6b2fc-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="6b2fc-104">新しい [User](user-object-adox.md) オブジェクトを [Users](users-collection-adox.md) コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="6b2fc-104">Adds a new [User](user-object-adox.md) object to the [Users](users-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b2fc-105">構文</span><span class="sxs-lookup"><span data-stu-id="6b2fc-105">Syntax</span></span>

<span data-ttu-id="6b2fc-106">*ユーザー*です。*ユーザー*を追加する\[、*パスワード*\]</span><span class="sxs-lookup"><span data-stu-id="6b2fc-106">*Users*.Append*User*\[,*Password*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="6b2fc-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6b2fc-107">Parameters</span></span>

  - <span data-ttu-id="6b2fc-108">*User*</span><span class="sxs-lookup"><span data-stu-id="6b2fc-108">*User*</span></span>

  - <span data-ttu-id="6b2fc-109">追加する **User** オブジェクトを含むバリアント型 ( **Variant** ) の値を指定します。または、新たに作成して追加するユーザーの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="6b2fc-109">A **Variant** value that contains the **User** object to append or the name of the user to create and append.</span></span>

  - <span data-ttu-id="6b2fc-110">*Password*</span><span class="sxs-lookup"><span data-stu-id="6b2fc-110">*Password*</span></span>

  - <span data-ttu-id="6b2fc-111">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="6b2fc-111">Optional.</span></span> <span data-ttu-id="6b2fc-112">このユーザーのパスワードを含む文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="6b2fc-112">A **String** value that contains the password for the user.</span></span> <span data-ttu-id="6b2fc-113">*パスワード*パラメーターは、**ユーザー**オブジェクトの[パスワードの変更](changepassword-method-adox.md)メソッドによって指定された値に対応します。</span><span class="sxs-lookup"><span data-stu-id="6b2fc-113">The *Password* parameter corresponds to the value specified by the [ChangePassword](changepassword-method-adox.md) method of a **User** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b2fc-114">解説</span><span class="sxs-lookup"><span data-stu-id="6b2fc-114">Remarks</span></span>

<span data-ttu-id="6b2fc-p102">**Catalog** の [Users](catalog-object-adox.md) コレクションは、そのカタログのすべてのユーザーを表します。 **Group** の [Users](group-object-adox.md) コレクションは、特定のグループでメンバーシップを持つユーザーのみを表します。</span><span class="sxs-lookup"><span data-stu-id="6b2fc-p102">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users. The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="6b2fc-117">プロバイダーがユーザーの作成をサポートしていない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6b2fc-117">An error will occur if the provider does not support creating users.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6b2fc-118">[!メモ] <STRONG>User</STRONG> オブジェクトを <STRONG>Group</STRONG> オブジェクトの <STRONG>Users</STRONG> コレクションに追加する前に、追加するものと同じ <STRONG>Name プロパティ (ADOX)</STRONG> を持つ <A href="name-property-adox.md">User</A> オブジェクトが、あらかじめ <STRONG>Catalog</STRONG> の <STRONG>Users</STRONG> コレクションに存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b2fc-118">Before appending a <STRONG>User</STRONG> object to the <STRONG>Users</STRONG> collection of a <STRONG>Group</STRONG> object, a <STRONG>User</STRONG> object with the same <A href="name-property-adox.md">Name</A> as the one to be appended must already exist in the <STRONG>Users</STRONG> collection of the <STRONG>Catalog</STRONG>.</span></span></P>


