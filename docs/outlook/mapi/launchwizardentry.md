---
title: LAUNCHWIZARDENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LAUNCHWIZARDENTRY
api_type:
- COM
ms.assetid: 5778dffa-f01b-46b3-9c19-862793740918
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c1509918eb587c17deebf95317cf57b4ab19928a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270190"
---
# <a name="launchwizardentry"></a><span data-ttu-id="38328-103">LAUNCHWIZARDENTRY</span><span class="sxs-lookup"><span data-stu-id="38328-103">LAUNCHWIZARDENTRY</span></span>

  
  
<span data-ttu-id="38328-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38328-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38328-105">プロファイルに1つ以上のメッセージサービスを追加することを目的として、プロファイルウィザードアプリケーションを起動する関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="38328-105">Defines a function that starts the Profile Wizard application for the purpose of adding one or more message services to a profile.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="38328-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="38328-106">Header file:</span></span>  <br/> |<span data-ttu-id="38328-107">Mapiwz</span><span class="sxs-lookup"><span data-stu-id="38328-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="38328-108">定義された関数の実装:</span><span class="sxs-lookup"><span data-stu-id="38328-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="38328-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="38328-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="38328-110">によって呼び出された定義済み関数:</span><span class="sxs-lookup"><span data-stu-id="38328-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="38328-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="38328-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT LAUNCHWIZARDENTRY(
  HWND hParentWnd,
  ULONG ulFlags,
  LPCSTR FAR * lppszServiceNameToAdd,
  ULONG cbBufferMax,
  LPSTR lpszNewProfileName
);
```

## <a name="parameters"></a><span data-ttu-id="38328-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="38328-112">Parameters</span></span>

 <span data-ttu-id="38328-113">_hParentWnd_</span><span class="sxs-lookup"><span data-stu-id="38328-113">_hParentWnd_</span></span>
  
> <span data-ttu-id="38328-114">順番呼び出し元の親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="38328-114">[in] A handle to the caller's parent window.</span></span> <span data-ttu-id="38328-115">呼び出し元が親ウィンドウを持たない場合は、 _hParentWnd_パラメーターを NULL にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="38328-115">If the caller does not have a parent window, the  _hParentWnd_ parameter should be NULL.</span></span> 
    
 <span data-ttu-id="38328-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="38328-116">_ulFlags_</span></span>
  
> <span data-ttu-id="38328-117">順番プロファイルウィザードのオプションを示すフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="38328-117">[in] Bitmask of flags indicating options for the Profile Wizard.</span></span> <span data-ttu-id="38328-118">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="38328-118">The following flags can be set:</span></span>
    
<span data-ttu-id="38328-119">MAPI_PW_ADD_SERVICE_ONLY</span><span class="sxs-lookup"><span data-stu-id="38328-119">MAPI_PW_ADD_SERVICE_ONLY</span></span> 
  
> <span data-ttu-id="38328-120">プロファイルウィザードでは、 _lppszServiceNameToAdd_パラメーターを使用してメッセージサービスのみを追加し、メッセージサービスを選択するためのページを表示しないようにします。</span><span class="sxs-lookup"><span data-stu-id="38328-120">The Profile Wizard is to add only the message services listed through the  _lppszServiceNameToAdd_ parameter, and not display its page for selecting message services.</span></span> 
    
<span data-ttu-id="38328-121">MAPI_PW_FIRST_PROFILE</span><span class="sxs-lookup"><span data-stu-id="38328-121">MAPI_PW_FIRST_PROFILE</span></span> 
  
> <span data-ttu-id="38328-122">このワークステーションの最初のプロファイルが作成されます。</span><span class="sxs-lookup"><span data-stu-id="38328-122">The profile to be created is the first one for this workstation.</span></span> 
    
<span data-ttu-id="38328-123">MAPI_PW_HIDE_SERVICES_LIST</span><span class="sxs-lookup"><span data-stu-id="38328-123">MAPI_PW_HIDE_SERVICES_LIST</span></span> 
  
> <span data-ttu-id="38328-124">メッセージサービスを選択するためのプロファイルウィザードのページは表示されません。</span><span class="sxs-lookup"><span data-stu-id="38328-124">The Profile Wizard's page for selecting message services should not be displayed.</span></span> 
    
<span data-ttu-id="38328-125">MAPI_PW_LAUNCHED_BY_CONFIG</span><span class="sxs-lookup"><span data-stu-id="38328-125">MAPI_PW_LAUNCHED_BY_CONFIG</span></span> 
  
> <span data-ttu-id="38328-126">プロファイルウィザードは、コントロールパネル構成アプリケーションによって起動されました。</span><span class="sxs-lookup"><span data-stu-id="38328-126">The Profile Wizard was launched by the Control Panel configuration application.</span></span> 
    
<span data-ttu-id="38328-127">MAPI_PW_PROVIDER_UI_ONLY</span><span class="sxs-lookup"><span data-stu-id="38328-127">MAPI_PW_PROVIDER_UI_ONLY</span></span> 
  
> <span data-ttu-id="38328-128">サービスプロバイダーの [構成] ダイアログボックスだけが表示され、プロファイルウィザードのページは表示されません。</span><span class="sxs-lookup"><span data-stu-id="38328-128">Only the service providers's configuration dialog boxes should be displayed and the Profile Wizard's pages should not appear.</span></span> <span data-ttu-id="38328-129">このフラグは、MAPI_PW_ADD_SERVICE_ONLY フラグが設定されている場合にのみ設定できます。</span><span class="sxs-lookup"><span data-stu-id="38328-129">This flag can only be set if the MAPI_PW_ADD_SERVICE_ONLY flag is set.</span></span> 
    
 <span data-ttu-id="38328-130">_lppszServiceNameToAdd_</span><span class="sxs-lookup"><span data-stu-id="38328-130">_lppszServiceNameToAdd_</span></span>
  
> <span data-ttu-id="38328-131">順番プロファイルに追加するメッセージサービスの名前を含む文字列の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="38328-131">[in] Pointer to an array of strings that contains the names of the message services to be added to the profile.</span></span> <span data-ttu-id="38328-132">配列は NULL 値で終了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="38328-132">The array must terminate with a NULL value.</span></span> 
    
 <span data-ttu-id="38328-133">_cbbuffermax_</span><span class="sxs-lookup"><span data-stu-id="38328-133">_cbBufferMax_</span></span>
  
> <span data-ttu-id="38328-134">順番_lpsznewprofilename_パラメーターによって示されるバッファーのサイズ。</span><span class="sxs-lookup"><span data-stu-id="38328-134">[in] Size of the buffer pointed to by the  _lpszNewProfileName_ parameter.</span></span> 
    
 <span data-ttu-id="38328-135">_lpsznewprofilename_</span><span class="sxs-lookup"><span data-stu-id="38328-135">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="38328-136">読み上げ**launchwizardentry**に基づく関数が、作成されたプロファイルの名前を返す文字列バッファーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="38328-136">[out] Pointer to a string buffer where the function based on **LAUNCHWIZARDENTRY** returns the name of the created profile.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="38328-137">戻り値</span><span class="sxs-lookup"><span data-stu-id="38328-137">Return value</span></span>

<span data-ttu-id="38328-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="38328-138">S_OK</span></span> 
  
> <span data-ttu-id="38328-139">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="38328-139">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="38328-140">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="38328-140">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="38328-141">予期しないまたは不明な配信元のエラーにより、操作が完了しませんでした。</span><span class="sxs-lookup"><span data-stu-id="38328-141">An error of unexpected or unknown origin prevented the operation from completing.</span></span> <span data-ttu-id="38328-142">これには、プロファイルウィザードの MAPI サブシステムを初期化できない、既定のプロファイルにアクセスできない、およびダイアログボックスからエラーが返されるなどの可能性があります。</span><span class="sxs-lookup"><span data-stu-id="38328-142">Possibilities include failure to initialize the MAPI subsystem for the Profile Wizard, inability to access the default profile, and an error return from the dialog box.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="38328-143">解説</span><span class="sxs-lookup"><span data-stu-id="38328-143">Remarks</span></span>

<span data-ttu-id="38328-144">**launchwizardentry**関数プロトタイプの mapi 実装は、mapi プロファイルウィザードアプリケーションへのエントリポイントです。</span><span class="sxs-lookup"><span data-stu-id="38328-144">The MAPI implementation of the **LAUNCHWIZARDENTRY** function prototype is the entry point into the MAPI Profile Wizard application.</span></span> <span data-ttu-id="38328-145">[MAPI 名] このエントリポイントの**launchwizard**。</span><span class="sxs-lookup"><span data-stu-id="38328-145">MAPI names this entry point **LaunchWizard**.</span></span> 
  
<span data-ttu-id="38328-146">_ulflags_パラメーターに MAPI_PW_ADD_SERVICE_ONLY フラグが設定されている場合は、次のルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="38328-146">When the MAPI_PW_ADD_SERVICE_ONLY flag is set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="38328-147">MAPI_PW_LAUNCHED_BY_CONFIG フラグは、ウェルカムページが表示されないようにします。</span><span class="sxs-lookup"><span data-stu-id="38328-147">The MAPI_PW_LAUNCHED_BY_CONFIG flag inhibits the welcome page from being displayed.</span></span> 
    
- <span data-ttu-id="38328-148">MAPI_PW_HIDE_SERVICES_LIST および MAPI_PW_PROVIDER_UI_ONLY フラグは、既定のプロファイルがない場合にのみ役立ちます。</span><span class="sxs-lookup"><span data-stu-id="38328-148">The MAPI_PW_HIDE_SERVICES_LIST and MAPI_PW_PROVIDER_UI_ONLY flags are useful only when there is no default profile.</span></span> <span data-ttu-id="38328-149">この場合、次のフラグは、どのプロファイルウィザードページを表示するかを決定します。</span><span class="sxs-lookup"><span data-stu-id="38328-149">In this case these flags determine which Profile Wizard page is to be displayed.</span></span> 
    
- <span data-ttu-id="38328-150">既定のプロファイルが存在する場合、プロファイルウィザードページは表示されません。</span><span class="sxs-lookup"><span data-stu-id="38328-150">If a default profile exists, none of the Profile Wizard pages are to be displayed.</span></span> 
    
- <span data-ttu-id="38328-151">既定のプロファイルが存在する場合、 _lppszServiceNameToAdd_パラメーターによって表示されるメッセージサービスは1つだけで、そのメッセージサービスは既に既定のプロファイルになっています。プロファイルウィザードは、プロファイルに何も追加せずに S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="38328-151">If a default profile exists, only one message service is listed through the  _lppszServiceNameToAdd_ parameter, and that message service is already in the default profile, the Profile Wizard returns S_OK without adding anything to the profile.</span></span> 
    
<span data-ttu-id="38328-152">プロファイルに追加されるすべてのメッセージサービスについて、プロファイルウィザードは[msgserviceentry](msgserviceentry.md)プロトタイプに基づいてサービスのエントリポイント関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="38328-152">For every message service to be added to the profile, the Profile Wizard calls the service's entry point function based on the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="38328-153">プロファイルに追加するメッセージサービスから選択された各サービスプロバイダーについて、プロファイルウィザードは、 [wizardentry](wizardentry.md) prototype に基づいて、プロバイダーのエントリポイント関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="38328-153">For each service provider selected from a message service to be added to the profile, the Profile Wizard calls the provider's entry point function based on the [WIZARDENTRY](wizardentry.md) prototype.</span></span> <span data-ttu-id="38328-154">対話形式の構成では、プロパティページのすべてのユーザーイベントによって、プロファイルウィザードによって、 [servicewizarddlgproc](servicewizarddlgproc.md)プロトタイプに基づいてプロバイダーのコールバック関数が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="38328-154">During interactive configuration, every user event in the property pages causes the Profile Wizard to call the provider's callback function based on the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
  
<span data-ttu-id="38328-155">プロファイルに追加されるサービスプロバイダーがプロファイルウィザードページをサポートしている場合は、プロファイルのプログラムによる構成を許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="38328-155">If a service provider being added to the profile supports the Profile Wizard pages, it must allow programmatic configuration of the profile.</span></span>
  

