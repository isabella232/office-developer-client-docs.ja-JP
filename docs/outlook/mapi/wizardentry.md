---
title: WIZARDENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.WIZARDENTRY
api_type:
- COM
ms.assetid: e807c6b5-06cd-4ade-9d9e-69ba6abd1614
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 907984a80dbb6c5464f95def1481d002f9d6638a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430680"
---
# <a name="wizardentry"></a><span data-ttu-id="13de3-103">WIZARDENTRY</span><span class="sxs-lookup"><span data-stu-id="13de3-103">WIZARDENTRY</span></span>

  
  
<span data-ttu-id="13de3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13de3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13de3-105">プロバイダーの構成プロパティ シートを表示するのに十分な情報を取得するためにプロファイル ウィザードが呼び出すサービス プロバイダー エントリ ポイント関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="13de3-105">Defines a service provider entry point function which the Profile Wizard calls to retrieve enough information to display the provider's configuration property sheets.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="13de3-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="13de3-106">Header file:</span></span>  <br/> |<span data-ttu-id="13de3-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="13de3-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="13de3-108">定義された関数は、次の方法で実装されます。</span><span class="sxs-lookup"><span data-stu-id="13de3-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="13de3-109">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="13de3-109">Service providers</span></span>  <br/> |
|<span data-ttu-id="13de3-110">によって呼び出される定義済み関数:</span><span class="sxs-lookup"><span data-stu-id="13de3-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="13de3-111">MAPI プロファイル ウィザード</span><span class="sxs-lookup"><span data-stu-id="13de3-111">MAPI Profile Wizard</span></span>  <br/> |
   
```cpp
ULONG WIZARDENTRY(
  HINSTANCE hProviderDLLInstance,
  LPSTR FAR * lpcsResourceName,
  DLGPROC FAR * lppDlgProc,
  LPMAPIPROP lpMAPIProp,
  LPMAPISUPPORTOBJECT lpMapiSupportObject
);
```

## <a name="parameters"></a><span data-ttu-id="13de3-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="13de3-112">Parameters</span></span>

 <span data-ttu-id="13de3-113">_hProviderDLLInstance_</span><span class="sxs-lookup"><span data-stu-id="13de3-113">_hProviderDLLInstance_</span></span>
  
> <span data-ttu-id="13de3-114">[in]サービス プロバイダーの DLL のインスタンス ハンドル。</span><span class="sxs-lookup"><span data-stu-id="13de3-114">[in] Instance handle of the service provider's DLL.</span></span> 
    
 <span data-ttu-id="13de3-115">_lpcsResourceName_</span><span class="sxs-lookup"><span data-stu-id="13de3-115">_lpcsResourceName_</span></span>
  
> <span data-ttu-id="13de3-116">[out]構成時にプロファイル ウィザードによって表示されるダイアログ リソースの完全な名前を含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="13de3-116">[out] Pointer to a string that contains the full name of the dialog resource that should be displayed by the Profile Wizard during configuration.</span></span> <span data-ttu-id="13de3-117">NULL ターミネーターを含む文字列の最大サイズは 32 文字です。</span><span class="sxs-lookup"><span data-stu-id="13de3-117">The maximum size of the string, including the NULL terminator, is 32 characters.</span></span> 
    
 <span data-ttu-id="13de3-118">_lppDlgProc_</span><span class="sxs-lookup"><span data-stu-id="13de3-118">_lppDlgProc_</span></span>
  
> <span data-ttu-id="13de3-119">[out]プロファイル ウィザードによってWindowsさまざまなイベントをプロバイダーに通知するために呼び出される標準のダイアログ ボックス プロシージャへのポインター。</span><span class="sxs-lookup"><span data-stu-id="13de3-119">[out] Pointer to a standard Windows dialog box procedure that will be called by the Profile Wizard to notify the provider of various events.</span></span> 
    
 <span data-ttu-id="13de3-120">_lpMAPIProp_</span><span class="sxs-lookup"><span data-stu-id="13de3-120">_lpMAPIProp_</span></span>
  
> <span data-ttu-id="13de3-121">[in]構成プロパティへのアクセスを提供するプロパティ インターフェイス実装へのポインター。</span><span class="sxs-lookup"><span data-stu-id="13de3-121">[in] Pointer to a property interface implementation that provides access to the configuration properties.</span></span> 
    
 <span data-ttu-id="13de3-122">_lpMapiSupportObject_</span><span class="sxs-lookup"><span data-stu-id="13de3-122">_lpMapiSupportObject_</span></span>
  
> <span data-ttu-id="13de3-123">[in]このセッションに適用可能な MAPI サポート オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="13de3-123">[in] Pointer to the MAPI support object applicable to this session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="13de3-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="13de3-124">Return value</span></span>

<span data-ttu-id="13de3-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="13de3-125">S_OK</span></span> 
  
> <span data-ttu-id="13de3-126">サービス プロバイダーの **WIZARDENTRY** 関数が正常に呼び出されました。</span><span class="sxs-lookup"><span data-stu-id="13de3-126">The service provider's **WIZARDENTRY** function was called successfully.</span></span> 
    
<span data-ttu-id="13de3-127">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="13de3-127">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="13de3-128">予期しない、または不明な発生源のエラーにより、操作が完了しなかっていません。</span><span class="sxs-lookup"><span data-stu-id="13de3-128">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="13de3-129">注釈</span><span class="sxs-lookup"><span data-stu-id="13de3-129">Remarks</span></span>

<span data-ttu-id="13de3-130">プロファイル ウィザードは、サービス プロバイダーの構成ユーザー インターフェイスを表示する準備ができたら **、WIZARDENTRY** ベースの関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="13de3-130">The Profile Wizard calls the **WIZARDENTRY** based function when it is ready to display the service provider's configuration user interface.</span></span> <span data-ttu-id="13de3-131">プロファイル ウィザードは、すべてのプロバイダーの構成が完了したら [、IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)を呼び出して構成プロパティをプロファイルに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="13de3-131">When the Profile Wizard is finished configuring all providers, it writes the configuration properties to the profile by calling [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="13de3-132">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="13de3-132">Notes to implementers</span></span>

<span data-ttu-id="13de3-133">**WIZARDENTRY ベースの関数** の名前は、MAPISVC.INF の WIZARD_ENTRY_NAMEエントリに配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13de3-133">The name of the **WIZARDENTRY** based function must be placed in the WIZARD_ENTRY_NAME entry in MAPISVC.INF.</span></span> 
  
<span data-ttu-id="13de3-134">リソース名は、プロファイル ウィザードのウィンドウに表示されるダイアログ リソースの名前です。</span><span class="sxs-lookup"><span data-stu-id="13de3-134">The resource name is that of the dialog resource that will be rendered in the pane of the Profile Wizard.</span></span> <span data-ttu-id="13de3-135">返されるリソースは、1 つのダイアログ リソース内のすべてのページを含む必要があります。</span><span class="sxs-lookup"><span data-stu-id="13de3-135">The resource that is passed back needs to contain all the pages in a single dialog resource.</span></span> <span data-ttu-id="13de3-136">プロファイル ウィザードがこのリソースを受け取った場合、ダイアログ スタイルは無視されますが、コントロール のスタイルは無視され、[プロファイル ウィザード] ページの子としてすべてのコントロールが作成されます。</span><span class="sxs-lookup"><span data-stu-id="13de3-136">When the Profile Wizard receives this resource, it ignores the dialog style, but not the control styles, and creates all the controls as children of the Profile Wizard page.</span></span> <span data-ttu-id="13de3-137">すべてのコントロールは、最初は非表示になっています。</span><span class="sxs-lookup"><span data-stu-id="13de3-137">All controls are initially hidden.</span></span> <span data-ttu-id="13de3-138">プロバイダーは、コントロールの座標が 0 または 0 から始め、最大幅が 200 ダイアログ 単位、最大高さ 150 ダイアログ 単位を超えないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="13de3-138">Providers should make sure that the coordinates for their controls are zero or zero-based, and that they do not exceed a maximum width of 200 dialog units and a maximum height of 150 dialog units.</span></span> <span data-ttu-id="13de3-139">400 より下のコントロール識別子は、プロファイル ウィザード用に予約されています。</span><span class="sxs-lookup"><span data-stu-id="13de3-139">Control identifiers below 400 are reserved for the Profile Wizard.</span></span> <span data-ttu-id="13de3-140">プロファイル ウィザードは、プロバイダーのユーザー インターフェイスの上に、プロバイダーのタイトルを太字で表示します。</span><span class="sxs-lookup"><span data-stu-id="13de3-140">The Profile Wizard displays the provider's title in bold text above the provider's user interface.</span></span> 
  
<span data-ttu-id="13de3-141">_lpMAPIProp_ パラメーターで指定されたプロパティ インターフェイス ポインターは、将来の参照のためにプロバイダーが保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13de3-141">The property interface pointer supplied in the  _lpMAPIProp_ parameter should be retained by the provider for future reference.</span></span> <span data-ttu-id="13de3-142">プロファイル ウィザードは、最も基本的なプロパティのセットのみを処理し、プロバイダーはプロパティ インターフェイスの実装を使用して追加のプロパティを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="13de3-142">The Profile Wizard deals with only the most basic set of properties, and the provider can use the property interface implementation to include additional properties.</span></span> <span data-ttu-id="13de3-143">構成中に、プロバイダーは、プロパティ インターフェイスを実装するオブジェクトに構成プロパティを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13de3-143">During configuration, providers should add their configuration properties to the object implementing the property interface.</span></span> <span data-ttu-id="13de3-144">すべてのプロバイダーが構成された後、プロファイル ウィザードは、これらのプロパティをプロファイルに追加します。</span><span class="sxs-lookup"><span data-stu-id="13de3-144">After all providers have been configured, the Profile Wizard adds these properties to the profile.</span></span> 
  
<span data-ttu-id="13de3-145">この関数の使い方の詳細については、「メッセージ サービス構成のサポート [」を参照してください](supporting-message-service-configuration.md)。</span><span class="sxs-lookup"><span data-stu-id="13de3-145">For more information about how to use this function, see [Supporting Message Service Configuration](supporting-message-service-configuration.md).</span></span> 
  

