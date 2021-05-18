---
title: IOlkAccountManagerEnumerateAccounts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbb8342b-e4e0-f89d-3e14-b4c7049095ef
description: 特定のカテゴリまたは種類のアカウントの列挙子を取得します。
ms.openlocfilehash: d0d383dee0e76dd6310d01bd1482e307c2374856
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423049"
---
# <a name="iolkaccountmanagerenumerateaccounts"></a><span data-ttu-id="481be-103">IOlkAccountManager::EnumerateAccounts</span><span class="sxs-lookup"><span data-stu-id="481be-103">IOlkAccountManager::EnumerateAccounts</span></span>

<span data-ttu-id="481be-104">特定のカテゴリまたは種類のアカウントの列挙子を取得します。</span><span class="sxs-lookup"><span data-stu-id="481be-104">Gets an enumerator for the accounts of the specific category or type.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="481be-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="481be-105">Quick info</span></span>

<span data-ttu-id="481be-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="481be-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::EnumerateAccounts (  
    const CLSID *pclsidCategory, 
    const CLSID *pclsidType, 
    DWORD dwFlags, 
    IOlkEnum **ppEnum 
);

```

## <a name="parameters"></a><span data-ttu-id="481be-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="481be-107">Parameters</span></span>

<span data-ttu-id="481be-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="481be-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="481be-p101">[in]列挙するカテゴリのクラスの id。値は、次のいずれかする必要があります。</span><span class="sxs-lookup"><span data-stu-id="481be-p101">[in] The class identifier of the category to enumerate. The value must be one of the following:</span></span>
    
   - <span data-ttu-id="481be-111">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="481be-111">CLSID_OlkMail</span></span> 
    
   -  <span data-ttu-id="481be-112">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="481be-112">CLSID_OlkAddressBook</span></span> 
    
   - <span data-ttu-id="481be-113">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="481be-113">CLSID_OlkStore</span></span> 
    
<span data-ttu-id="481be-114">_pclsidType_</span><span class="sxs-lookup"><span data-stu-id="481be-114">_pclsidType_</span></span>
  
> <span data-ttu-id="481be-p102">[in]アカウントの種類を列挙するのクラス識別子。値は、次のいずれかする必要があります。</span><span class="sxs-lookup"><span data-stu-id="481be-p102">[in] The class identifier of the account type to enumerate. The value must be one of the following:</span></span>
    
   - <span data-ttu-id="481be-117">CLSID_OlkPOP3Account</span><span class="sxs-lookup"><span data-stu-id="481be-117">CLSID_OlkPOP3Account</span></span>
    
   - <span data-ttu-id="481be-118">CLSID_OlkIMAP4Account</span><span class="sxs-lookup"><span data-stu-id="481be-118">CLSID_OlkIMAP4Account</span></span>
    
   - <span data-ttu-id="481be-119">CLSID_OlkMAPIAccount</span><span class="sxs-lookup"><span data-stu-id="481be-119">CLSID_OlkMAPIAccount</span></span>
    
   - <span data-ttu-id="481be-120">CLSID_OlkHotmailAccount</span><span class="sxs-lookup"><span data-stu-id="481be-120">CLSID_OlkHotmailAccount</span></span>
    
   - <span data-ttu-id="481be-121">CLSID_OlkLDAPAccount</span><span class="sxs-lookup"><span data-stu-id="481be-121">CLSID_OlkLDAPAccount</span></span>
    
<span data-ttu-id="481be-122">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="481be-122">_dwFlags_</span></span>
  
> <span data-ttu-id="481be-p103">[in]動作を変更するフラグです。サポートされている唯一の値は OLK_ACCOUNT_NO_FLAGS です。</span><span class="sxs-lookup"><span data-stu-id="481be-p103">[in] Flags to modify behavior. The only supported value is OLK_ACCOUNT_NO_FLAGS.</span></span>
    
<span data-ttu-id="481be-125">_ppEnum_</span><span class="sxs-lookup"><span data-stu-id="481be-125">_ppEnum_</span></span>
  
> <span data-ttu-id="481be-126">[out] An enumerator that supports the [IOlkEnum](iolkenum.md) interface.</span><span class="sxs-lookup"><span data-stu-id="481be-126">[out] An enumerator that supports the [IOlkEnum](iolkenum.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="481be-127">戻り値</span><span class="sxs-lookup"><span data-stu-id="481be-127">Return values</span></span>

|<span data-ttu-id="481be-128">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="481be-128">**HRESULT**</span></span>|<span data-ttu-id="481be-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="481be-129">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="481be-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="481be-130">S_OK</span></span>  <br/> |<span data-ttu-id="481be-131">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="481be-131">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="481be-132">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="481be-132">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="481be-133">アカウント マネージャーが使用するために初期化されていません。</span><span class="sxs-lookup"><span data-stu-id="481be-133">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="481be-134">注釈</span><span class="sxs-lookup"><span data-stu-id="481be-134">Remarks</span></span>

<span data-ttu-id="481be-p104">NULL を指定するカテゴリの指定した型のすべてのアカウントの列挙子を返します。同様に、NULL の種類を指定すると、指定したカテゴリのすべてのアカウントの列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="481be-p104">Specifying NULL for category returns an enumerator of all accounts of the specified type. Similarly, specifying NULL for type returns an enumerator of all accounts of the specified category.</span></span>
  
 <span data-ttu-id="481be-137">**IOlkAccountManager::EnumerateAccounts** は、Exchange アカウントのアドレス帳カテゴリをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="481be-137">**IOlkAccountManager::EnumerateAccounts** does not support the address book category for an Exchange account.</span></span> <span data-ttu-id="481be-138">アカウントが Exchange アカウント *(pclsidType* は **CLSID_OlkMAPIAccount)** で、アドレス帳を実装するアカウントを列挙しようとしている場合 *(prgclsidCategory* は CLSID_OlkAddressBook)、IOlkAccountManager::EnumerateAccounts を呼び出した場合、アカウント列挙子 *ppEnum* の Exchange アカウントは返されません。  </span><span class="sxs-lookup"><span data-stu-id="481be-138">If the account is an Exchange account (*pclsidType*  is **CLSID_OlkMAPIAccount** ), and you are trying to enumerate accounts that implement the address book (*prgclsidCategory*  is **CLSID_OlkAddressBook** ), calling **IOlkAccountManager::EnumerateAccounts** will not return the Exchange account in the accounts enumerator  *ppEnum*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="481be-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="481be-139">See also</span></span>

- [<span data-ttu-id="481be-140">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="481be-140">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="481be-141">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="481be-141">IOlkEnum</span></span>](iolkenum.md)

