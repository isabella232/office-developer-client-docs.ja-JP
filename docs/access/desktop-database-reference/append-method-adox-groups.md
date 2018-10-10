---
title: Append メソッド (ADOX Groups)
TOCTitle: Append Method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 76c602896a629881d06a3f3cf80326e02340186e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479255"
---
# <a name="append-method-adox-groups"></a><span data-ttu-id="ae851-102">Append メソッド (ADOX Groups)</span><span class="sxs-lookup"><span data-stu-id="ae851-102">Append Method (ADOX Groups)</span></span>


<span data-ttu-id="ae851-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="ae851-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="ae851-104">新しい [Group](group-object-adox.md) オブジェクトを [Groups](groups-collection-adox.md) コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="ae851-104">Adds a new [Group](group-object-adox.md) object to the [Groups](groups-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae851-105">構文</span><span class="sxs-lookup"><span data-stu-id="ae851-105">Syntax</span></span>

<span data-ttu-id="ae851-106">*グループ*です。*グループ*を追加します。</span><span class="sxs-lookup"><span data-stu-id="ae851-106">*Groups*.Append*Group*</span></span>

## <a name="parameters"></a><span data-ttu-id="ae851-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae851-107">Parameters</span></span>

  - <span data-ttu-id="ae851-108">*Group*</span><span class="sxs-lookup"><span data-stu-id="ae851-108">*Group*</span></span>

  - <span data-ttu-id="ae851-109">追加する **Group** オブジェクトを指定します。または、新たに作成して追加するグループの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="ae851-109">The **Group** object to append or the name of the group to create and append.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae851-110">解説</span><span class="sxs-lookup"><span data-stu-id="ae851-110">Remarks</span></span>

<span data-ttu-id="ae851-p101">**Catalog** の [Groups](catalog-object-adox.md) コレクションは、そのカタログのすべてのグループ アカウントを表します。 **User** の [Groups](user-object-adox.md) コレクションは、ユーザーが属するグループのみを表します。</span><span class="sxs-lookup"><span data-stu-id="ae851-p101">The **Groups** collection of a [Catalog](catalog-object-adox.md) represents all of the catalog's group accounts. The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="ae851-113">プロバイダーがグループの作成をサポートしていない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="ae851-113">An error will occur if the provider does not support creating groups.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ae851-114">[!メモ] <STRONG>Group</STRONG> オブジェクトを <STRONG>User</STRONG> オブジェクトの <STRONG>Groups</STRONG> コレクションに追加する前に、追加するものと同じ <STRONG>Name プロパティ (ADOX)</STRONG> を持つ <A href="name-property-adox.md">Group</A> オブジェクトが、あらかじめ <STRONG>Catalog</STRONG> の <STRONG>Groups</STRONG> コレクションに存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae851-114">Before appending a <STRONG>Group</STRONG> object to the <STRONG>Groups</STRONG> collection of a <STRONG>User</STRONG> object, a <STRONG>Group</STRONG> object with the same <A href="name-property-adox.md">Name</A> as the one to be appended must already exist in the <STRONG>Groups</STRONG> collection of the <STRONG>Catalog</STRONG>.</span></span></P>


