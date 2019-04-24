---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 59f43e8b3b0819b0178d60fa357e01937ae19d81
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322100"
---
# <a name="iolkenum"></a><span data-ttu-id="5ab9b-102">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="5ab9b-102">IOlkEnum</span></span>

<span data-ttu-id="5ab9b-103">[IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown)オブジェクトとしてのアカウントの列挙をサポートします。</span><span class="sxs-lookup"><span data-stu-id="5ab9b-103">Supports enumerating accounts as [IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) objects.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="5ab9b-104">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="5ab9b-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5ab9b-105">継承元:</span><span class="sxs-lookup"><span data-stu-id="5ab9b-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="5ab9b-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="5ab9b-106">IUnknown</span></span>](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|<span data-ttu-id="5ab9b-107">実装元:</span><span class="sxs-lookup"><span data-stu-id="5ab9b-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="5ab9b-108">Outlook</span><span class="sxs-lookup"><span data-stu-id="5ab9b-108">Outlook</span></span>  <br/> |
|<span data-ttu-id="5ab9b-109">提供元:</span><span class="sxs-lookup"><span data-stu-id="5ab9b-109">Provided by:</span></span>  <br/> |[<span data-ttu-id="5ab9b-110">IOlkAccountManager::EnumerateAccounts</span><span class="sxs-lookup"><span data-stu-id="5ab9b-110">IOlkAccountManager::EnumerateAccounts</span></span>](iolkaccountmanager-enumerateaccounts.md) <br/> |
|<span data-ttu-id="5ab9b-111">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="5ab9b-111">Called by:</span></span>  <br/> |<span data-ttu-id="5ab9b-112">クライアント</span><span class="sxs-lookup"><span data-stu-id="5ab9b-112">Client</span></span>  <br/> |
|<span data-ttu-id="5ab9b-113">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="5ab9b-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="5ab9b-114">IID_IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="5ab9b-114">IID_IOlkEnum</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="5ab9b-115">v の順序</span><span class="sxs-lookup"><span data-stu-id="5ab9b-115">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="5ab9b-116">GetCount</span><span class="sxs-lookup"><span data-stu-id="5ab9b-116">GetCount</span></span>](iolkenum-getcount.md) <br/> |<span data-ttu-id="5ab9b-117">列挙子内のアカウントの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="5ab9b-117">Gets the number of accounts in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="5ab9b-118">Reset</span><span class="sxs-lookup"><span data-stu-id="5ab9b-118">Reset</span></span>](iolkenum-reset.md) <br/> |<span data-ttu-id="5ab9b-119">列挙子を最初にリセットします。</span><span class="sxs-lookup"><span data-stu-id="5ab9b-119">Resets the enumerator to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="5ab9b-120">GetNext</span><span class="sxs-lookup"><span data-stu-id="5ab9b-120">GetNext</span></span>](iolkenum-getnext.md) <br/> |<span data-ttu-id="5ab9b-121">列挙子の次のアカウントを取得します。</span><span class="sxs-lookup"><span data-stu-id="5ab9b-121">Gets the next account in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="5ab9b-122">Skip</span><span class="sxs-lookup"><span data-stu-id="5ab9b-122">Skip</span></span>](iolkenum-skip.md) <br/> |<span data-ttu-id="5ab9b-123">列挙子内の指定された数のアカウントをスキップします。</span><span class="sxs-lookup"><span data-stu-id="5ab9b-123">Skips a specified number of accounts in the enumerator.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ab9b-124">解説</span><span class="sxs-lookup"><span data-stu-id="5ab9b-124">Remarks</span></span>

<span data-ttu-id="5ab9b-125">このインターフェイスは、アカウントの列挙子を取得するときに、 **IOlkAccountManager:: EnumerateAccounts**によって返されます。</span><span class="sxs-lookup"><span data-stu-id="5ab9b-125">This interface is returned by **IOlkAccountManager::EnumerateAccounts** when obtaining an enumerator of accounts.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5ab9b-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="5ab9b-126">See also</span></span>

- [<span data-ttu-id="5ab9b-127">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="5ab9b-127">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="5ab9b-128">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="5ab9b-128">Constants (Account management API)</span></span>](constants-account-management-api.md)

