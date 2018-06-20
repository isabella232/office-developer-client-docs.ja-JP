---
title: IOlkAccountGetAccountInfo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 97f08cde-d6e4-8935-1758-4018a3baf682
description: 指定したアカウントの種類とカテゴリの情報を取得します。
ms.openlocfilehash: 85f27d1d5f47a372090b208821b52656a56559ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799399"
---
# <a name="iolkaccountgetaccountinfo"></a><span data-ttu-id="515bb-103">IOlkAccount::GetAccountInfo</span><span class="sxs-lookup"><span data-stu-id="515bb-103">IOlkAccount::GetAccountInfo</span></span>

<span data-ttu-id="515bb-104">指定したアカウントの種類とカテゴリの情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="515bb-104">Gets the type and categories information for the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="515bb-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="515bb-105">Quick info</span></span>

<span data-ttu-id="515bb-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="515bb-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::GetAccountInfo(  
    CLSID *pclsidType, 
    DWORD *pcCategories, 
    CLSID **prgclsidCategory 
);

```

## <a name="parameters"></a><span data-ttu-id="515bb-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="515bb-107">Parameters</span></span>

<span data-ttu-id="515bb-108">_pclsidType_</span><span class="sxs-lookup"><span data-stu-id="515bb-108">_pclsidType_</span></span>
  
> <span data-ttu-id="515bb-109">[out]アカウントの種類のクラスの識別子です。</span><span class="sxs-lookup"><span data-stu-id="515bb-109">[out] The class identifier for the account type.</span></span> <span data-ttu-id="515bb-110">値は、次のいずれかする必要があります。</span><span class="sxs-lookup"><span data-stu-id="515bb-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="515bb-111">CLSID_OlkPOP3Account</span><span class="sxs-lookup"><span data-stu-id="515bb-111">CLSID_OlkPOP3Account</span></span> 
    
   - <span data-ttu-id="515bb-112">CLSID_OlkIMAP4Account</span><span class="sxs-lookup"><span data-stu-id="515bb-112">CLSID_OlkIMAP4Account</span></span> 
    
   - <span data-ttu-id="515bb-113">CLSID_OlkMAPIAccount</span><span class="sxs-lookup"><span data-stu-id="515bb-113">CLSID_OlkMAPIAccount</span></span> 
    
   - <span data-ttu-id="515bb-114">CLSID_OlkHotmailAccount</span><span class="sxs-lookup"><span data-stu-id="515bb-114">CLSID_OlkHotmailAccount</span></span> 
    
   - <span data-ttu-id="515bb-115">CLSID_OlkLDAPAccount</span><span class="sxs-lookup"><span data-stu-id="515bb-115">CLSID_OlkLDAPAccount</span></span>
    
<span data-ttu-id="515bb-116">_pcCategories_</span><span class="sxs-lookup"><span data-stu-id="515bb-116">_pcCategories_</span></span>
  
> <span data-ttu-id="515bb-117">[out]_PrgclsidCategory_内のカテゴリの数です。</span><span class="sxs-lookup"><span data-stu-id="515bb-117">[out] The number of categories in  _prgclsidCategory_.</span></span>
    
<span data-ttu-id="515bb-118">_prgclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="515bb-118">_prgclsidCategory_</span></span>
  
> <span data-ttu-id="515bb-119">[out]このアカウントが関連付けられているカテゴリの配列。</span><span class="sxs-lookup"><span data-stu-id="515bb-119">[out] An array of categories that this account is associated with.</span></span> <span data-ttu-id="515bb-120">サイズの配列は、\* _pcCategories_。</span><span class="sxs-lookup"><span data-stu-id="515bb-120">The array is of size \* _pcCategories_.</span></span> <span data-ttu-id="515bb-121">配列内の各カテゴリの値は、次のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="515bb-121">The value of each category in the array must be one of the following:</span></span>
    
   - <span data-ttu-id="515bb-122">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="515bb-122">CLSID_OlkMail</span></span>
    
   - <span data-ttu-id="515bb-123">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="515bb-123">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="515bb-124">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="515bb-124">CLSID_OlkStore</span></span>
    
## <a name="return-values"></a><span data-ttu-id="515bb-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="515bb-125">Return values</span></span>

<span data-ttu-id="515bb-126">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="515bb-126">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="515bb-127">解釈</span><span class="sxs-lookup"><span data-stu-id="515bb-127">Remarks</span></span>

<span data-ttu-id="515bb-128">このメソッドから制御が戻った後、 [IOlkAccount::FreeMemory](iolkaccount-freememory.md)を使用して*prgclsidCategory*を解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="515bb-128">After this method returns, you must free  *prgclsidCategory*  by using [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span></span>
  
<span data-ttu-id="515bb-129">**IOlkAccount::GetAccountInfo**は、Exchange アカウントのアドレス帳の分類をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="515bb-129">**IOlkAccount::GetAccountInfo** does not support the address book category for an Exchange account.</span></span> <span data-ttu-id="515bb-130">アカウントが Exchange の場合、取引先企業 (*pclsidType* **CLSID_OlkMAPIAccount** )、およびアカウントは、アドレス帳を実装して、呼び出し元の**IOlkAccount::GetAccountInfo** *でカテゴリとして**CLSID_OlkAddressBook**が返されませんprgclsidCategory* 。</span><span class="sxs-lookup"><span data-stu-id="515bb-130">If the account is an Exchange account (*pclsidType*  is **CLSID_OlkMAPIAccount** ), and the account implements the address book, calling **IOlkAccount::GetAccountInfo** will not return **CLSID_OlkAddressBook** as a category in  *prgclsidCategory*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="515bb-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="515bb-131">See also</span></span>

- [<span data-ttu-id="515bb-132">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="515bb-132">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="515bb-133">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="515bb-133">IOlkAccount::FreeMemory</span></span>](iolkaccount-freememory.md)

