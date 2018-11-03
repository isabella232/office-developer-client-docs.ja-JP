---
title: Append メソッド (ADOX Users)
TOCTitle: Append method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e8b03bb74c5442eba3e1794d8067fa709f68af3d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931366"
---
# <a name="append-method-adox-users"></a><span data-ttu-id="bec1b-102">Append メソッド (ADOX Users)</span><span class="sxs-lookup"><span data-stu-id="bec1b-102">Append method (ADOX Users)</span></span>


<span data-ttu-id="bec1b-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="bec1b-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="bec1b-104">新しい [User](user-object-adox.md) オブジェクトを [Users](users-collection-adox.md) コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="bec1b-104">Adds a new [User](user-object-adox.md) object to the [Users](users-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="bec1b-105">構文</span><span class="sxs-lookup"><span data-stu-id="bec1b-105">Syntax</span></span>

<span data-ttu-id="bec1b-106">*ユーザー*です。*ユーザー*を追加する\[、*パスワード*\]</span><span class="sxs-lookup"><span data-stu-id="bec1b-106">*Users*.Append*User*\[,*Password*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="bec1b-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bec1b-107">Parameters</span></span>

  - <span data-ttu-id="bec1b-108">*User*</span><span class="sxs-lookup"><span data-stu-id="bec1b-108">*User*</span></span>

  - <span data-ttu-id="bec1b-109">追加する **User** オブジェクトを含むバリアント型 ( **Variant** ) の値を指定します。または、新たに作成して追加するユーザーの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="bec1b-109">A **Variant** value that contains the **User** object to append or the name of the user to create and append.</span></span>

  - <span data-ttu-id="bec1b-110">*Password*</span><span class="sxs-lookup"><span data-stu-id="bec1b-110">*Password*</span></span>

  - <span data-ttu-id="bec1b-111">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="bec1b-111">Optional.</span></span> <span data-ttu-id="bec1b-112">このユーザーのパスワードを含む文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="bec1b-112">A **String** value that contains the password for the user.</span></span> <span data-ttu-id="bec1b-113">*パスワード*パラメーターは、**ユーザー**オブジェクトの[パスワードの変更](changepassword-method-adox.md)メソッドによって指定された値に対応します。</span><span class="sxs-lookup"><span data-stu-id="bec1b-113">The *Password* parameter corresponds to the value specified by the [ChangePassword](changepassword-method-adox.md) method of a **User** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bec1b-114">解説</span><span class="sxs-lookup"><span data-stu-id="bec1b-114">Remarks</span></span>

<span data-ttu-id="bec1b-p102">**Catalog** の [Users](catalog-object-adox.md) コレクションは、そのカタログのすべてのユーザーを表します。 **Group** の [Users](group-object-adox.md) コレクションは、特定のグループでメンバーシップを持つユーザーのみを表します。</span><span class="sxs-lookup"><span data-stu-id="bec1b-p102">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users. The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="bec1b-117">プロバイダーがユーザーの作成をサポートしていない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="bec1b-117">An error will occur if the provider does not support creating users.</span></span>


> [!NOTE]
> <span data-ttu-id="bec1b-118">[!メモ] **User** オブジェクトを **Group** オブジェクトの **Users** コレクションに追加する前に、追加するものと同じ **Name プロパティ (ADOX)** を持つ [User](name-property-adox.md) オブジェクトが、あらかじめ **Catalog** の **Users** コレクションに存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="bec1b-118">Before appending a **User** object to the **Users** collection of a **Group** object, a **User** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Users** collection of the **Catalog**.</span></span>


