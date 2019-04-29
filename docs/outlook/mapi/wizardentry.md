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
# <a name="wizardentry"></a><span data-ttu-id="95430-103">WIZARDENTRY</span><span class="sxs-lookup"><span data-stu-id="95430-103">WIZARDENTRY</span></span>

  
  
<span data-ttu-id="95430-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95430-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95430-105">プロバイダーの構成プロパティシートを表示するのに十分な情報を取得するために、プロファイルウィザードが呼び出すサービスプロバイダーエントリポイント関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="95430-105">Defines a service provider entry point function which the Profile Wizard calls to retrieve enough information to display the provider's configuration property sheets.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="95430-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="95430-106">Header file:</span></span>  <br/> |<span data-ttu-id="95430-107">Mapiwz</span><span class="sxs-lookup"><span data-stu-id="95430-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="95430-108">定義された関数の実装:</span><span class="sxs-lookup"><span data-stu-id="95430-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="95430-109">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="95430-109">Service providers</span></span>  <br/> |
|<span data-ttu-id="95430-110">によって呼び出された定義済み関数:</span><span class="sxs-lookup"><span data-stu-id="95430-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="95430-111">MAPI プロファイルウィザード</span><span class="sxs-lookup"><span data-stu-id="95430-111">MAPI Profile Wizard</span></span>  <br/> |
   
```cpp
ULONG WIZARDENTRY(
  HINSTANCE hProviderDLLInstance,
  LPSTR FAR * lpcsResourceName,
  DLGPROC FAR * lppDlgProc,
  LPMAPIPROP lpMAPIProp,
  LPMAPISUPPORTOBJECT lpMapiSupportObject
);
```

## <a name="parameters"></a><span data-ttu-id="95430-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="95430-112">Parameters</span></span>

 <span data-ttu-id="95430-113">_hproviderdllinstance_</span><span class="sxs-lookup"><span data-stu-id="95430-113">_hProviderDLLInstance_</span></span>
  
> <span data-ttu-id="95430-114">順番サービスプロバイダーの DLL のインスタンスハンドル。</span><span class="sxs-lookup"><span data-stu-id="95430-114">[in] Instance handle of the service provider's DLL.</span></span> 
    
 <span data-ttu-id="95430-115">_lpcsResourceName_</span><span class="sxs-lookup"><span data-stu-id="95430-115">_lpcsResourceName_</span></span>
  
> <span data-ttu-id="95430-116">読み上げ構成中にプロファイルウィザードによって表示されるダイアログリソースの完全な名前を含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="95430-116">[out] Pointer to a string that contains the full name of the dialog resource that should be displayed by the Profile Wizard during configuration.</span></span> <span data-ttu-id="95430-117">NULL ターミネータを含む文字列の最大サイズは、32文字です。</span><span class="sxs-lookup"><span data-stu-id="95430-117">The maximum size of the string, including the NULL terminator, is 32 characters.</span></span> 
    
 <span data-ttu-id="95430-118">_lppdlgproc_</span><span class="sxs-lookup"><span data-stu-id="95430-118">_lppDlgProc_</span></span>
  
> <span data-ttu-id="95430-119">読み上げプロファイルウィザードによって呼び出され、さまざまなイベントをプロバイダーに通知する標準の Windows ダイアログボックスプロシージャへのポインター。</span><span class="sxs-lookup"><span data-stu-id="95430-119">[out] Pointer to a standard Windows dialog box procedure that will be called by the Profile Wizard to notify the provider of various events.</span></span> 
    
 <span data-ttu-id="95430-120">_lpMAPIProp_</span><span class="sxs-lookup"><span data-stu-id="95430-120">_lpMAPIProp_</span></span>
  
> <span data-ttu-id="95430-121">順番構成プロパティへのアクセスを提供するプロパティインターフェイス実装へのポインター。</span><span class="sxs-lookup"><span data-stu-id="95430-121">[in] Pointer to a property interface implementation that provides access to the configuration properties.</span></span> 
    
 <span data-ttu-id="95430-122">_lpMapiSupportObject_</span><span class="sxs-lookup"><span data-stu-id="95430-122">_lpMapiSupportObject_</span></span>
  
> <span data-ttu-id="95430-123">順番このセッションに適用される MAPI サポートオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="95430-123">[in] Pointer to the MAPI support object applicable to this session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="95430-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="95430-124">Return value</span></span>

<span data-ttu-id="95430-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="95430-125">S_OK</span></span> 
  
> <span data-ttu-id="95430-126">サービスプロバイダーの**wizardentry**関数が正常に呼び出されました。</span><span class="sxs-lookup"><span data-stu-id="95430-126">The service provider's **WIZARDENTRY** function was called successfully.</span></span> 
    
<span data-ttu-id="95430-127">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="95430-127">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="95430-128">予期しないまたは不明な配信元のエラーにより、操作が完了しませんでした。</span><span class="sxs-lookup"><span data-stu-id="95430-128">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="95430-129">注釈</span><span class="sxs-lookup"><span data-stu-id="95430-129">Remarks</span></span>

<span data-ttu-id="95430-130">プロファイルウィザードは、サービスプロバイダーの構成ユーザーインターフェイスを表示する準備ができたときに、 **wizardentry**ベースの関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="95430-130">The Profile Wizard calls the **WIZARDENTRY** based function when it is ready to display the service provider's configuration user interface.</span></span> <span data-ttu-id="95430-131">すべてのプロバイダーの構成が完了すると、プロファイルウィザードは[IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)を呼び出して、プロファイルに構成プロパティを書き込みます。</span><span class="sxs-lookup"><span data-stu-id="95430-131">When the Profile Wizard is finished configuring all providers, it writes the configuration properties to the profile by calling [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="95430-132">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="95430-132">Notes to implementers</span></span>

<span data-ttu-id="95430-133">**wizardentry**に基づく関数の名前は、mapisvc.inf の WIZARD_ENTRY_NAME エントリに配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="95430-133">The name of the **WIZARDENTRY** based function must be placed in the WIZARD_ENTRY_NAME entry in MAPISVC.INF.</span></span> 
  
<span data-ttu-id="95430-134">リソース名は、プロファイルウィザードのウィンドウに表示されるダイアログリソースの名前です。</span><span class="sxs-lookup"><span data-stu-id="95430-134">The resource name is that of the dialog resource that will be rendered in the pane of the Profile Wizard.</span></span> <span data-ttu-id="95430-135">渡されるリソースには、1つのダイアログリソース内のすべてのページが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="95430-135">The resource that is passed back needs to contain all the pages in a single dialog resource.</span></span> <span data-ttu-id="95430-136">プロファイルウィザードがこのリソースを受け取ると、ダイアログスタイルは無視されますが、コントロールスタイルは無視され、すべてのコントロールがプロファイルウィザードページの子として作成されます。</span><span class="sxs-lookup"><span data-stu-id="95430-136">When the Profile Wizard receives this resource, it ignores the dialog style, but not the control styles, and creates all the controls as children of the Profile Wizard page.</span></span> <span data-ttu-id="95430-137">すべてのコントロールが最初に非表示になります。</span><span class="sxs-lookup"><span data-stu-id="95430-137">All controls are initially hidden.</span></span> <span data-ttu-id="95430-138">プロバイダーは、コントロールの座標が0またはゼロであること、および最大幅が200ダイアログ単位で、最大高さが150ダイアログ単位であることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="95430-138">Providers should make sure that the coordinates for their controls are zero or zero-based, and that they do not exceed a maximum width of 200 dialog units and a maximum height of 150 dialog units.</span></span> <span data-ttu-id="95430-139">400の下にあるコントロール id は、プロファイルウィザード用に予約されています。</span><span class="sxs-lookup"><span data-stu-id="95430-139">Control identifiers below 400 are reserved for the Profile Wizard.</span></span> <span data-ttu-id="95430-140">プロファイルウィザードは、プロバイダーのタイトルを、プロバイダーのユーザーインターフェイスの上に太字のテキストで表示します。</span><span class="sxs-lookup"><span data-stu-id="95430-140">The Profile Wizard displays the provider's title in bold text above the provider's user interface.</span></span> 
  
<span data-ttu-id="95430-141">_lpMAPIProp_パラメーターで指定されたプロパティインターフェイスポインターは、プロバイダーが後で参照できるように保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="95430-141">The property interface pointer supplied in the  _lpMAPIProp_ parameter should be retained by the provider for future reference.</span></span> <span data-ttu-id="95430-142">プロファイルウィザードは、最も基本的なプロパティのセットのみを処理し、プロバイダーはプロパティインターフェイスの実装を使用して、追加のプロパティを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="95430-142">The Profile Wizard deals with only the most basic set of properties, and the provider can use the property interface implementation to include additional properties.</span></span> <span data-ttu-id="95430-143">構成時に、プロバイダーは、プロパティインターフェイスを実装するオブジェクトに構成プロパティを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="95430-143">During configuration, providers should add their configuration properties to the object implementing the property interface.</span></span> <span data-ttu-id="95430-144">すべてのプロバイダーを構成した後、プロファイルウィザードによってこれらのプロパティがプロファイルに追加されます。</span><span class="sxs-lookup"><span data-stu-id="95430-144">After all providers have been configured, the Profile Wizard adds these properties to the profile.</span></span> 
  
<span data-ttu-id="95430-145">この関数の使用方法の詳細については、「[メッセージサービス構成のサポート](supporting-message-service-configuration.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="95430-145">For more information about how to use this function, see [Supporting Message Service Configuration](supporting-message-service-configuration.md).</span></span> 
  

