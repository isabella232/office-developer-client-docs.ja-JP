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
ms.openlocfilehash: d80671331c2760c574ab32d79115a352ee4bcf25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801288"
---
# <a name="launchwizardentry"></a><span data-ttu-id="e9335-103">LAUNCHWIZARDENTRY</span><span class="sxs-lookup"><span data-stu-id="e9335-103">LAUNCHWIZARDENTRY</span></span>

  
  
<span data-ttu-id="e9335-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e9335-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e9335-105">1 つまたは複数のメッセージ サービスをプロファイルに追加するためのプロファイル ウィザード アプリケーションを起動する関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="e9335-105">Defines a function that starts the Profile Wizard application for the purpose of adding one or more message services to a profile.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e9335-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e9335-106">Header file:</span></span>  <br/> |<span data-ttu-id="e9335-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="e9335-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="e9335-108">によって実装される関数の定義:</span><span class="sxs-lookup"><span data-stu-id="e9335-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="e9335-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e9335-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e9335-110">によって呼び出される関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="e9335-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="e9335-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="e9335-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT LAUNCHWIZARDENTRY(
  HWND hParentWnd,
  ULONG ulFlags,
  LPCSTR FAR * lppszServiceNameToAdd,
  ULONG cbBufferMax,
  LPSTR lpszNewProfileName
);
```

## <a name="parameters"></a><span data-ttu-id="e9335-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e9335-112">Parameters</span></span>

 <span data-ttu-id="e9335-113">_hParentWnd_</span><span class="sxs-lookup"><span data-stu-id="e9335-113">_hParentWnd_</span></span>
  
> <span data-ttu-id="e9335-114">[in]呼び出し元の親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="e9335-114">[in] A handle to the caller's parent window.</span></span> <span data-ttu-id="e9335-115">呼び出し元は、親ウィンドウを持たない場合、 _hParentWnd_パラメーターは、NULL のはずです。</span><span class="sxs-lookup"><span data-stu-id="e9335-115">If the caller does not have a parent window, the  _hParentWnd_ parameter should be NULL.</span></span> 
    
 <span data-ttu-id="e9335-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e9335-116">_ulFlags_</span></span>
  
> <span data-ttu-id="e9335-117">[in]プロファイル ウィザードのオプションを示すフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="e9335-117">[in] Bitmask of flags indicating options for the Profile Wizard.</span></span> <span data-ttu-id="e9335-118">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="e9335-118">The following flags can be set:</span></span>
    
<span data-ttu-id="e9335-119">MAPI_PW_ADD_SERVICE_ONLY</span><span class="sxs-lookup"><span data-stu-id="e9335-119">MAPI_PW_ADD_SERVICE_ONLY</span></span> 
  
> <span data-ttu-id="e9335-120">プロファイル ウィザードでは、 _lppszServiceNameToAdd_パラメーターでは、表示されているメッセージ サービスのみを追加し、メッセージ サービスを選択するためには、そのページを表示できません。</span><span class="sxs-lookup"><span data-stu-id="e9335-120">The Profile Wizard is to add only the message services listed through the  _lppszServiceNameToAdd_ parameter, and not display its page for selecting message services.</span></span> 
    
<span data-ttu-id="e9335-121">MAPI_PW_FIRST_PROFILE</span><span class="sxs-lookup"><span data-stu-id="e9335-121">MAPI_PW_FIRST_PROFILE</span></span> 
  
> <span data-ttu-id="e9335-122">プロファイルを作成するのには、このワークステーションの 1 つ目です。</span><span class="sxs-lookup"><span data-stu-id="e9335-122">The profile to be created is the first one for this workstation.</span></span> 
    
<span data-ttu-id="e9335-123">MAPI_PW_HIDE_SERVICES_LIST</span><span class="sxs-lookup"><span data-stu-id="e9335-123">MAPI_PW_HIDE_SERVICES_LIST</span></span> 
  
> <span data-ttu-id="e9335-124">メッセージ サービスを選択するためのプロファイル ウィザードのページが表示されない必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9335-124">The Profile Wizard's page for selecting message services should not be displayed.</span></span> 
    
<span data-ttu-id="e9335-125">MAPI_PW_LAUNCHED_BY_CONFIG</span><span class="sxs-lookup"><span data-stu-id="e9335-125">MAPI_PW_LAUNCHED_BY_CONFIG</span></span> 
  
> <span data-ttu-id="e9335-126">プロファイル ウィザードは、コントロール パネルの構成アプリケーションによって起動されました。</span><span class="sxs-lookup"><span data-stu-id="e9335-126">The Profile Wizard was launched by the Control Panel configuration application.</span></span> 
    
<span data-ttu-id="e9335-127">MAPI_PW_PROVIDER_UI_ONLY</span><span class="sxs-lookup"><span data-stu-id="e9335-127">MAPI_PW_PROVIDER_UI_ONLY</span></span> 
  
> <span data-ttu-id="e9335-128">サービス プロバイダーの構成] ダイアログ ボックスのみを表示する必要があり、プロファイル ウィザードのページは表示されません。</span><span class="sxs-lookup"><span data-stu-id="e9335-128">Only the service providers's configuration dialog boxes should be displayed and the Profile Wizard's pages should not appear.</span></span> <span data-ttu-id="e9335-129">このフラグは、MAPI_PW_ADD_SERVICE_ONLY フラグが設定されている場合にのみ設定できます。</span><span class="sxs-lookup"><span data-stu-id="e9335-129">This flag can only be set if the MAPI_PW_ADD_SERVICE_ONLY flag is set.</span></span> 
    
 <span data-ttu-id="e9335-130">_lppszServiceNameToAdd_</span><span class="sxs-lookup"><span data-stu-id="e9335-130">_lppszServiceNameToAdd_</span></span>
  
> <span data-ttu-id="e9335-131">[in]プロファイルに追加するメッセージ サービスの名前を格納する文字列の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e9335-131">[in] Pointer to an array of strings that contains the names of the message services to be added to the profile.</span></span> <span data-ttu-id="e9335-132">配列は NULL 値で終了してください。</span><span class="sxs-lookup"><span data-stu-id="e9335-132">The array must terminate with a NULL value.</span></span> 
    
 <span data-ttu-id="e9335-133">_cbBufferMax_</span><span class="sxs-lookup"><span data-stu-id="e9335-133">_cbBufferMax_</span></span>
  
> <span data-ttu-id="e9335-134">[in]_LpszNewProfileName_パラメーターが指すバッファーのサイズです。</span><span class="sxs-lookup"><span data-stu-id="e9335-134">[in] Size of the buffer pointed to by the  _lpszNewProfileName_ parameter.</span></span> 
    
 <span data-ttu-id="e9335-135">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="e9335-135">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="e9335-136">[out]作成したプロファイルの名前を**LAUNCHWIZARDENTRY**に基づく関数が返す文字列のバッファーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e9335-136">[out] Pointer to a string buffer where the function based on **LAUNCHWIZARDENTRY** returns the name of the created profile.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e9335-137">�߂�l</span><span class="sxs-lookup"><span data-stu-id="e9335-137">Return value</span></span>

<span data-ttu-id="e9335-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="e9335-138">S_OK</span></span> 
  
> <span data-ttu-id="e9335-139">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="e9335-139">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="e9335-140">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="e9335-140">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="e9335-141">予期しない、または不明な発生元のエラーでは、操作を完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="e9335-141">An error of unexpected or unknown origin prevented the operation from completing.</span></span> <span data-ttu-id="e9335-142">ダイアログ ボックスから取得する既定のプロファイル、およびエラーにアクセスできない可能性には、プロファイル ウィザードは、MAPI サブシステムを初期化するためにエラーが含まれている。</span><span class="sxs-lookup"><span data-stu-id="e9335-142">Possibilities include failure to initialize the MAPI subsystem for the Profile Wizard, inability to access the default profile, and an error return from the dialog box.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e9335-143">注釈</span><span class="sxs-lookup"><span data-stu-id="e9335-143">Remarks</span></span>

<span data-ttu-id="e9335-144">**LAUNCHWIZARDENTRY**関数のプロトタイプの MAPI 実装は、MAPI プロファイル ウィザードのアプリケーションへのエントリ ポイントです。</span><span class="sxs-lookup"><span data-stu-id="e9335-144">The MAPI implementation of the **LAUNCHWIZARDENTRY** function prototype is the entry point into the MAPI Profile Wizard application.</span></span> <span data-ttu-id="e9335-145">MAPI では、このエントリ ポイント**LaunchWizard**を名前です。</span><span class="sxs-lookup"><span data-stu-id="e9335-145">MAPI names this entry point **LaunchWizard**.</span></span> 
  
<span data-ttu-id="e9335-146">_UlFlags_パラメーターに MAPI_PW_ADD_SERVICE_ONLY フラグを設定すると、ときに、次の規則が適用されます。</span><span class="sxs-lookup"><span data-stu-id="e9335-146">When the MAPI_PW_ADD_SERVICE_ONLY flag is set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="e9335-147">MAPI_PW_LAUNCHED_BY_CONFIG フラグは、表示されている [ようこそ] ページを禁止します。</span><span class="sxs-lookup"><span data-stu-id="e9335-147">The MAPI_PW_LAUNCHED_BY_CONFIG flag inhibits the welcome page from being displayed.</span></span> 
    
- <span data-ttu-id="e9335-148">MAPI_PW_HIDE_SERVICES_LIST と MAPI_PW_PROVIDER_UI_ONLY のフラグは、既定のプロファイルがない場合にのみ便利です。</span><span class="sxs-lookup"><span data-stu-id="e9335-148">The MAPI_PW_HIDE_SERVICES_LIST and MAPI_PW_PROVIDER_UI_ONLY flags are useful only when there is no default profile.</span></span> <span data-ttu-id="e9335-149">ここではこれらのフラグは、どのプロファイル ウィザードのページが表示されるを確認します。</span><span class="sxs-lookup"><span data-stu-id="e9335-149">In this case these flags determine which Profile Wizard page is to be displayed.</span></span> 
    
- <span data-ttu-id="e9335-150">既定のプロファイルが存在する場合、プロファイル ウィザードのページ、表示します。</span><span class="sxs-lookup"><span data-stu-id="e9335-150">If a default profile exists, none of the Profile Wizard pages are to be displayed.</span></span> 
    
- <span data-ttu-id="e9335-151">既定のプロファイルが存在する、 _lppszServiceNameToAdd_パラメーターでは、サービスの 1 つのメッセージが表示されているとメッセージ サービスは既に既定のプロファイル、プロファイル ウィザードは、プロファイルに何も追加せず S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="e9335-151">If a default profile exists, only one message service is listed through the  _lppszServiceNameToAdd_ parameter, and that message service is already in the default profile, the Profile Wizard returns S_OK without adding anything to the profile.</span></span> 
    
<span data-ttu-id="e9335-152">プロファイルに追加するすべてのメッセージ サービスは、プロファイル ウィザードは、 [MSGSERVICEENTRY](msgserviceentry.md)プロトタイプに基づいて、サービスのエントリ ポイント関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e9335-152">For every message service to be added to the profile, the Profile Wizard calls the service's entry point function based on the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="e9335-153">プロファイルに追加するメッセージ サービスから選択したサービス プロバイダーごとに、プロファイル ウィザードは[WIZARDENTRY](wizardentry.md)プロトタイプに基づいて、プロバイダーのエントリ ポイント関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e9335-153">For each service provider selected from a message service to be added to the profile, the Profile Wizard calls the provider's entry point function based on the [WIZARDENTRY](wizardentry.md) prototype.</span></span> <span data-ttu-id="e9335-154">対話型の構成時にプロパティ ページで、すべてのユーザー イベントはプロファイル ウィザードで[SERVICEWIZARDDLGPROC](servicewizarddlgproc.md)プロトタイプに基づいて、プロバイダーのコールバック関数を呼び出すとします。</span><span class="sxs-lookup"><span data-stu-id="e9335-154">During interactive configuration, every user event in the property pages causes the Profile Wizard to call the provider's callback function based on the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
  
<span data-ttu-id="e9335-155">プロファイルに追加するサービス プロバイダーは、プロファイル ウィザードのページをサポートする場合は、プロファイルのプログラムによる構成を許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9335-155">If a service provider being added to the profile supports the Profile Wizard pages, it must allow programmatic configuration of the profile.</span></span>
  

