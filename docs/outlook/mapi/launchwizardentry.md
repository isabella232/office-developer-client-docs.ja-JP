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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c1509918eb587c17deebf95317cf57b4ab19928a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437386"
---
# <a name="launchwizardentry"></a><span data-ttu-id="e6e7e-103">LAUNCHWIZARDENTRY</span><span class="sxs-lookup"><span data-stu-id="e6e7e-103">LAUNCHWIZARDENTRY</span></span>

  
  
<span data-ttu-id="e6e7e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6e7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6e7e-105">プロファイルに 1 つ以上のメッセージ サービスを追加する目的で、プロファイル ウィザード アプリケーションを開始する関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="e6e7e-105">Defines a function that starts the Profile Wizard application for the purpose of adding one or more message services to a profile.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e6e7e-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e6e7e-106">Header file:</span></span>  <br/> |<span data-ttu-id="e6e7e-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="e6e7e-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="e6e7e-108">定義された関数は、次の方法で実装されます。</span><span class="sxs-lookup"><span data-stu-id="e6e7e-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="e6e7e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e6e7e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e6e7e-110">によって呼び出される定義済み関数:</span><span class="sxs-lookup"><span data-stu-id="e6e7e-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="e6e7e-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="e6e7e-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT LAUNCHWIZARDENTRY(
  HWND hParentWnd,
  ULONG ulFlags,
  LPCSTR FAR * lppszServiceNameToAdd,
  ULONG cbBufferMax,
  LPSTR lpszNewProfileName
);
```

## <a name="parameters"></a><span data-ttu-id="e6e7e-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e6e7e-112">Parameters</span></span>

 <span data-ttu-id="e6e7e-113">_hParentWnd_</span><span class="sxs-lookup"><span data-stu-id="e6e7e-113">_hParentWnd_</span></span>
  
> <span data-ttu-id="e6e7e-114">[in]呼び出し元の親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="e6e7e-114">[in] A handle to the caller's parent window.</span></span> <span data-ttu-id="e6e7e-115">呼び出し元に親ウィンドウがない場合  _、hParentWnd_ パラメーターは NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="e6e7e-115">If the caller does not have a parent window, the  _hParentWnd_ parameter should be NULL.</span></span> 
    
 <span data-ttu-id="e6e7e-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e6e7e-116">_ulFlags_</span></span>
  
> <span data-ttu-id="e6e7e-117">[in]プロファイル ウィザードのオプションを示すフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="e6e7e-117">[in] Bitmask of flags indicating options for the Profile Wizard.</span></span> <span data-ttu-id="e6e7e-118">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="e6e7e-118">The following flags can be set:</span></span>
    
<span data-ttu-id="e6e7e-119">MAPI_PW_ADD_SERVICE_ONLY</span><span class="sxs-lookup"><span data-stu-id="e6e7e-119">MAPI_PW_ADD_SERVICE_ONLY</span></span> 
  
> <span data-ttu-id="e6e7e-120">プロファイル ウィザードでは  _、lppszServiceNameToAdd_ パラメーターを使用して一覧表示されているメッセージ サービスのみを追加し、メッセージ サービスを選択するページは表示されません。</span><span class="sxs-lookup"><span data-stu-id="e6e7e-120">The Profile Wizard is to add only the message services listed through the  _lppszServiceNameToAdd_ parameter, and not display its page for selecting message services.</span></span> 
    
<span data-ttu-id="e6e7e-121">MAPI_PW_FIRST_PROFILE</span><span class="sxs-lookup"><span data-stu-id="e6e7e-121">MAPI_PW_FIRST_PROFILE</span></span> 
  
> <span data-ttu-id="e6e7e-122">作成するプロファイルは、このワークステーションの最初のプロファイルです。</span><span class="sxs-lookup"><span data-stu-id="e6e7e-122">The profile to be created is the first one for this workstation.</span></span> 
    
<span data-ttu-id="e6e7e-123">MAPI_PW_HIDE_SERVICES_LIST</span><span class="sxs-lookup"><span data-stu-id="e6e7e-123">MAPI_PW_HIDE_SERVICES_LIST</span></span> 
  
> <span data-ttu-id="e6e7e-124">メッセージ サービスを選択するプロファイル ウィザードのページは表示されません。</span><span class="sxs-lookup"><span data-stu-id="e6e7e-124">The Profile Wizard's page for selecting message services should not be displayed.</span></span> 
    
<span data-ttu-id="e6e7e-125">MAPI_PW_LAUNCHED_BY_CONFIG</span><span class="sxs-lookup"><span data-stu-id="e6e7e-125">MAPI_PW_LAUNCHED_BY_CONFIG</span></span> 
  
> <span data-ttu-id="e6e7e-126">プロファイル ウィザードは、コントロール パネル構成アプリケーションによって起動されました。</span><span class="sxs-lookup"><span data-stu-id="e6e7e-126">The Profile Wizard was launched by the Control Panel configuration application.</span></span> 
    
<span data-ttu-id="e6e7e-127">MAPI_PW_PROVIDER_UI_ONLY</span><span class="sxs-lookup"><span data-stu-id="e6e7e-127">MAPI_PW_PROVIDER_UI_ONLY</span></span> 
  
> <span data-ttu-id="e6e7e-128">サービス プロバイダーの構成ダイアログ ボックスだけが表示され、プロファイル ウィザードのページは表示されません。</span><span class="sxs-lookup"><span data-stu-id="e6e7e-128">Only the service providers's configuration dialog boxes should be displayed and the Profile Wizard's pages should not appear.</span></span> <span data-ttu-id="e6e7e-129">このフラグを設定できるのは、MAPI_PW_ADD_SERVICE_ONLYフラグが設定されている場合のみです。</span><span class="sxs-lookup"><span data-stu-id="e6e7e-129">This flag can only be set if the MAPI_PW_ADD_SERVICE_ONLY flag is set.</span></span> 
    
 <span data-ttu-id="e6e7e-130">_lppszServiceNameToAdd_</span><span class="sxs-lookup"><span data-stu-id="e6e7e-130">_lppszServiceNameToAdd_</span></span>
  
> <span data-ttu-id="e6e7e-131">[in]プロファイルに追加するメッセージ サービスの名前を含む文字列の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e6e7e-131">[in] Pointer to an array of strings that contains the names of the message services to be added to the profile.</span></span> <span data-ttu-id="e6e7e-132">配列は NULL 値で終了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e6e7e-132">The array must terminate with a NULL value.</span></span> 
    
 <span data-ttu-id="e6e7e-133">_cbBufferMax_</span><span class="sxs-lookup"><span data-stu-id="e6e7e-133">_cbBufferMax_</span></span>
  
> <span data-ttu-id="e6e7e-134">[in]  _lpszNewProfileName_ パラメーターが指すバッファーのサイズ。</span><span class="sxs-lookup"><span data-stu-id="e6e7e-134">[in] Size of the buffer pointed to by the  _lpszNewProfileName_ parameter.</span></span> 
    
 <span data-ttu-id="e6e7e-135">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="e6e7e-135">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="e6e7e-136">[out] **LAUNCHWIZARDENTRY** に基づく関数が作成されたプロファイルの名前を返す文字列バッファーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e6e7e-136">[out] Pointer to a string buffer where the function based on **LAUNCHWIZARDENTRY** returns the name of the created profile.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e6e7e-137">戻り値</span><span class="sxs-lookup"><span data-stu-id="e6e7e-137">Return value</span></span>

<span data-ttu-id="e6e7e-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="e6e7e-138">S_OK</span></span> 
  
> <span data-ttu-id="e6e7e-139">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="e6e7e-139">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="e6e7e-140">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="e6e7e-140">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="e6e7e-141">予期しない、または不明な発生源のエラーにより、操作が完了しなかっていません。</span><span class="sxs-lookup"><span data-stu-id="e6e7e-141">An error of unexpected or unknown origin prevented the operation from completing.</span></span> <span data-ttu-id="e6e7e-142">プロファイル ウィザードの MAPI サブシステムの初期化に失敗した場合、既定のプロファイルにアクセスできません。ダイアログ ボックスからエラーが返される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e6e7e-142">Possibilities include failure to initialize the MAPI subsystem for the Profile Wizard, inability to access the default profile, and an error return from the dialog box.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e6e7e-143">注釈</span><span class="sxs-lookup"><span data-stu-id="e6e7e-143">Remarks</span></span>

<span data-ttu-id="e6e7e-144">**LAUNCHWIZARDENTRY** 関数プロトタイプの MAPI 実装は、MAPI プロファイル ウィザード アプリケーションへのエントリ ポイントです。</span><span class="sxs-lookup"><span data-stu-id="e6e7e-144">The MAPI implementation of the **LAUNCHWIZARDENTRY** function prototype is the entry point into the MAPI Profile Wizard application.</span></span> <span data-ttu-id="e6e7e-145">MAPI の名前は、このエントリ ポイント **LaunchWizard です**。</span><span class="sxs-lookup"><span data-stu-id="e6e7e-145">MAPI names this entry point **LaunchWizard**.</span></span> 
  
<span data-ttu-id="e6e7e-146">_ulFlags_ パラメーター MAPI_PW_ADD_SERVICE_ONLYフラグが設定されている場合、次のルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="e6e7e-146">When the MAPI_PW_ADD_SERVICE_ONLY flag is set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="e6e7e-147">このMAPI_PW_LAUNCHED_BY_CONFIGは、ウェルカム ページの表示を禁止します。</span><span class="sxs-lookup"><span data-stu-id="e6e7e-147">The MAPI_PW_LAUNCHED_BY_CONFIG flag inhibits the welcome page from being displayed.</span></span> 
    
- <span data-ttu-id="e6e7e-148">既定MAPI_PW_HIDE_SERVICES_LISTおよびMAPI_PW_PROVIDER_UI_ONLYフラグは、既定のプロファイルがない場合にのみ役立ちます。</span><span class="sxs-lookup"><span data-stu-id="e6e7e-148">The MAPI_PW_HIDE_SERVICES_LIST and MAPI_PW_PROVIDER_UI_ONLY flags are useful only when there is no default profile.</span></span> <span data-ttu-id="e6e7e-149">この場合、これらのフラグは、表示するプロファイル ウィザード ページを決定します。</span><span class="sxs-lookup"><span data-stu-id="e6e7e-149">In this case these flags determine which Profile Wizard page is to be displayed.</span></span> 
    
- <span data-ttu-id="e6e7e-150">既定のプロファイルが存在する場合、どのプロファイル ウィザード ページも表示されません。</span><span class="sxs-lookup"><span data-stu-id="e6e7e-150">If a default profile exists, none of the Profile Wizard pages are to be displayed.</span></span> 
    
- <span data-ttu-id="e6e7e-151">既定のプロファイルが存在する場合  _、lppszServiceNameToAdd_ パラメーターを使用して 1 つのメッセージ サービスだけが一覧表示され、そのメッセージ サービスは既定のプロファイルに既に存在し、プロファイル ウィザードはプロファイルに何も追加せずに S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="e6e7e-151">If a default profile exists, only one message service is listed through the  _lppszServiceNameToAdd_ parameter, and that message service is already in the default profile, the Profile Wizard returns S_OK without adding anything to the profile.</span></span> 
    
<span data-ttu-id="e6e7e-152">プロファイルに追加するメッセージ サービスごとに、プロファイル ウィザードは [MSGSERVICEENTRY](msgserviceentry.md) プロトタイプに基づいてサービスのエントリ ポイント関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e6e7e-152">For every message service to be added to the profile, the Profile Wizard calls the service's entry point function based on the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="e6e7e-153">プロファイルに追加するメッセージ サービスから選択された各サービス プロバイダーについて、プロファイル ウィザードは WIZARDENTRY プロトタイプに基づいてプロバイダーのエントリ ポイント関数 [を呼び出](wizardentry.md) します。</span><span class="sxs-lookup"><span data-stu-id="e6e7e-153">For each service provider selected from a message service to be added to the profile, the Profile Wizard calls the provider's entry point function based on the [WIZARDENTRY](wizardentry.md) prototype.</span></span> <span data-ttu-id="e6e7e-154">対話型構成中に、プロパティ ページ内のすべてのユーザー イベントによって、プロファイル ウィザードは [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) プロトタイプに基づいてプロバイダーのコールバック関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e6e7e-154">During interactive configuration, every user event in the property pages causes the Profile Wizard to call the provider's callback function based on the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
  
<span data-ttu-id="e6e7e-155">プロファイルに追加するサービス プロバイダーがプロファイル ウィザード ページをサポートしている場合は、プロファイルのプログラムによる構成を許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e6e7e-155">If a service provider being added to the profile supports the Profile Wizard pages, it must allow programmatic configuration of the profile.</span></span>
  

