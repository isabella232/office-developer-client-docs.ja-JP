---
title: IOlkAccountManagerDisplayAccountList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a637dcab-81e0-4195-a1d5-61d9957fcf10
description: アカウントの設定または新しいアカウントの追加] ダイアログ ボックスが表示されます。
ms.openlocfilehash: 3c7c433eb4d8f316d32b6cd12bbbbb0e1a1cee43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799475"
---
# <a name="iolkaccountmanagerdisplayaccountlist"></a><span data-ttu-id="62bfd-103">IOlkAccountManager::DisplayAccountList</span><span class="sxs-lookup"><span data-stu-id="62bfd-103">IOlkAccountManager::DisplayAccountList</span></span>

<span data-ttu-id="62bfd-104">**アカウントの設定**または**新しいアカウントの追加**] ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="62bfd-104">Displays either the **Account Settings** or **Add New Account** dialog box.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="62bfd-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="62bfd-105">Quick info</span></span>

<span data-ttu-id="62bfd-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="62bfd-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::DisplayAccountList ( 
    HWND hwnd,
    DWORD dwFlags,
    LPCWSTR wszTitle,
    DWORD cCategories,
    const CLSID * rgclsidCategories,
    const CLSID * pclsidType
);

```

## <a name="parameters"></a><span data-ttu-id="62bfd-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="62bfd-107">Parameters</span></span>

<span data-ttu-id="62bfd-108">_hwnd_</span><span class="sxs-lookup"><span data-stu-id="62bfd-108">_hwnd_</span></span>
  
> <span data-ttu-id="62bfd-109">[in]表示されたダイアログ ボックスはモーダル ウィンドウへのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="62bfd-109">[in] The handle to the window to which the displayed dialog box is modal.</span></span> <span data-ttu-id="62bfd-110">0 にすることがあります。</span><span class="sxs-lookup"><span data-stu-id="62bfd-110">May be zero.</span></span>
    
<span data-ttu-id="62bfd-111">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="62bfd-111">_dwFlags_</span></span>
  
> <span data-ttu-id="62bfd-112">[in]表示の動作を変更するフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="62bfd-112">[in] Flags to modify the behavior of the display.</span></span> 
    
   - <span data-ttu-id="62bfd-113">**ACCTUI_NO_WARNING**-こと変更は有効になりませんが、Outlook を再起動するまで、警告は表示されません。</span><span class="sxs-lookup"><span data-stu-id="62bfd-113">**ACCTUI_NO_WARNING**—Do not display the warning that changes will not take effect until Outlook is restarted.</span></span> <span data-ttu-id="62bfd-114">アプリケーションが Outlook.exe でインプロセスで実行中である場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="62bfd-114">Applies only if the application is running in-process with Outlook.exe.</span></span>
    
   - <span data-ttu-id="62bfd-115">**ACCTUI_SHOW_DATA_TAB**: [**データ**] タブで、[**アカウント設定**] ダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="62bfd-115">**ACCTUI_SHOW_DATA_TAB**—Show the **Account Settings** dialog box with the **Data** tab selected.</span></span> <span data-ttu-id="62bfd-116">**ACCTUI_SHOW_ACCTWIZARD**が設定されていない場合にのみ有効にします。</span><span class="sxs-lookup"><span data-stu-id="62bfd-116">Valid only if **ACCTUI_SHOW_ACCTWIZARD** is not set.</span></span> 
    
   - <span data-ttu-id="62bfd-117">**ACCTUI_SHOW_ACCTWIZARD**:**新しいアカウントの追加**] ダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="62bfd-117">**ACCTUI_SHOW_ACCTWIZARD**—Display the **Add New Account** dialog box.</span></span> 
    
<span data-ttu-id="62bfd-118">_wszTitle_</span><span class="sxs-lookup"><span data-stu-id="62bfd-118">_wszTitle_</span></span>
  
> <span data-ttu-id="62bfd-119">[in]このパラメーターは、実行されていないと、NULL にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="62bfd-119">[in] This parameter is not used and should be NULL.</span></span>
    
<span data-ttu-id="62bfd-120">_cCategories_</span><span class="sxs-lookup"><span data-stu-id="62bfd-120">_cCategories_</span></span>
  
> <span data-ttu-id="62bfd-121">[in]このパラメーターは、実行されていないと、NULL にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="62bfd-121">[in] This parameter is not used and must be NULL.</span></span> 
    
<span data-ttu-id="62bfd-122">_rgclsidCategories_</span><span class="sxs-lookup"><span data-stu-id="62bfd-122">_rgclsidCategories_</span></span>
  
> <span data-ttu-id="62bfd-123">[in]このパラメーターは、実行されていないと、NULL にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="62bfd-123">[in] This parameter is not used and must be NULL.</span></span>
    
<span data-ttu-id="62bfd-124">_pclsidType_</span><span class="sxs-lookup"><span data-stu-id="62bfd-124">_pclsidType_</span></span>
  
> <span data-ttu-id="62bfd-125">[in]このパラメーターは、実行されていないと、NULL にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="62bfd-125">[in] This parameter is not used and must be NULL.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="62bfd-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="62bfd-126">Return values</span></span>

|<span data-ttu-id="62bfd-127">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="62bfd-127">**HRESULT**</span></span>|<span data-ttu-id="62bfd-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="62bfd-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="62bfd-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="62bfd-129">S_OK</span></span>  <br/> |<span data-ttu-id="62bfd-130">呼び出しが正常になされました。</span><span class="sxs-lookup"><span data-stu-id="62bfd-130">The call was successful.</span></span>  <br/> |
|<span data-ttu-id="62bfd-131">E_ACCT_UI_BUSY</span><span class="sxs-lookup"><span data-stu-id="62bfd-131">E_ACCT_UI_BUSY</span></span>  <br/> |<span data-ttu-id="62bfd-132">ダイアログ ボックスを作成できませんでした。</span><span class="sxs-lookup"><span data-stu-id="62bfd-132">The dialog box could not be created.</span></span>  <br/> |
|<span data-ttu-id="62bfd-133">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="62bfd-133">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="62bfd-134">アカウント マネージャーが使用するために初期化されていません。</span><span class="sxs-lookup"><span data-stu-id="62bfd-134">The account manager has not been initialized for use.</span></span>  <br/> |
|<span data-ttu-id="62bfd-135">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="62bfd-135">MAPI_E_CALL_FAILED</span></span>  <br/> |<span data-ttu-id="62bfd-136">**新しいアカウントの追加**] ダイアログ ボックスには、エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="62bfd-136">The **Add New Account** dialog box returned an error.</span></span>  <br/> |
|<span data-ttu-id="62bfd-137">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="62bfd-137">MAPI_E_INVALID_PARAMETER</span></span>  <br/> |<span data-ttu-id="62bfd-138">_CCategories_、 _rgclsidCategories_、または_pclsidType_パラメーターは、NULL 以外です。</span><span class="sxs-lookup"><span data-stu-id="62bfd-138">The  _cCategories_,  _rgclsidCategories_, or  _pclsidType_ parameter is non-NULL.</span></span>  <br/> |
|<span data-ttu-id="62bfd-139">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="62bfd-139">MAPI_E_USER_CANCEL</span></span>  <br/> |<span data-ttu-id="62bfd-140">**アカウント設定**] ダイアログ ボックスには、エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="62bfd-140">The **Account Settings** dialog box returned an error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62bfd-141">注釈</span><span class="sxs-lookup"><span data-stu-id="62bfd-141">Remarks</span></span>

<span data-ttu-id="62bfd-142">_CCategories_、 _rgclsidCategories_、および_pclsidType_パラメーターは、この時点では使用されず、NULL にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="62bfd-142">The  _cCategories_,  _rgclsidCategories_, and  _pclsidType_ parameters are not used at this time and must be NULL.</span></span>  <span data-ttu-id="62bfd-143">_wszTitle_は、使用しないと、NULL 必要があります。</span><span class="sxs-lookup"><span data-stu-id="62bfd-143">_wszTitle_ is not used and should also be NULL.</span></span> 
  

