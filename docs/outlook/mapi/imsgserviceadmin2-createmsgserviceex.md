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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f700389315ca7bd184a9d6defb0b44eaec99a38e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574777"
---
# <a name="imsgserviceadmin2createmsgserviceex"></a><span data-ttu-id="6335b-103">IMsgServiceAdmin2::CreateMsgServiceEx</span><span class="sxs-lookup"><span data-stu-id="6335b-103">IMsgServiceAdmin2::CreateMsgServiceEx</span></span>

  
  
<span data-ttu-id="6335b-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6335b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6335b-105">サービス UID を新しく追加すること、現在のプロファイルには、メッセージ サービスを追加します。</span><span class="sxs-lookup"><span data-stu-id="6335b-105">Adds a message service to the current profile and returns that newly added service UID.</span></span>
  
```cpp
HRESULT CreateMsgServiceEx(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,    
  LPMAPIUID lpuidService
);
```

## <a name="parameters"></a><span data-ttu-id="6335b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6335b-106">Parameters</span></span>

 <span data-ttu-id="6335b-107">_lpszService_</span><span class="sxs-lookup"><span data-stu-id="6335b-107">_lpszService_</span></span>
  
> <span data-ttu-id="6335b-108">[in]追加するのにはメッセージ サービスの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6335b-108">[in] A pointer to the name of the message service to add.</span></span> <span data-ttu-id="6335b-109">MapiSvc.inf ファイルの **[サービス]** セクションで、このメッセージのサービス名があります。</span><span class="sxs-lookup"><span data-stu-id="6335b-109">This message service name must appear in the **[Services]** section of the MapiSvc.inf file.</span></span> 
    
 <span data-ttu-id="6335b-110">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="6335b-110">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="6335b-111">[in]追加するのにはメッセージ サービスの表示名へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6335b-111">[in] A pointer to the display name of the message service to add.</span></span> <span data-ttu-id="6335b-112">メッセージ サービスが、MapiSvc.inf ファイルの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) のプロパティを設定されている場合、 _lpszDisplayName_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="6335b-112">The  _lpszDisplayName_ parameter is ignored if the message service has set the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MapiSvc.inf file.</span></span>
    
 <span data-ttu-id="6335b-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="6335b-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="6335b-114">[in]ダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドルを表示します。</span><span class="sxs-lookup"><span data-stu-id="6335b-114">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="6335b-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6335b-115">_ulFlags_</span></span>
  
> <span data-ttu-id="6335b-116">[in]メッセージ サービスをインストールする方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="6335b-116">[in] A bitmask of flags that controls how the message service is installed.</span></span> <span data-ttu-id="6335b-117">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="6335b-117">The following flags can be set:</span></span>
    
<span data-ttu-id="6335b-118">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6335b-118">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="6335b-119">LpszService および lpszDisplayName パラメーターを LPWSTR にキャストし、Unicode 文字列として解釈する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6335b-119">The lpszService and the lpszDisplayName parameters should be cast to LPWSTR and interpreted as Unicode strings.</span></span>
    
<span data-ttu-id="6335b-120">SERVICE_NO_RESTART_WARNING</span><span class="sxs-lookup"><span data-stu-id="6335b-120">SERVICE_NO_RESTART_WARNING</span></span>
  
> <span data-ttu-id="6335b-121">新しいメッセージ サービスをプロファイルに追加するときに多くの場合さまざまな状況や条件に基づき、MAPI サブシステムがアクションには、Outlook の再起動が必要ですを決定します。</span><span class="sxs-lookup"><span data-stu-id="6335b-121">When adding a new message service to the profile, the MAPI subsystem, based on various circumstances and criteria, often determines that this action requires a restart of Outlook.</span></span> <span data-ttu-id="6335b-122">SERVICE_NO_RESTART_WARNING フラグが含まれていない UI を使用すると-- SERVICE_UI_ALWAYS と SERVICE_UI_ALLOWED のフラグに基づくし、少なくとも 1 つのプロセスは、現在のプロファイルにログオンしている、この関数、メッセージが表示"する必要があります Outlook を再起動これらの変更を有効にする。」</span><span class="sxs-lookup"><span data-stu-id="6335b-122">If the SERVICE_NO_RESTART_WARNING flag is not included and UI is allowed - based on the SERVICE_UI_ALWAYS and SERVICE_UI_ALLOWED flags - and at least one process is logged onto the current profile, this function displays the message "You must restart Outlook for these changes to take effect."</span></span> <span data-ttu-id="6335b-123">SERVICE_NO_RESTART_WARNING フラグを含む、警告メッセージの表示を抑制します。</span><span class="sxs-lookup"><span data-stu-id="6335b-123">Including the SERVICE_NO_RESTART_WARNING flag suppresses the display of that warning message.</span></span>
    
<span data-ttu-id="6335b-124">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="6335b-124">SERVICE_UI_ALLOWED</span></span>
  
> <span data-ttu-id="6335b-125">メッセージ サービスの構成が必要な場合、UI は許可されています。</span><span class="sxs-lookup"><span data-stu-id="6335b-125">The message service configuration UI is allowed if needed.</span></span>
    
<span data-ttu-id="6335b-126">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="6335b-126">SERVICE_UI_ALWAYS</span></span>
  
> <span data-ttu-id="6335b-127">メッセージ サービスでは、[設定] プロパティ シートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6335b-127">The message service displays its configuration property sheet.</span></span>
    
 <span data-ttu-id="6335b-128">_lpuidService_</span><span class="sxs-lookup"><span data-stu-id="6335b-128">_lpuidService_</span></span>
  
> <span data-ttu-id="6335b-129">[out]追加メッセージ サービスの UID へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6335b-129">[out] The pointer to the UID of the message service added.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6335b-130">�߂�l</span><span class="sxs-lookup"><span data-stu-id="6335b-130">Return value</span></span>

<span data-ttu-id="6335b-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="6335b-131">S_OK</span></span>
  
> <span data-ttu-id="6335b-132">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="6335b-132">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="6335b-133">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="6335b-133">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="6335b-134">メッセージ サービス名は、MapiSvc.inf の **[サービス]** セクションではありません。</span><span class="sxs-lookup"><span data-stu-id="6335b-134">The message service name is not in the **[Services]** section of MapiSvc.inf.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6335b-135">注釈</span><span class="sxs-lookup"><span data-stu-id="6335b-135">Remarks</span></span>

<span data-ttu-id="6335b-136">**IMsgServiceAdmin2::CreateMsgServiceEx**メソッドは、メッセージ サービスを現在のプロファイルに追加します。</span><span class="sxs-lookup"><span data-stu-id="6335b-136">The **IMsgServiceAdmin2::CreateMsgServiceEx** method adds a message service to the current profile.</span></span> <span data-ttu-id="6335b-137">**CreateMsgServiceEx**は、サービス固有の構成タスクを実行するのには、メッセージ サービスのエントリ ポイント関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6335b-137">**CreateMsgServiceEx** calls the message service's entry point function to perform any service-specific configuration tasks.</span></span> <span data-ttu-id="6335b-138">_UlFlags_パラメーターに SERVICE_UI_ALLOWED フラグを設定すると、メッセージ サービスがインストールされているがその設定を構成するユーザーを有効にすると、プロパティ シートを表示できます。</span><span class="sxs-lookup"><span data-stu-id="6335b-138">If the SERVICE_UI_ALLOWED flag is set in the  _ulFlags_ parameter, the message service being installed can display a property sheet enabling the user to configure its settings.</span></span> 
  
<span data-ttu-id="6335b-139">MapiSvc.inf ファイルには、それぞれのメッセージ サービスとプロパティを構成するプロバイダーの一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6335b-139">The MapiSvc.inf file contains the list of providers that make up a message service and the properties for each.</span></span> <span data-ttu-id="6335b-140">**CreateMsgServiceEx**は、まずメッセージ サービス用の新しいプロファイル セクションを作成し、そのサービスの情報をすべて MapiSvc.inf ファイルからにコピー、プロファイルでは、プロバイダーごとに新しいセクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="6335b-140">**CreateMsgServiceEx** first creates a new profile section for the message service and then copies all of the information for that service from the MapiSvc.inf file into the profile, creating new sections for each provider.</span></span> 
  
<span data-ttu-id="6335b-141">MapiSvc.inf からすべての情報がコピーされた後は、 _ulContext_パラメーターに設定された MSG_SERVICE_CREATE 値を持つメッセージ サービスのエントリ ポイント関数、 **MSGSERVICEENTRY**が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6335b-141">After all the information has been copied from MapiSvc.inf, the message service's entry point function, **MSGSERVICEENTRY**, is called with the MSG_SERVICE_CREATE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="6335b-142">**CreateMsgServiceEx**メソッドの_ulFlags_パラメーターに SERVICE_UI_ALLOWED フラグを設定すると、またには、 _ulUIParam_と_ulFlags_パラメーターの値は、メッセージ サービスのエントリ ポイント関数が呼び出されたときに渡されます。</span><span class="sxs-lookup"><span data-stu-id="6335b-142">If the SERVICE_UI_ALLOWED flag is set in the **CreateMsgServiceEx** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed when the message service's entry point function is called.</span></span> <span data-ttu-id="6335b-143">サービス プロバイダーは、ユーザーは、メッセージ サービスを構成することができますので、構成のプロパティ シートを表示します。</span><span class="sxs-lookup"><span data-stu-id="6335b-143">Service providers should display their configuration property sheets so users can configure the message service.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6335b-144">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="6335b-144">Notes to callers</span></span>

<span data-ttu-id="6335b-145">**CreateMsgServiceEx** _lpuidService_の引数が NULL でない場合は、 **GUID**の指し示す先のプロファイルに追加されたメッセージ サービスの**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) プロパティが返されます。</span><span class="sxs-lookup"><span data-stu-id="6335b-145">If the **CreateMsgServiceEx** _lpuidService_ argument is not NULL, the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property of the message service that was added to the profile is returned in the **GUID** to which it points.</span></span> 
  
<span data-ttu-id="6335b-146">**PR_SERVICE_UID**プロパティの値を_lpuidService_パラメーターでメソッドに渡す、 [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)サービスを構成します。</span><span class="sxs-lookup"><span data-stu-id="6335b-146">Pass the value of the **PR_SERVICE_UID** property in the  _lpuidService_ parameter to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method to configure the service.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="6335b-147">MAPI サブシステムの Microsoft Outlook 2010 の実装は、MAPI_UNICODE をサポートしていませんし、使用されている場合は失敗します。</span><span class="sxs-lookup"><span data-stu-id="6335b-147">The Microsoft Outlook 2010 implementation of the MAPI subsystem does not support MAPI_UNICODE and will fail if it is used.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="6335b-148">IMsgServiceAdmin2 インターフェイスは、IMsgServiceAdmin インターフェイスを実装して、MAPI サブシステムの Outlook 2003 以降の Outlook の実装を使用して提供されている同じオブジェクトによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="6335b-148">The IMsgServiceAdmin2 interface is exposed by the same object that implements the IMsgServiceAdmin interface, and has been available using Outlook's implementation of the MAPI subsystem since Outlook 2003.</span></span> <span data-ttu-id="6335b-149">インターフェイスの IID は、次のように定義されている: > `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)` >   `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> _ulFlags_ SERVICE_NO_RESTART_WARNING は、現在あるダウンロード可能なヘッダー ファイルで定義されていない可能性があります、場合に追加できます、次の値を使用してコード: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`</span><span class="sxs-lookup"><span data-stu-id="6335b-149">Its IID is defined as follows: >  `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)`>  `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> The  _ulFlags_ SERVICE_NO_RESTART_WARNING might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define SERVICE_NO_RESTART_WARNING 0x00000080`</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6335b-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="6335b-150">See also</span></span>



[<span data-ttu-id="6335b-151">IMsgServiceAdmin2 : IMsgServiceAdmin</span><span class="sxs-lookup"><span data-stu-id="6335b-151">IMsgServiceAdmin2 : IMsgServiceAdmin</span></span>](imsgserviceadmin2imsgserviceadmin.md)


<span data-ttu-id="6335b-152">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="6335b-152">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

