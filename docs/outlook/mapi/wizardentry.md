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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3d78b4e6a4a0cc3363edefc84e7ae80dbe72c510
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590359"
---
# <a name="wizardentry"></a><span data-ttu-id="e08e6-103">WIZARDENTRY</span><span class="sxs-lookup"><span data-stu-id="e08e6-103">WIZARDENTRY</span></span>

  
  
<span data-ttu-id="e08e6-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e08e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e08e6-105">プロファイル ウィザードは、プロバイダーの構成のプロパティ シートを表示するための十分な情報を取得するためにはサービス プロバイダーのエントリ ポイント関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="e08e6-105">Defines a service provider entry point function which the Profile Wizard calls to retrieve enough information to display the provider's configuration property sheets.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e08e6-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e08e6-106">Header file:</span></span>  <br/> |<span data-ttu-id="e08e6-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="e08e6-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="e08e6-108">によって実装される関数の定義:</span><span class="sxs-lookup"><span data-stu-id="e08e6-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="e08e6-109">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e08e6-109">Service providers</span></span>  <br/> |
|<span data-ttu-id="e08e6-110">によって呼び出される関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="e08e6-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="e08e6-111">MAPI プロファイル ウィザード</span><span class="sxs-lookup"><span data-stu-id="e08e6-111">MAPI Profile Wizard</span></span>  <br/> |
   
```cpp
ULONG WIZARDENTRY(
  HINSTANCE hProviderDLLInstance,
  LPSTR FAR * lpcsResourceName,
  DLGPROC FAR * lppDlgProc,
  LPMAPIPROP lpMAPIProp,
  LPMAPISUPPORTOBJECT lpMapiSupportObject
);
```

## <a name="parameters"></a><span data-ttu-id="e08e6-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e08e6-112">Parameters</span></span>

 <span data-ttu-id="e08e6-113">_hProviderDLLInstance_</span><span class="sxs-lookup"><span data-stu-id="e08e6-113">_hProviderDLLInstance_</span></span>
  
> <span data-ttu-id="e08e6-114">[in]サービス プロバイダーの DLL のインスタンス ハンドルです。</span><span class="sxs-lookup"><span data-stu-id="e08e6-114">[in] Instance handle of the service provider's DLL.</span></span> 
    
 <span data-ttu-id="e08e6-115">_lpcsResourceName_</span><span class="sxs-lookup"><span data-stu-id="e08e6-115">_lpcsResourceName_</span></span>
  
> <span data-ttu-id="e08e6-116">[out]構成中にプロファイル ウィザードによって表示されるダイアログ リソースの完全名を含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e08e6-116">[out] Pointer to a string that contains the full name of the dialog resource that should be displayed by the Profile Wizard during configuration.</span></span> <span data-ttu-id="e08e6-117">NULL 終端文字を含む、文字列の最大サイズは、32 文字です。</span><span class="sxs-lookup"><span data-stu-id="e08e6-117">The maximum size of the string, including the NULL terminator, is 32 characters.</span></span> 
    
 <span data-ttu-id="e08e6-118">_lppDlgProc_</span><span class="sxs-lookup"><span data-stu-id="e08e6-118">_lppDlgProc_</span></span>
  
> <span data-ttu-id="e08e6-119">[out]標準的な Windows ダイアログ ボックス プロシージャのさまざまなイベント プロバイダーに通知するためにプロファイル ウィザードによって呼び出されるへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e08e6-119">[out] Pointer to a standard Windows dialog box procedure that will be called by the Profile Wizard to notify the provider of various events.</span></span> 
    
 <span data-ttu-id="e08e6-120">_lpMAPIProp_</span><span class="sxs-lookup"><span data-stu-id="e08e6-120">_lpMAPIProp_</span></span>
  
> <span data-ttu-id="e08e6-121">[in]構成プロパティへのアクセスを提供するプロパティのインターフェイス実装へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e08e6-121">[in] Pointer to a property interface implementation that provides access to the configuration properties.</span></span> 
    
 <span data-ttu-id="e08e6-122">_lpMapiSupportObject_</span><span class="sxs-lookup"><span data-stu-id="e08e6-122">_lpMapiSupportObject_</span></span>
  
> <span data-ttu-id="e08e6-123">[in]このセッションに適用可能な MAPI のサポートのオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e08e6-123">[in] Pointer to the MAPI support object applicable to this session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e08e6-124">�߂�l</span><span class="sxs-lookup"><span data-stu-id="e08e6-124">Return value</span></span>

<span data-ttu-id="e08e6-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="e08e6-125">S_OK</span></span> 
  
> <span data-ttu-id="e08e6-126">サービス プロバイダーの**WIZARDENTRY**関数は正常に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e08e6-126">The service provider's **WIZARDENTRY** function was called successfully.</span></span> 
    
<span data-ttu-id="e08e6-127">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="e08e6-127">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="e08e6-128">予期しない、または不明な発生元のエラーでは、操作を完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="e08e6-128">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e08e6-129">注釈</span><span class="sxs-lookup"><span data-stu-id="e08e6-129">Remarks</span></span>

<span data-ttu-id="e08e6-130">プロファイル ウィザードは、サービス プロバイダーの構成のユーザー インターフェイスを表示する準備ができたときに、ベースの**WIZARDENTRY**関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e08e6-130">The Profile Wizard calls the **WIZARDENTRY** based function when it is ready to display the service provider's configuration user interface.</span></span> <span data-ttu-id="e08e6-131">プロファイル ウィザードがすべてのプロバイダーの構成が完了すると、 [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)を呼び出すことによって、プロファイルに構成プロパティを書き込みます。</span><span class="sxs-lookup"><span data-stu-id="e08e6-131">When the Profile Wizard is finished configuring all providers, it writes the configuration properties to the profile by calling [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e08e6-132">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="e08e6-132">Notes to implementers</span></span>

<span data-ttu-id="e08e6-133">MAPISVC.INF の WIZARD_ENTRY_NAME エントリでは、 **WIZARDENTRY**ベースの関数の名前を配置しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="e08e6-133">The name of the **WIZARDENTRY** based function must be placed in the WIZARD_ENTRY_NAME entry in MAPISVC.INF.</span></span> 
  
<span data-ttu-id="e08e6-134">ダイアログ リソースのある描画されること、プロファイル ウィザードのウィンドウで、リソースの名前です。</span><span class="sxs-lookup"><span data-stu-id="e08e6-134">The resource name is that of the dialog resource that will be rendered in the pane of the Profile Wizard.</span></span> <span data-ttu-id="e08e6-135">バックさせる必要があります 1 つのダイアログ リソースのすべてのページに渡されるリソースです。</span><span class="sxs-lookup"><span data-stu-id="e08e6-135">The resource that is passed back needs to contain all the pages in a single dialog resource.</span></span> <span data-ttu-id="e08e6-136">プロファイル ウィザードでは、このリソースを受信すると無視して、ダイアログのスタイルが、コントロール スタイルではありませんし、プロファイル ウィザードのページの子として、すべてのコントロールを作成します。</span><span class="sxs-lookup"><span data-stu-id="e08e6-136">When the Profile Wizard receives this resource, it ignores the dialog style, but not the control styles, and creates all the controls as children of the Profile Wizard page.</span></span> <span data-ttu-id="e08e6-137">すべてのコントロールが最初に表示されません。</span><span class="sxs-lookup"><span data-stu-id="e08e6-137">All controls are initially hidden.</span></span> <span data-ttu-id="e08e6-138">プロバイダーは、コントロールの座標が 0 であることを確認または 0 から始まる、する必要があり、それらを超えない 200 のダイアログ単位の最大の幅と高さの最大値] ダイアログが 150 単位の。</span><span class="sxs-lookup"><span data-stu-id="e08e6-138">Providers should make sure that the coordinates for their controls are zero or zero-based, and that they do not exceed a maximum width of 200 dialog units and a maximum height of 150 dialog units.</span></span> <span data-ttu-id="e08e6-139">400 の下のコントロール id は、プロファイル ウィザードの予約されています。</span><span class="sxs-lookup"><span data-stu-id="e08e6-139">Control identifiers below 400 are reserved for the Profile Wizard.</span></span> <span data-ttu-id="e08e6-140">プロファイル ウィザードでは、プロバイダーのユーザー ・ インタ フェース上の太字のテキストで、プロバイダーのタイトルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e08e6-140">The Profile Wizard displays the provider's title in bold text above the provider's user interface.</span></span> 
  
<span data-ttu-id="e08e6-141">_LpMAPIProp_パラメーターで指定されたプロパティのインターフェイス ポインターは、将来参照できるように、プロバイダーが保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e08e6-141">The property interface pointer supplied in the  _lpMAPIProp_ parameter should be retained by the provider for future reference.</span></span> <span data-ttu-id="e08e6-142">プロファイル ウィザードが最も基本的なプロパティのセットだけを扱うし、プロバイダーは、プロパティのインターフェイスの実装を使用して、追加のプロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="e08e6-142">The Profile Wizard deals with only the most basic set of properties, and the provider can use the property interface implementation to include additional properties.</span></span> <span data-ttu-id="e08e6-143">コンフィギュレーションでは、プロバイダーは、プロパティのインターフェイスを実装するオブジェクトへの設定のプロパティを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e08e6-143">During configuration, providers should add their configuration properties to the object implementing the property interface.</span></span> <span data-ttu-id="e08e6-144">すべてのプロバイダーを構成すると、プロファイル ウィザードはこれらのプロパティをプロファイルに追加します。</span><span class="sxs-lookup"><span data-stu-id="e08e6-144">After all providers have been configured, the Profile Wizard adds these properties to the profile.</span></span> 
  
<span data-ttu-id="e08e6-145">この関数を使用する方法の詳細については、[メッセージ サービスの構成のサポート](supporting-message-service-configuration.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e08e6-145">For more information about how to use this function, see [Supporting Message Service Configuration](supporting-message-service-configuration.md).</span></span> 
  

