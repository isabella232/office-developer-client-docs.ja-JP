---
title: Delete メソッド (ADOX コレクション)
TOCTitle: Delete method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b5fdcd80a49d7d9d14ba17a85f675fdfd9906c1b
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921664"
---
# <a name="delete-method-adox-collections"></a><span data-ttu-id="87f6f-102">Delete メソッド (ADOX コレクション)</span><span class="sxs-lookup"><span data-stu-id="87f6f-102">Delete method (ADOX Collections)</span></span>


<span data-ttu-id="87f6f-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="87f6f-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="87f6f-104">コレクションからオブジェクトを削除します。</span><span class="sxs-lookup"><span data-stu-id="87f6f-104">Removes an object from a collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="87f6f-105">構文</span><span class="sxs-lookup"><span data-stu-id="87f6f-105">Syntax</span></span>

<span data-ttu-id="87f6f-106">*コレクション*です。*名前*を削除します。</span><span class="sxs-lookup"><span data-stu-id="87f6f-106">*Collection*.Delete*Name*</span></span>

## <a name="parameters"></a><span data-ttu-id="87f6f-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="87f6f-107">Parameters</span></span>

  - <span data-ttu-id="87f6f-108">*Name*</span><span class="sxs-lookup"><span data-stu-id="87f6f-108">*Name*</span></span>

  - <span data-ttu-id="87f6f-109">削除するオブジェクトの名前または位置 (インデックス) を示すバリアント型 ( **Variant** ) を指定します。</span><span class="sxs-lookup"><span data-stu-id="87f6f-109">A **Variant** that specifies the name or ordinal position (index) of the object to delete.</span></span>

## <a name="remarks"></a><span data-ttu-id="87f6f-110">解説</span><span class="sxs-lookup"><span data-stu-id="87f6f-110">Remarks</span></span>

<span data-ttu-id="87f6f-111">*名*がコレクション内に存在しない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="87f6f-111">An error will occur if the *Name* does not exist in the collection.</span></span>

<span data-ttu-id="87f6f-p101">[Tables](tables-collection-adox.md) コレクションおよび [Users](users-collection-adox.md) コレクションでは、プロバイダーがテーブルやユーザーの削除をサポートしていない場合、それぞれエラーが発生します。 [Procedures](procedures-collection-adox.md) コレクションおよび [Views](views-collection-adox.md) コレクションでは、プロバイダーが持続的なコマンドをサポートしていない場合、 **Delete** は失敗します。</span><span class="sxs-lookup"><span data-stu-id="87f6f-p101">For [Tables](tables-collection-adox.md) and [Users](users-collection-adox.md) collections, an error will occur if the provider does not support deleting tables or users, respectively. For [Procedures](procedures-collection-adox.md) and [Views](views-collection-adox.md) collections, **Delete** will fail if the provider does not support persisting commands.</span></span>

