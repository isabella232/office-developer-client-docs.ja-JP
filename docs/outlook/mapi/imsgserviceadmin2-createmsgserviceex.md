---
title: IMsgServiceAdmin2CreateMsgServiceEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin2.CreateMsgServiceEx
api_type:
- COM
ms.assetid: 4910dabd-9380-4fde-a440-5c64d74c0bba
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b7fe25491228f00f6865af963db36f27bae5d7a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410183"
---
# <a name="imsgserviceadmin2createmsgserviceex"></a><span data-ttu-id="4cce0-103">IMsgServiceAdmin2::CreateMsgServiceEx</span><span class="sxs-lookup"><span data-stu-id="4cce0-103">IMsgServiceAdmin2::CreateMsgServiceEx</span></span>

  
  
<span data-ttu-id="4cce0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4cce0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4cce0-105">メッセージ サービスを現在のプロファイルに追加し、新しく追加されたサービス UID を返します。</span><span class="sxs-lookup"><span data-stu-id="4cce0-105">Adds a message service to the current profile and returns that newly added service UID.</span></span>
  
```cpp
HRESULT CreateMsgServiceEx(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,    
  LPMAPIUID lpuidService
);
```

## <a name="parameters"></a><span data-ttu-id="4cce0-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4cce0-106">Parameters</span></span>

 <span data-ttu-id="4cce0-107">_lpszService_</span><span class="sxs-lookup"><span data-stu-id="4cce0-107">_lpszService_</span></span>
  
> <span data-ttu-id="4cce0-108">[in]追加するメッセージ サービスの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4cce0-108">[in] A pointer to the name of the message service to add.</span></span> <span data-ttu-id="4cce0-109">このメッセージ サービス名は、MapiSvc.inf ファイル **の [Services]** セクションに表示される必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cce0-109">This message service name must appear in the **[Services]** section of the MapiSvc.inf file.</span></span> 
    
 <span data-ttu-id="4cce0-110">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="4cce0-110">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="4cce0-111">[in]追加するメッセージ サービスの表示名へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4cce0-111">[in] A pointer to the display name of the message service to add.</span></span> <span data-ttu-id="4cce0-112">メッセージ サービスが MapiSvc.inf ファイルの PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティを設定している場合 _、lpszDisplayName_ パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="4cce0-112">The  _lpszDisplayName_ parameter is ignored if the message service has set the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MapiSvc.inf file.</span></span>
    
 <span data-ttu-id="4cce0-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="4cce0-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="4cce0-114">[in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="4cce0-114">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="4cce0-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4cce0-115">_ulFlags_</span></span>
  
> <span data-ttu-id="4cce0-116">[in]メッセージ サービスのインストール方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="4cce0-116">[in] A bitmask of flags that controls how the message service is installed.</span></span> <span data-ttu-id="4cce0-117">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="4cce0-117">The following flags can be set:</span></span>
    
<span data-ttu-id="4cce0-118">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4cce0-118">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="4cce0-119">lpszService パラメーターと lpszDisplayName パラメーターを LPWSTR にキャストし、Unicode 文字列として解釈する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cce0-119">The lpszService and the lpszDisplayName parameters should be cast to LPWSTR and interpreted as Unicode strings.</span></span>
    
<span data-ttu-id="4cce0-120">SERVICE_NO_RESTART_WARNING</span><span class="sxs-lookup"><span data-stu-id="4cce0-120">SERVICE_NO_RESTART_WARNING</span></span>
  
> <span data-ttu-id="4cce0-121">プロファイルに新しいメッセージ サービスを追加する場合、MAPI サブシステムは、さまざまな状況と条件に基づいて、多くの場合、このアクションでプロファイルの再起動が必要Outlook。</span><span class="sxs-lookup"><span data-stu-id="4cce0-121">When adding a new message service to the profile, the MAPI subsystem, based on various circumstances and criteria, often determines that this action requires a restart of Outlook.</span></span> <span data-ttu-id="4cce0-122">SERVICE_NO_RESTART_WARNING フラグが含まれていない場合に、SERVICE_UI_ALWAYS フラグと SERVICE_UI_ALLOWED フラグに基づいて UI が許可され、少なくとも 1 つのプロセスが現在のプロファイルにログオンしている場合、この関数は「これらの変更を有効にするために Outlook を再起動する必要があります」というメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="4cce0-122">If the SERVICE_NO_RESTART_WARNING flag is not included and UI is allowed - based on the SERVICE_UI_ALWAYS and SERVICE_UI_ALLOWED flags - and at least one process is logged onto the current profile, this function displays the message "You must restart Outlook for these changes to take effect."</span></span> <span data-ttu-id="4cce0-123">フラグをSERVICE_NO_RESTART_WARNINGすると、その警告メッセージの表示が抑制されます。</span><span class="sxs-lookup"><span data-stu-id="4cce0-123">Including the SERVICE_NO_RESTART_WARNING flag suppresses the display of that warning message.</span></span>
    
<span data-ttu-id="4cce0-124">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="4cce0-124">SERVICE_UI_ALLOWED</span></span>
  
> <span data-ttu-id="4cce0-125">必要に応じて、メッセージ サービス構成 UI を使用できます。</span><span class="sxs-lookup"><span data-stu-id="4cce0-125">The message service configuration UI is allowed if needed.</span></span>
    
<span data-ttu-id="4cce0-126">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="4cce0-126">SERVICE_UI_ALWAYS</span></span>
  
> <span data-ttu-id="4cce0-127">メッセージ サービスは、構成プロパティ シートを表示します。</span><span class="sxs-lookup"><span data-stu-id="4cce0-127">The message service displays its configuration property sheet.</span></span>
    
 <span data-ttu-id="4cce0-128">_lpuidService_</span><span class="sxs-lookup"><span data-stu-id="4cce0-128">_lpuidService_</span></span>
  
> <span data-ttu-id="4cce0-129">[out]追加されたメッセージ サービスの UID へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4cce0-129">[out] The pointer to the UID of the message service added.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4cce0-130">戻り値</span><span class="sxs-lookup"><span data-stu-id="4cce0-130">Return value</span></span>

<span data-ttu-id="4cce0-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="4cce0-131">S_OK</span></span>
  
> <span data-ttu-id="4cce0-132">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="4cce0-132">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="4cce0-133">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="4cce0-133">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="4cce0-134">メッセージ サービス名は MapiSvc.inf の **[Services]** セクションに含めではありません。</span><span class="sxs-lookup"><span data-stu-id="4cce0-134">The message service name is not in the **[Services]** section of MapiSvc.inf.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4cce0-135">注釈</span><span class="sxs-lookup"><span data-stu-id="4cce0-135">Remarks</span></span>

<span data-ttu-id="4cce0-136">**IMsgServiceAdmin2::CreateMsgServiceEx** メソッドは、現在のプロファイルにメッセージ サービスを追加します。</span><span class="sxs-lookup"><span data-stu-id="4cce0-136">The **IMsgServiceAdmin2::CreateMsgServiceEx** method adds a message service to the current profile.</span></span> <span data-ttu-id="4cce0-137">**CreateMsgServiceEx は** 、メッセージ サービスのエントリ ポイント関数を呼び出して、サービス固有の構成タスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="4cce0-137">**CreateMsgServiceEx** calls the message service's entry point function to perform any service-specific configuration tasks.</span></span> <span data-ttu-id="4cce0-138">_ulFlags_ パラメーター SERVICE_UI_ALLOWEDフラグが設定されている場合、インストール中のメッセージ サービスにプロパティ シートを表示して、ユーザーが設定を構成できます。</span><span class="sxs-lookup"><span data-stu-id="4cce0-138">If the SERVICE_UI_ALLOWED flag is set in the  _ulFlags_ parameter, the message service being installed can display a property sheet enabling the user to configure its settings.</span></span> 
  
<span data-ttu-id="4cce0-139">MapiSvc.inf ファイルには、メッセージ サービスを構成するプロバイダーの一覧と、それぞれのプロパティが含まれる。</span><span class="sxs-lookup"><span data-stu-id="4cce0-139">The MapiSvc.inf file contains the list of providers that make up a message service and the properties for each.</span></span> <span data-ttu-id="4cce0-140">**CreateMsgServiceEx** は、まずメッセージ サービスの新しいプロファイル セクションを作成し、そのサービスのすべての情報を MapiSvc.inf ファイルからプロファイルにコピーし、プロバイダーごとに新しいセクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="4cce0-140">**CreateMsgServiceEx** first creates a new profile section for the message service and then copies all of the information for that service from the MapiSvc.inf file into the profile, creating new sections for each provider.</span></span> 
  
<span data-ttu-id="4cce0-141">MapiSvc.inf からすべての情報がコピーされた後、メッセージ サービスのエントリ ポイント関数 **MSGSERVICEENTRY** が  _ulContext_ パラメーターに設定された MSG_SERVICE_CREATE 値で呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4cce0-141">After all the information has been copied from MapiSvc.inf, the message service's entry point function, **MSGSERVICEENTRY**, is called with the MSG_SERVICE_CREATE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="4cce0-142">**CreateMsgServiceEx** メソッドの _ulFlags_ パラメーターで SERVICE_UI_ALLOWED フラグが設定されている場合、メッセージ サービスのエントリ ポイント関数が呼び出された場合 _、ulUIParam_ パラメーターと _ulFlags_ パラメーターの値も渡されます。</span><span class="sxs-lookup"><span data-stu-id="4cce0-142">If the SERVICE_UI_ALLOWED flag is set in the **CreateMsgServiceEx** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed when the message service's entry point function is called.</span></span> <span data-ttu-id="4cce0-143">サービス プロバイダーは、ユーザーがメッセージ サービスを構成できるよう、構成プロパティ シートを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cce0-143">Service providers should display their configuration property sheets so users can configure the message service.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4cce0-144">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="4cce0-144">Notes to callers</span></span>

<span data-ttu-id="4cce0-145">引数 **CreateMsgServiceEx** _lpuidService_ が NULL ではない場合、プロファイルに追加されたメッセージ サービスの **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) プロパティが、そのプロファイルがポイントする **GUID** に返されます。</span><span class="sxs-lookup"><span data-stu-id="4cce0-145">If the **CreateMsgServiceEx** _lpuidService_ argument is not NULL, the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property of the message service that was added to the profile is returned in the **GUID** to which it points.</span></span> 
  
<span data-ttu-id="4cce0-146">_lpuidService_ **パラメーターの PR_SERVICE_UID** プロパティの値を [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)メソッドに渡して、サービスを構成します。</span><span class="sxs-lookup"><span data-stu-id="4cce0-146">Pass the value of the **PR_SERVICE_UID** property in the  _lpuidService_ parameter to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method to configure the service.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="4cce0-147">MAPI Microsoft Outlook 2010の実装では、MAPI サブシステムMAPI_UNICODEサポートされません。使用すると失敗します。</span><span class="sxs-lookup"><span data-stu-id="4cce0-147">The Microsoft Outlook 2010 implementation of the MAPI subsystem does not support MAPI_UNICODE and will fail if it is used.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="4cce0-148">IMsgServiceAdmin2 インターフェイスは、IMsgServiceAdmin インターフェイスを実装するオブジェクトと同じオブジェクトによって公開され、Outlook の MAPI サブシステムの実装を 2003 年から使用Outlookされています。</span><span class="sxs-lookup"><span data-stu-id="4cce0-148">The IMsgServiceAdmin2 interface is exposed by the same object that implements the IMsgServiceAdmin interface, and has been available using Outlook's implementation of the MAPI subsystem since Outlook 2003.</span></span> <span data-ttu-id="4cce0-149">その IID は次のように定義されます:> `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)` >   `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> _ulFlags_ SERVICE_NO_RESTART_WARNING は、現在使用しているダウンロード可能なヘッダー ファイルで定義されていない可能性があります。その場合は、次の値を使用してコードに追加できます。>`#define SERVICE_NO_RESTART_WARNING 0x00000080`</span><span class="sxs-lookup"><span data-stu-id="4cce0-149">Its IID is defined as follows: >  `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)`>  `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> The  _ulFlags_ SERVICE_NO_RESTART_WARNING might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define SERVICE_NO_RESTART_WARNING 0x00000080`</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4cce0-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="4cce0-150">See also</span></span>



[<span data-ttu-id="4cce0-151">IMsgServiceAdmin2 : IMsgServiceAdmin</span><span class="sxs-lookup"><span data-stu-id="4cce0-151">IMsgServiceAdmin2 : IMsgServiceAdmin</span></span>](imsgserviceadmin2imsgserviceadmin.md)


<span data-ttu-id="4cce0-152">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="4cce0-152">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

