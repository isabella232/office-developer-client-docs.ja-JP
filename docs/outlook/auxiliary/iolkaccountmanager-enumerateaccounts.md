---
title: IOlkAccountManagerEnumerateAccounts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbb8342b-e4e0-f89d-3e14-b4c7049095ef
description: 特定のカテゴリまたは種類のアカウントの列挙子を取得します。
ms.openlocfilehash: f9b332c0bbc90b1a8f5f944492448055f23c0668
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799471"
---
# <a name="iolkaccountmanagerenumerateaccounts"></a><span data-ttu-id="30a61-103">IOlkAccountManager::EnumerateAccounts</span><span class="sxs-lookup"><span data-stu-id="30a61-103">IOlkAccountManager::EnumerateAccounts</span></span>

<span data-ttu-id="30a61-104">特定のカテゴリまたは種類のアカウントの列挙子を取得します。</span><span class="sxs-lookup"><span data-stu-id="30a61-104">Gets an enumerator for the accounts of the specific category or type.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="30a61-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="30a61-105">Quick info</span></span>

<span data-ttu-id="30a61-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="30a61-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::EnumerateAccounts (  
    const CLSID *pclsidCategory, 
    const CLSID *pclsidType, 
    DWORD dwFlags, 
    IOlkEnum **ppEnum 
);

```

## <a name="parameters"></a><span data-ttu-id="30a61-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="30a61-107">Parameters</span></span>

<span data-ttu-id="30a61-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="30a61-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="30a61-p101">[in]列挙するカテゴリのクラスの id。値は、次のいずれかする必要があります。</span><span class="sxs-lookup"><span data-stu-id="30a61-p101">[in] The class identifier of the category to enumerate. The value must be one of the following:</span></span>
    
   - <span data-ttu-id="30a61-111">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="30a61-111">CLSID_OlkMail</span></span> 
    
   -  <span data-ttu-id="30a61-112">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="30a61-112">CLSID_OlkAddressBook</span></span> 
    
   - <span data-ttu-id="30a61-113">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="30a61-113">CLSID_OlkStore</span></span> 
    
<span data-ttu-id="30a61-114">_pclsidType_</span><span class="sxs-lookup"><span data-stu-id="30a61-114">_pclsidType_</span></span>
  
> <span data-ttu-id="30a61-p102">[in]アカウントの種類を列挙するのクラス識別子。値は、次のいずれかする必要があります。</span><span class="sxs-lookup"><span data-stu-id="30a61-p102">[in] The class identifier of the account type to enumerate. The value must be one of the following:</span></span>
    
   - <span data-ttu-id="30a61-117">CLSID_OlkPOP3Account</span><span class="sxs-lookup"><span data-stu-id="30a61-117">CLSID_OlkPOP3Account</span></span>
    
   - <span data-ttu-id="30a61-118">CLSID_OlkIMAP4Account</span><span class="sxs-lookup"><span data-stu-id="30a61-118">CLSID_OlkIMAP4Account</span></span>
    
   - <span data-ttu-id="30a61-119">CLSID_OlkMAPIAccount</span><span class="sxs-lookup"><span data-stu-id="30a61-119">CLSID_OlkMAPIAccount</span></span>
    
   - <span data-ttu-id="30a61-120">CLSID_OlkHotmailAccount</span><span class="sxs-lookup"><span data-stu-id="30a61-120">CLSID_OlkHotmailAccount</span></span>
    
   - <span data-ttu-id="30a61-121">CLSID_OlkLDAPAccount</span><span class="sxs-lookup"><span data-stu-id="30a61-121">CLSID_OlkLDAPAccount</span></span>
    
<span data-ttu-id="30a61-122">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="30a61-122">_dwFlags_</span></span>
  
> <span data-ttu-id="30a61-p103">[in]動作を変更するフラグです。サポートされている唯一の値は OLK_ACCOUNT_NO_FLAGS です。</span><span class="sxs-lookup"><span data-stu-id="30a61-p103">[in] Flags to modify behavior. The only supported value is OLK_ACCOUNT_NO_FLAGS.</span></span>
    
<span data-ttu-id="30a61-125">_ppEnum_</span><span class="sxs-lookup"><span data-stu-id="30a61-125">_ppEnum_</span></span>
  
> <span data-ttu-id="30a61-126">[out] An enumerator that supports the [IOlkEnum](iolkenum.md) interface.</span><span class="sxs-lookup"><span data-stu-id="30a61-126">[out] An enumerator that supports the [IOlkEnum](iolkenum.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="30a61-127">戻り値</span><span class="sxs-lookup"><span data-stu-id="30a61-127">Return values</span></span>

|<span data-ttu-id="30a61-128">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="30a61-128">**HRESULT**</span></span>|<span data-ttu-id="30a61-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="30a61-129">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="30a61-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="30a61-130">S_OK</span></span>  <br/> |<span data-ttu-id="30a61-131">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="30a61-131">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="30a61-132">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="30a61-132">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="30a61-133">アカウント マネージャーが使用するために初期化されていません。</span><span class="sxs-lookup"><span data-stu-id="30a61-133">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30a61-134">注釈</span><span class="sxs-lookup"><span data-stu-id="30a61-134">Remarks</span></span>

<span data-ttu-id="30a61-p104">NULL を指定するカテゴリの指定した型のすべてのアカウントの列挙子を返します。同様に、NULL の種類を指定すると、指定したカテゴリのすべてのアカウントの列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="30a61-p104">Specifying NULL for category returns an enumerator of all accounts of the specified type. Similarly, specifying NULL for type returns an enumerator of all accounts of the specified category.</span></span>
  
 <span data-ttu-id="30a61-137">**IOlkAccountManager::EnumerateAccounts** は、Exchange アカウントのアドレス帳カテゴリをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="30a61-137">**IOlkAccountManager::EnumerateAccounts** does not support the address book category for an Exchange account.</span></span> <span data-ttu-id="30a61-138">アカウントが Exchange アカウントの場合 (*pclsidType*は**CLSID_OlkMAPIAccount** )、アドレス帳を実装しているアカウントを列挙しようとして (*prgclsidCategory*は**CLSID_OlkAddressBook** )、**を呼び出すIOlkAccountManager::EnumerateAccounts**アカウントの列挙子の*ppEnum*で、Exchange アカウントが返されません。</span><span class="sxs-lookup"><span data-stu-id="30a61-138">If the account is an Exchange account (*pclsidType*  is **CLSID_OlkMAPIAccount** ), and you are trying to enumerate accounts that implement the address book (*prgclsidCategory*  is **CLSID_OlkAddressBook** ), calling **IOlkAccountManager::EnumerateAccounts** will not return the Exchange account in the accounts enumerator  *ppEnum*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="30a61-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="30a61-139">See also</span></span>

- [<span data-ttu-id="30a61-140">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="30a61-140">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="30a61-141">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="30a61-141">IOlkEnum</span></span>](iolkenum.md)

