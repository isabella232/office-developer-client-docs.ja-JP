---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: be91a56f93b787f5570139768d96eb4f7fe9ac02
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799503"
---
# <a name="iolkenum"></a><span data-ttu-id="3e0f6-102">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="3e0f6-102">IOlkEnum</span></span>

<span data-ttu-id="3e0f6-103">[IUnknown](http://msdn.microsoft.com/library/com.iunknown%28Office.15%29.aspx)オブジェクトとしてアカウントの列挙をサポートします。</span><span class="sxs-lookup"><span data-stu-id="3e0f6-103">Supports enumerating accounts as [IUnknown](http://msdn.microsoft.com/library/com.iunknown%28Office.15%29.aspx) objects.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="3e0f6-104">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="3e0f6-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3e0f6-105">継承します。</span><span class="sxs-lookup"><span data-stu-id="3e0f6-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="3e0f6-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="3e0f6-106">IUnknown</span></span>](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="3e0f6-107">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="3e0f6-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="3e0f6-108">Outlook</span><span class="sxs-lookup"><span data-stu-id="3e0f6-108">Outlook</span></span>  <br/> |
|<span data-ttu-id="3e0f6-109">提供元:</span><span class="sxs-lookup"><span data-stu-id="3e0f6-109">Provided by:</span></span>  <br/> |[<span data-ttu-id="3e0f6-110">IOlkAccountManager::EnumerateAccounts</span><span class="sxs-lookup"><span data-stu-id="3e0f6-110">IOlkAccountManager::EnumerateAccounts</span></span>](iolkaccountmanager-enumerateaccounts.md) <br/> |
|<span data-ttu-id="3e0f6-111">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3e0f6-111">Called by:</span></span>  <br/> |<span data-ttu-id="3e0f6-112">クライアント</span><span class="sxs-lookup"><span data-stu-id="3e0f6-112">Client</span></span>  <br/> |
|<span data-ttu-id="3e0f6-113">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="3e0f6-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3e0f6-114">IID_IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="3e0f6-114">IID_IOlkEnum</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3e0f6-115">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="3e0f6-115">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="3e0f6-116">GetCount</span><span class="sxs-lookup"><span data-stu-id="3e0f6-116">GetCount</span></span>](iolkenum-getcount.md) <br/> |<span data-ttu-id="3e0f6-117">列挙子では、アカウントの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="3e0f6-117">Gets the number of accounts in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="3e0f6-118">Reset</span><span class="sxs-lookup"><span data-stu-id="3e0f6-118">Reset</span></span>](iolkenum-reset.md) <br/> |<span data-ttu-id="3e0f6-119">先頭に列挙子をリセットします。</span><span class="sxs-lookup"><span data-stu-id="3e0f6-119">Resets the enumerator to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="3e0f6-120">GetNext</span><span class="sxs-lookup"><span data-stu-id="3e0f6-120">GetNext</span></span>](iolkenum-getnext.md) <br/> |<span data-ttu-id="3e0f6-121">列挙子では、次のアカウントを取得します。</span><span class="sxs-lookup"><span data-stu-id="3e0f6-121">Gets the next account in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="3e0f6-122">スキップ</span><span class="sxs-lookup"><span data-stu-id="3e0f6-122">Skip</span></span>](iolkenum-skip.md) <br/> |<span data-ttu-id="3e0f6-123">列挙子内のアカウントの指定した数をスキップします。</span><span class="sxs-lookup"><span data-stu-id="3e0f6-123">Skips a specified number of accounts in the enumerator.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3e0f6-124">備考</span><span class="sxs-lookup"><span data-stu-id="3e0f6-124">Remarks</span></span>

<span data-ttu-id="3e0f6-125">アカウントの列挙子を取得するときは、 **IOlkAccountManager::EnumerateAccounts**によってこのインターフェイスが返されます。</span><span class="sxs-lookup"><span data-stu-id="3e0f6-125">This interface is returned by **IOlkAccountManager::EnumerateAccounts** when obtaining an enumerator of accounts.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3e0f6-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="3e0f6-126">See also</span></span>

- [<span data-ttu-id="3e0f6-127">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="3e0f6-127">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="3e0f6-128">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="3e0f6-128">Constants (Account management API)</span></span>](constants-account-management-api.md)

