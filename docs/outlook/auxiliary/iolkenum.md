---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 19ec67bf033859073e7685912196369b664f4a36
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592690"
---
# <a name="iolkenum"></a><span data-ttu-id="2fed8-102">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="2fed8-102">IOlkEnum</span></span>

<span data-ttu-id="2fed8-103">[IUnknown](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nn-unknwn-iunknown)オブジェクトとしてアカウントの列挙をサポートします。</span><span class="sxs-lookup"><span data-stu-id="2fed8-103">Supports enumerating accounts as [IUnknown](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nn-unknwn-iunknown) objects.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="2fed8-104">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="2fed8-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2fed8-105">継承します。</span><span class="sxs-lookup"><span data-stu-id="2fed8-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="2fed8-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="2fed8-106">IUnknown</span></span>](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|<span data-ttu-id="2fed8-107">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="2fed8-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="2fed8-108">Outlook</span><span class="sxs-lookup"><span data-stu-id="2fed8-108">Outlook</span></span>  <br/> |
|<span data-ttu-id="2fed8-109">提供元:</span><span class="sxs-lookup"><span data-stu-id="2fed8-109">Provided by:</span></span>  <br/> |[<span data-ttu-id="2fed8-110">IOlkAccountManager::EnumerateAccounts</span><span class="sxs-lookup"><span data-stu-id="2fed8-110">IOlkAccountManager::EnumerateAccounts</span></span>](iolkaccountmanager-enumerateaccounts.md) <br/> |
|<span data-ttu-id="2fed8-111">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2fed8-111">Called by:</span></span>  <br/> |<span data-ttu-id="2fed8-112">クライアント</span><span class="sxs-lookup"><span data-stu-id="2fed8-112">Client</span></span>  <br/> |
|<span data-ttu-id="2fed8-113">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="2fed8-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2fed8-114">IID_IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="2fed8-114">IID_IOlkEnum</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="2fed8-115">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="2fed8-115">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="2fed8-116">GetCount</span><span class="sxs-lookup"><span data-stu-id="2fed8-116">GetCount</span></span>](iolkenum-getcount.md) <br/> |<span data-ttu-id="2fed8-117">列挙子では、アカウントの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="2fed8-117">Gets the number of accounts in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="2fed8-118">Reset</span><span class="sxs-lookup"><span data-stu-id="2fed8-118">Reset</span></span>](iolkenum-reset.md) <br/> |<span data-ttu-id="2fed8-119">先頭に列挙子をリセットします。</span><span class="sxs-lookup"><span data-stu-id="2fed8-119">Resets the enumerator to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="2fed8-120">GetNext</span><span class="sxs-lookup"><span data-stu-id="2fed8-120">GetNext</span></span>](iolkenum-getnext.md) <br/> |<span data-ttu-id="2fed8-121">列挙子では、次のアカウントを取得します。</span><span class="sxs-lookup"><span data-stu-id="2fed8-121">Gets the next account in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="2fed8-122">スキップ</span><span class="sxs-lookup"><span data-stu-id="2fed8-122">Skip</span></span>](iolkenum-skip.md) <br/> |<span data-ttu-id="2fed8-123">列挙子内のアカウントの指定した数をスキップします。</span><span class="sxs-lookup"><span data-stu-id="2fed8-123">Skips a specified number of accounts in the enumerator.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2fed8-124">注釈</span><span class="sxs-lookup"><span data-stu-id="2fed8-124">Remarks</span></span>

<span data-ttu-id="2fed8-125">アカウントの列挙子を取得するときは、 **IOlkAccountManager::EnumerateAccounts**によってこのインターフェイスが返されます。</span><span class="sxs-lookup"><span data-stu-id="2fed8-125">This interface is returned by **IOlkAccountManager::EnumerateAccounts** when obtaining an enumerator of accounts.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2fed8-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="2fed8-126">See also</span></span>

- [<span data-ttu-id="2fed8-127">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="2fed8-127">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="2fed8-128">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="2fed8-128">Constants (Account management API)</span></span>](constants-account-management-api.md)

