---
title: Append メソッド (ADOX Groups)
TOCTitle: Append method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9f0e7731777e3d82e3746c3886bdbddb3e43db66
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297103"
---
# <a name="append-method-adox-groups"></a><span data-ttu-id="a6743-102">Append メソッド (ADOX Groups)</span><span class="sxs-lookup"><span data-stu-id="a6743-102">Append method (ADOX Groups)</span></span>

<span data-ttu-id="a6743-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="a6743-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a6743-104">新しい [Group](group-object-adox.md) オブジェクトを [Groups](groups-collection-adox.md) コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="a6743-104">Adds a new [Group](group-object-adox.md) object to the [Groups](groups-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6743-105">構文</span><span class="sxs-lookup"><span data-stu-id="a6743-105">Syntax</span></span>

<span data-ttu-id="a6743-106">*グループ*。*グループ*の追加</span><span class="sxs-lookup"><span data-stu-id="a6743-106">*Groups*.Append*Group*</span></span>

## <a name="parameters"></a><span data-ttu-id="a6743-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a6743-107">Parameters</span></span>

|<span data-ttu-id="a6743-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a6743-108">Parameter</span></span>|<span data-ttu-id="a6743-109">説明</span><span class="sxs-lookup"><span data-stu-id="a6743-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a6743-110">*Group*</span><span class="sxs-lookup"><span data-stu-id="a6743-110">*Group*</span></span> |<span data-ttu-id="a6743-111">追加する **Group** オブジェクトを指定します。または、新たに作成して追加するグループの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="a6743-111">The **Group** object to append or the name of the group to create and append.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a6743-112">注釈</span><span class="sxs-lookup"><span data-stu-id="a6743-112">Remarks</span></span>

<span data-ttu-id="a6743-p101">**Catalog** の [Groups](catalog-object-adox.md) コレクションは、そのカタログのすべてのグループ アカウントを表します。 **User** の [Groups](user-object-adox.md) コレクションは、ユーザーが属するグループのみを表します。</span><span class="sxs-lookup"><span data-stu-id="a6743-p101">The **Groups** collection of a [Catalog](catalog-object-adox.md) represents all of the catalog's group accounts. The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="a6743-115">プロバイダーがグループの作成をサポートしていない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="a6743-115">An error will occur if the provider does not support creating groups.</span></span>

> [!NOTE]
> <span data-ttu-id="a6743-116">[!メモ] **Group** オブジェクトを **User** オブジェクトの **Groups** コレクションに追加する前に、追加するものと同じ **Name プロパティ (ADOX)** を持つ [Group](name-property-adox.md) オブジェクトが、あらかじめ **Catalog** の **Groups** コレクションに存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6743-116">Before appending a **Group** object to the **Groups** collection of a **User** object, a **Group** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Groups** collection of the **Catalog**.</span></span>


