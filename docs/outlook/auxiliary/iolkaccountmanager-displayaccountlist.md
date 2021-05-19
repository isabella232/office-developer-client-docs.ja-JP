---
title: IOlkAccountManagerDisplayAccountList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a637dcab-81e0-4195-a1d5-61d9957fcf10
description: '[アカウント の追加] ダイアログ 設定 [新しいアカウントの追加] ダイアログ ボックスが表示されます。'
ms.openlocfilehash: ecf5242fa4f224516e12e667ab66fd0adfe4a25d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415034"
---
# <a name="iolkaccountmanagerdisplayaccountlist"></a><span data-ttu-id="7e185-103">IOlkAccountManager::DisplayAccountList</span><span class="sxs-lookup"><span data-stu-id="7e185-103">IOlkAccountManager::DisplayAccountList</span></span>

<span data-ttu-id="7e185-104">[アカウント の追加 **] ダイアログ 設定**[新しいアカウントの **追加] ダイアログ ボックスを** 表示します。</span><span class="sxs-lookup"><span data-stu-id="7e185-104">Displays either the **Account Settings** or **Add New Account** dialog box.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="7e185-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="7e185-105">Quick info</span></span>

<span data-ttu-id="7e185-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="7e185-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="7e185-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7e185-107">Parameters</span></span>

<span data-ttu-id="7e185-108">_hwnd_</span><span class="sxs-lookup"><span data-stu-id="7e185-108">_hwnd_</span></span>
  
> <span data-ttu-id="7e185-109">[in]表示されるダイアログ ボックスがモーダルであるウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="7e185-109">[in] The handle to the window to which the displayed dialog box is modal.</span></span> <span data-ttu-id="7e185-110">ゼロの場合があります。</span><span class="sxs-lookup"><span data-stu-id="7e185-110">May be zero.</span></span>
    
<span data-ttu-id="7e185-111">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="7e185-111">_dwFlags_</span></span>
  
> <span data-ttu-id="7e185-112">[in]表示の動作を変更するフラグ。</span><span class="sxs-lookup"><span data-stu-id="7e185-112">[in] Flags to modify the behavior of the display.</span></span> 
    
   - <span data-ttu-id="7e185-113">**ACCTUI_NO_WARNING**—再起動するまで変更が有効になOutlook表示しません。</span><span class="sxs-lookup"><span data-stu-id="7e185-113">**ACCTUI_NO_WARNING**—Do not display the warning that changes will not take effect until Outlook is restarted.</span></span> <span data-ttu-id="7e185-114">アプリケーションがプロセス内で実行中の場合にのみ適用Outlook.exe。</span><span class="sxs-lookup"><span data-stu-id="7e185-114">Applies only if the application is running in-process with Outlook.exe.</span></span>
    
   - <span data-ttu-id="7e185-115">**ACCTUI_SHOW_DATA_TAB**— [データ] タブ **を選択設定[** アカウント のアカウント]**ダイアログ ボックス** を表示します。</span><span class="sxs-lookup"><span data-stu-id="7e185-115">**ACCTUI_SHOW_DATA_TAB**—Show the **Account Settings** dialog box with the **Data** tab selected.</span></span> <span data-ttu-id="7e185-116">この値は **、ACCTUI_SHOW_ACCTWIZARD** 設定されていない場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="7e185-116">Valid only if **ACCTUI_SHOW_ACCTWIZARD** is not set.</span></span> 
    
   - <span data-ttu-id="7e185-117">**ACCTUI_SHOW_ACCTWIZARD**—[新しいアカウントの **追加] ダイアログ ボックスを** 表示します。</span><span class="sxs-lookup"><span data-stu-id="7e185-117">**ACCTUI_SHOW_ACCTWIZARD**—Display the **Add New Account** dialog box.</span></span> 
    
<span data-ttu-id="7e185-118">_wszTitle_</span><span class="sxs-lookup"><span data-stu-id="7e185-118">_wszTitle_</span></span>
  
> <span data-ttu-id="7e185-119">[in]このパラメーターは使用されないので、NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e185-119">[in] This parameter is not used and should be NULL.</span></span>
    
<span data-ttu-id="7e185-120">_cCategories_</span><span class="sxs-lookup"><span data-stu-id="7e185-120">_cCategories_</span></span>
  
> <span data-ttu-id="7e185-121">[in]このパラメーターは使用されないので、NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e185-121">[in] This parameter is not used and must be NULL.</span></span> 
    
<span data-ttu-id="7e185-122">_rgclsidCategories_</span><span class="sxs-lookup"><span data-stu-id="7e185-122">_rgclsidCategories_</span></span>
  
> <span data-ttu-id="7e185-123">[in]このパラメーターは使用されないので、NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e185-123">[in] This parameter is not used and must be NULL.</span></span>
    
<span data-ttu-id="7e185-124">_pclsidType_</span><span class="sxs-lookup"><span data-stu-id="7e185-124">_pclsidType_</span></span>
  
> <span data-ttu-id="7e185-125">[in]このパラメーターは使用されないので、NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e185-125">[in] This parameter is not used and must be NULL.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="7e185-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="7e185-126">Return values</span></span>

|<span data-ttu-id="7e185-127">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="7e185-127">**HRESULT**</span></span>|<span data-ttu-id="7e185-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="7e185-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7e185-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="7e185-129">S_OK</span></span>  <br/> |<span data-ttu-id="7e185-130">呼び出しが正常になされました。</span><span class="sxs-lookup"><span data-stu-id="7e185-130">The call was successful.</span></span>  <br/> |
|<span data-ttu-id="7e185-131">E_ACCT_UI_BUSY</span><span class="sxs-lookup"><span data-stu-id="7e185-131">E_ACCT_UI_BUSY</span></span>  <br/> |<span data-ttu-id="7e185-132">ダイアログ ボックスを作成できません。</span><span class="sxs-lookup"><span data-stu-id="7e185-132">The dialog box could not be created.</span></span>  <br/> |
|<span data-ttu-id="7e185-133">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="7e185-133">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="7e185-134">アカウント マネージャーが使用するために初期化されていません。</span><span class="sxs-lookup"><span data-stu-id="7e185-134">The account manager has not been initialized for use.</span></span>  <br/> |
|<span data-ttu-id="7e185-135">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="7e185-135">MAPI_E_CALL_FAILED</span></span>  <br/> |<span data-ttu-id="7e185-136">[ **新しいアカウントの追加]** ダイアログ ボックスにエラーが返されました。</span><span class="sxs-lookup"><span data-stu-id="7e185-136">The **Add New Account** dialog box returned an error.</span></span>  <br/> |
|<span data-ttu-id="7e185-137">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7e185-137">MAPI_E_INVALID_PARAMETER</span></span>  <br/> |<span data-ttu-id="7e185-138">_cCategories_ _、rgclsidCategories、__または pclsidType_ パラメーターは NULL 以外です。</span><span class="sxs-lookup"><span data-stu-id="7e185-138">The  _cCategories_,  _rgclsidCategories_, or  _pclsidType_ parameter is non-NULL.</span></span>  <br/> |
|<span data-ttu-id="7e185-139">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="7e185-139">MAPI_E_USER_CANCEL</span></span>  <br/> |<span data-ttu-id="7e185-140">[**アカウントの設定]** ダイアログ ボックスにエラーが返されました。</span><span class="sxs-lookup"><span data-stu-id="7e185-140">The **Account Settings** dialog box returned an error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7e185-141">注釈</span><span class="sxs-lookup"><span data-stu-id="7e185-141">Remarks</span></span>

<span data-ttu-id="7e185-142">_cCategories、rgclsidCategories、_ および _pclsidType_ パラメーターは現時点では使用されません。NULL である必要があります。 </span><span class="sxs-lookup"><span data-stu-id="7e185-142">The  _cCategories_,  _rgclsidCategories_, and  _pclsidType_ parameters are not used at this time and must be NULL.</span></span>  <span data-ttu-id="7e185-143">_wszTitle_ は使用されません。また、NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e185-143">_wszTitle_ is not used and should also be NULL.</span></span> 
  

