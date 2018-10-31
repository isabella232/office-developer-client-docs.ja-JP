---
title: Append メソッド (ADOX Groups)
TOCTitle: Append Method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be31cc01122aa24eff2acb8396be2caab33c7dd4
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863060"
---
# <a name="append-method-adox-groups"></a><span data-ttu-id="bf9ac-102">Append メソッド (ADOX Groups)</span><span class="sxs-lookup"><span data-stu-id="bf9ac-102">Append Method (ADOX Groups)</span></span>


<span data-ttu-id="bf9ac-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="bf9ac-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="bf9ac-104">新しい [Group](group-object-adox.md) オブジェクトを [Groups](groups-collection-adox.md) コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="bf9ac-104">Adds a new [Group](group-object-adox.md) object to the [Groups](groups-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf9ac-105">構文</span><span class="sxs-lookup"><span data-stu-id="bf9ac-105">Syntax</span></span>

<span data-ttu-id="bf9ac-106">*グループ*です。*グループ*を追加します。</span><span class="sxs-lookup"><span data-stu-id="bf9ac-106">*Groups*.Append*Group*</span></span>

## <a name="parameters"></a><span data-ttu-id="bf9ac-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bf9ac-107">Parameters</span></span>

  - <span data-ttu-id="bf9ac-108">*Group*</span><span class="sxs-lookup"><span data-stu-id="bf9ac-108">*Group*</span></span>

  - <span data-ttu-id="bf9ac-109">追加する **Group** オブジェクトを指定します。または、新たに作成して追加するグループの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="bf9ac-109">The **Group** object to append or the name of the group to create and append.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf9ac-110">解説</span><span class="sxs-lookup"><span data-stu-id="bf9ac-110">Remarks</span></span>

<span data-ttu-id="bf9ac-p101">**Catalog** の [Groups](catalog-object-adox.md) コレクションは、そのカタログのすべてのグループ アカウントを表します。 **User** の [Groups](user-object-adox.md) コレクションは、ユーザーが属するグループのみを表します。</span><span class="sxs-lookup"><span data-stu-id="bf9ac-p101">The **Groups** collection of a [Catalog](catalog-object-adox.md) represents all of the catalog's group accounts. The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="bf9ac-113">プロバイダーがグループの作成をサポートしていない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="bf9ac-113">An error will occur if the provider does not support creating groups.</span></span>


> [!NOTE]
> <span data-ttu-id="bf9ac-114">[!メモ] **Group** オブジェクトを **User** オブジェクトの **Groups** コレクションに追加する前に、追加するものと同じ **Name プロパティ (ADOX)** を持つ [Group](name-property-adox.md) オブジェクトが、あらかじめ **Catalog** の **Groups** コレクションに存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="bf9ac-114">Before appending a **Group** object to the **Groups** collection of a **User** object, a **Group** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Groups** collection of the **Catalog**.</span></span>


