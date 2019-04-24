---
title: IOlkAccountGetAccountInfo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 97f08cde-d6e4-8935-1758-4018a3baf682
description: 指定されたアカウントの種類とカテゴリ情報を取得します。
ms.openlocfilehash: 88021537cc7ff4c55759081e6f3619c2a9f10ea3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318187"
---
# <a name="iolkaccountgetaccountinfo"></a><span data-ttu-id="5f592-103">IOlkAccount::GetAccountInfo</span><span class="sxs-lookup"><span data-stu-id="5f592-103">IOlkAccount::GetAccountInfo</span></span>

<span data-ttu-id="5f592-104">指定されたアカウントの種類とカテゴリ情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="5f592-104">Gets the type and categories information for the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5f592-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="5f592-105">Quick info</span></span>

<span data-ttu-id="5f592-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5f592-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::GetAccountInfo(  
    CLSID *pclsidType, 
    DWORD *pcCategories, 
    CLSID **prgclsidCategory 
);

```

## <a name="parameters"></a><span data-ttu-id="5f592-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5f592-107">Parameters</span></span>

<span data-ttu-id="5f592-108">_pclsidtype_</span><span class="sxs-lookup"><span data-stu-id="5f592-108">_pclsidType_</span></span>
  
> <span data-ttu-id="5f592-109">読み上げアカウントの種類のクラス識別子。</span><span class="sxs-lookup"><span data-stu-id="5f592-109">[out] The class identifier for the account type.</span></span> <span data-ttu-id="5f592-110">値は、次のいずれかする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f592-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="5f592-111">CLSID_OlkPOP3Account</span><span class="sxs-lookup"><span data-stu-id="5f592-111">CLSID_OlkPOP3Account</span></span> 
    
   - <span data-ttu-id="5f592-112">CLSID_OlkIMAP4Account</span><span class="sxs-lookup"><span data-stu-id="5f592-112">CLSID_OlkIMAP4Account</span></span> 
    
   - <span data-ttu-id="5f592-113">CLSID_OlkMAPIAccount</span><span class="sxs-lookup"><span data-stu-id="5f592-113">CLSID_OlkMAPIAccount</span></span> 
    
   - <span data-ttu-id="5f592-114">CLSID_OlkHotmailAccount</span><span class="sxs-lookup"><span data-stu-id="5f592-114">CLSID_OlkHotmailAccount</span></span> 
    
   - <span data-ttu-id="5f592-115">CLSID_OlkLDAPAccount</span><span class="sxs-lookup"><span data-stu-id="5f592-115">CLSID_OlkLDAPAccount</span></span>
    
<span data-ttu-id="5f592-116">_pccategories_</span><span class="sxs-lookup"><span data-stu-id="5f592-116">_pcCategories_</span></span>
  
> <span data-ttu-id="5f592-117">読み上げ_prgclsidCategory_の分類項目数を指定します。</span><span class="sxs-lookup"><span data-stu-id="5f592-117">[out] The number of categories in  _prgclsidCategory_.</span></span>
    
<span data-ttu-id="5f592-118">_prgclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="5f592-118">_prgclsidCategory_</span></span>
  
> <span data-ttu-id="5f592-119">読み上げこのアカウントが関連付けられているカテゴリの配列。</span><span class="sxs-lookup"><span data-stu-id="5f592-119">[out] An array of categories that this account is associated with.</span></span> <span data-ttu-id="5f592-120">配列のサイズは、 _pccategories_です。</span><span class="sxs-lookup"><span data-stu-id="5f592-120">The array is of size \* _pcCategories_.</span></span> <span data-ttu-id="5f592-121">配列内の各カテゴリの値は、次のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f592-121">The value of each category in the array must be one of the following:</span></span>
    
   - <span data-ttu-id="5f592-122">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="5f592-122">CLSID_OlkMail</span></span>
    
   - <span data-ttu-id="5f592-123">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="5f592-123">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="5f592-124">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="5f592-124">CLSID_OlkStore</span></span>
    
## <a name="return-values"></a><span data-ttu-id="5f592-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="5f592-125">Return values</span></span>

<span data-ttu-id="5f592-126">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="5f592-126">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5f592-127">解説</span><span class="sxs-lookup"><span data-stu-id="5f592-127">Remarks</span></span>

<span data-ttu-id="5f592-128">このメソッドが返された後、 [IOlkAccount:: FreeMemory](iolkaccount-freememory.md)を使用して*prgclsidCategory*を解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f592-128">After this method returns, you must free  *prgclsidCategory*  by using [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span></span>
  
<span data-ttu-id="5f592-129">**IOlkAccount:: getaccountinfo**は、Exchange アカウントのアドレス帳カテゴリをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="5f592-129">**IOlkAccount::GetAccountInfo** does not support the address book category for an Exchange account.</span></span> <span data-ttu-id="5f592-130">アカウントが Exchange アカウント (*pclsidtype*が**CLSID_OlkMAPIAccount** ) で、そのアカウントがアドレス帳を実装している場合、 **IOlkAccount:: getaccountinfo**を呼び出しても、 **CLSID_OlkAddressBook**はの*カテゴリとして返されません。prgclsidCategory* 。</span><span class="sxs-lookup"><span data-stu-id="5f592-130">If the account is an Exchange account (*pclsidType*  is **CLSID_OlkMAPIAccount** ), and the account implements the address book, calling **IOlkAccount::GetAccountInfo** will not return **CLSID_OlkAddressBook** as a category in  *prgclsidCategory*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5f592-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="5f592-131">See also</span></span>

- [<span data-ttu-id="5f592-132">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="5f592-132">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="5f592-133">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="5f592-133">IOlkAccount::FreeMemory</span></span>](iolkaccount-freememory.md)

