---
title: Delete メソッド (ADOX コレクション)
TOCTitle: Delete method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54c67848d321125af44d9f5bf50f3aa582b043bb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708635"
---
# <a name="delete-method-adox-collections"></a><span data-ttu-id="9d3bb-102">Delete メソッド (ADOX コレクション)</span><span class="sxs-lookup"><span data-stu-id="9d3bb-102">Delete method (ADOX Collections)</span></span>

<span data-ttu-id="9d3bb-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="9d3bb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9d3bb-104">コレクションからオブジェクトを削除します。</span><span class="sxs-lookup"><span data-stu-id="9d3bb-104">Removes an object from a collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d3bb-105">構文</span><span class="sxs-lookup"><span data-stu-id="9d3bb-105">Syntax</span></span>

<span data-ttu-id="9d3bb-106">*コレクション*です。*名前*を削除します。</span><span class="sxs-lookup"><span data-stu-id="9d3bb-106">*Collection*.Delete*Name*</span></span>

## <a name="parameters"></a><span data-ttu-id="9d3bb-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9d3bb-107">Parameters</span></span>

|<span data-ttu-id="9d3bb-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9d3bb-108">Parameter</span></span>|<span data-ttu-id="9d3bb-109">説明</span><span class="sxs-lookup"><span data-stu-id="9d3bb-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="9d3bb-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="9d3bb-110">*Name*</span></span> |<span data-ttu-id="9d3bb-111">削除するオブジェクトの名前または位置 (インデックス) を示すバリアント型 ( **Variant** ) を指定します。</span><span class="sxs-lookup"><span data-stu-id="9d3bb-111">A **Variant** that specifies the name or ordinal position (index) of the object to delete.</span></span>|

## <a name="remarks"></a><span data-ttu-id="9d3bb-112">解説</span><span class="sxs-lookup"><span data-stu-id="9d3bb-112">Remarks</span></span>

<span data-ttu-id="9d3bb-113">*名*がコレクション内に存在しない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="9d3bb-113">An error will occur if the *Name* does not exist in the collection.</span></span>

<span data-ttu-id="9d3bb-p101">[Tables](tables-collection-adox.md) コレクションおよび [Users](users-collection-adox.md) コレクションでは、プロバイダーがテーブルやユーザーの削除をサポートしていない場合、それぞれエラーが発生します。 [Procedures](procedures-collection-adox.md) コレクションおよび [Views](views-collection-adox.md) コレクションでは、プロバイダーが持続的なコマンドをサポートしていない場合、 **Delete** は失敗します。</span><span class="sxs-lookup"><span data-stu-id="9d3bb-p101">For [Tables](tables-collection-adox.md) and [Users](users-collection-adox.md) collections, an error will occur if the provider does not support deleting tables or users, respectively. For [Procedures](procedures-collection-adox.md) and [Views](views-collection-adox.md) collections, **Delete** will fail if the provider does not support persisting commands.</span></span>

