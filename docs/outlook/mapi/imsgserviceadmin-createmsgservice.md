---
title: IMsgServiceAdminCreateMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.CreateMsgService
api_type:
- COM
ms.assetid: 0135f049-0311-45e5-9685-78597d599a4e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7c649680d1d04e210ac4d90779e9a4e57aaab25a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579866"
---
# <a name="imsgserviceadmincreatemsgservice"></a><span data-ttu-id="1ecee-103">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="1ecee-103">IMsgServiceAdmin::CreateMsgService</span></span>

  
  
<span data-ttu-id="1ecee-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ecee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ecee-105">使用されなくなりました。 [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md)の使用をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="1ecee-105">Deprecated: The use of [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) is recommended.</span></span> <span data-ttu-id="1ecee-106">メッセージ サービスは、現在のプロファイルに追加します。</span><span class="sxs-lookup"><span data-stu-id="1ecee-106">Adds a message service to the current profile.</span></span> 
  
```cpp
HRESULT CreateMsgService(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags    
);
```

## <a name="parameters"></a><span data-ttu-id="1ecee-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1ecee-107">Parameters</span></span>

 <span data-ttu-id="1ecee-108">_lpszService_</span><span class="sxs-lookup"><span data-stu-id="1ecee-108">_lpszService_</span></span>
  
> <span data-ttu-id="1ecee-109">[in]追加するのにはメッセージ サービスの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1ecee-109">[in] A pointer to the name of the message service to add.</span></span> <span data-ttu-id="1ecee-110">MapiSvc.inf ファイルの **[サービス]** セクションで、このメッセージのサービス名があります。</span><span class="sxs-lookup"><span data-stu-id="1ecee-110">This message service name must appear in the **[Services]** section of the MapiSvc.inf file.</span></span> 
    
 <span data-ttu-id="1ecee-111">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="1ecee-111">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="1ecee-112">[in]追加するのにはメッセージ サービスの表示名へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1ecee-112">[in] A pointer to the display name of the message service to add.</span></span> <span data-ttu-id="1ecee-113">メッセージ サービスが、MapiSvc.inf ファイルの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) のプロパティを設定されている場合、 _lpszDisplayName_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="1ecee-113">The  _lpszDisplayName_ parameter is ignored if the message service has set the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MapiSvc.inf file.</span></span>
    
 <span data-ttu-id="1ecee-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1ecee-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="1ecee-115">[in]ダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドルを表示します。</span><span class="sxs-lookup"><span data-stu-id="1ecee-115">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="1ecee-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1ecee-116">_ulFlags_</span></span>
  
> <span data-ttu-id="1ecee-117">[in]メッセージ サービスをインストールする方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="1ecee-117">[in] A bitmask of flags that controls how the message service is installed.</span></span> <span data-ttu-id="1ecee-118">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="1ecee-118">The following flags can be set:</span></span>
    
<span data-ttu-id="1ecee-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1ecee-119">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="1ecee-120">LpszService および lpszDisplayName パラメーターを LPWSTR にキャストし、Unicode 文字列として解釈する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ecee-120">The lpszService and the lpszDisplayName parameters should be cast to LPWSTR and interpreted as Unicode strings.</span></span>
    
<span data-ttu-id="1ecee-121">SERVICE_NO_RESTART_WARNING</span><span class="sxs-lookup"><span data-stu-id="1ecee-121">SERVICE_NO_RESTART_WARNING</span></span>
  
> <span data-ttu-id="1ecee-122">新しいメッセージ サービスをプロファイルに追加するときに多くの場合さまざまな状況や条件に基づき、MAPI サブシステムがアクションには、Outlook の再起動が必要ですを決定します。</span><span class="sxs-lookup"><span data-stu-id="1ecee-122">When adding a new message service to the profile, the MAPI subsystem, based on various circumstances and criteria, often determines that this action requires a restart of Outlook.</span></span> <span data-ttu-id="1ecee-123">SERVICE_NO_RESTART_WARNING フラグが含まれていない UI を使用すると-- SERVICE_UI_ALWAYS と SERVICE_UI_ALLOWED のフラグに基づくし、少なくとも 1 つのプロセスは、現在のプロファイルにログオンしている、この関数、メッセージが表示"する必要があります Outlook を再起動これらの変更を有効にする。」</span><span class="sxs-lookup"><span data-stu-id="1ecee-123">If the SERVICE_NO_RESTART_WARNING flag is not included and UI is allowed - based on the SERVICE_UI_ALWAYS and SERVICE_UI_ALLOWED flags - and at least one process is logged onto the current profile, this function displays the message "You must restart Outlook for these changes to take effect."</span></span> <span data-ttu-id="1ecee-124">SERVICE_NO_RESTART_WARNING フラグを含む、警告メッセージの表示を抑制します。</span><span class="sxs-lookup"><span data-stu-id="1ecee-124">Including the SERVICE_NO_RESTART_WARNING flag suppresses the display of that warning message.</span></span>
    
<span data-ttu-id="1ecee-125">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="1ecee-125">SERVICE_UI_ALLOWED</span></span>
  
> <span data-ttu-id="1ecee-126">メッセージ サービスの構成が必要な場合、UI は許可されています。</span><span class="sxs-lookup"><span data-stu-id="1ecee-126">The message service configuration UI is allowed if needed.</span></span>
    
<span data-ttu-id="1ecee-127">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="1ecee-127">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="1ecee-128">メッセージ サービスでは、[設定] プロパティ シートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1ecee-128">The message service displays its configuration property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1ecee-129">�߂�l</span><span class="sxs-lookup"><span data-stu-id="1ecee-129">Return value</span></span>

<span data-ttu-id="1ecee-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="1ecee-130">S_OK</span></span> 
  
> <span data-ttu-id="1ecee-131">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="1ecee-131">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="1ecee-132">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="1ecee-132">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="1ecee-133">メッセージ サービス名は、MapiSvc.inf の **[サービス]** セクションではありません。</span><span class="sxs-lookup"><span data-stu-id="1ecee-133">The message service name is not in the **[Services]** section of MapiSvc.inf.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1ecee-134">注釈</span><span class="sxs-lookup"><span data-stu-id="1ecee-134">Remarks</span></span>

<span data-ttu-id="1ecee-135">**IMsgServiceAdmin::CreateMsgService**メソッドは、メッセージ サービスを現在のプロファイルに追加します。</span><span class="sxs-lookup"><span data-stu-id="1ecee-135">The **IMsgServiceAdmin::CreateMsgService** method adds a message service to the current profile.</span></span> <span data-ttu-id="1ecee-136">**CreateMsgService**は、サービス固有の構成タスクを実行するのには、メッセージ サービスのエントリ ポイント関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1ecee-136">**CreateMsgService** calls the message service's entry point function to perform any service-specific configuration tasks.</span></span> <span data-ttu-id="1ecee-137">_UlFlags_パラメーターに SERVICE_UI_ALLOWED フラグを設定すると、メッセージ サービスがインストールされているがその設定を構成するユーザーを有効にするプロパティ シートを表示できます。</span><span class="sxs-lookup"><span data-stu-id="1ecee-137">If the SERVICE_UI_ALLOWED flag is set in the  _ulFlags_ parameter, the message service being installed can display a property sheet to enable the user to configure its settings.</span></span> 
  
<span data-ttu-id="1ecee-138">MapiSvc.inf ファイルには、それぞれのメッセージ サービスとプロパティを構成するプロバイダーの一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1ecee-138">The MapiSvc.inf file contains the list of providers that make up a message service and the properties for each.</span></span> <span data-ttu-id="1ecee-139">**CreateMsgService**は、まずメッセージ サービス用の新しいプロファイル セクションを作成し、そのサービスの情報をすべて MapiSvc.inf ファイルからにコピー、プロファイルでは、プロバイダーごとに新しいセクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="1ecee-139">**CreateMsgService** first creates a new profile section for the message service and then copies all of the information for that service from the MapiSvc.inf file into the profile, creating new sections for each provider.</span></span> 
  
<span data-ttu-id="1ecee-140">MapiSvc.inf からすべての情報がコピーされた後は、 _ulContext_パラメーターに設定された MSG_SERVICE_CREATE 値を持つメッセージ サービスのエントリ ポイント関数が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="1ecee-140">After all the information has been copied from MapiSvc.inf, the message service's entry point function is called with the MSG_SERVICE_CREATE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="1ecee-141">**CreateMsgService**メソッドの_ulFlags_パラメーターに SERVICE_UI_ALLOWED フラグを設定すると、またには、 _ulUIParam_と_ulFlags_パラメーターの値は、メッセージ サービスのエントリ ポイント関数が呼び出されたときに渡されます。</span><span class="sxs-lookup"><span data-stu-id="1ecee-141">If the SERVICE_UI_ALLOWED flag is set in the **CreateMsgService** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed when the message service's entry point function is called.</span></span> <span data-ttu-id="1ecee-142">サービス プロバイダーは、ユーザーは、メッセージ サービスを構成することができますので、構成のプロパティ シートを表示します。</span><span class="sxs-lookup"><span data-stu-id="1ecee-142">Service providers should display their configuration property sheets so users can configure the message service.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1ecee-143">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="1ecee-143">Notes to callers</span></span>

 <span data-ttu-id="1ecee-144">**CreateMsgService**では、プロファイルに追加されたメッセージ サービスの[MAPIUID](mapiuid.md)構造体が返されません。</span><span class="sxs-lookup"><span data-stu-id="1ecee-144">**CreateMsgService** does not return the [MAPIUID](mapiuid.md) structure for the message service that was added to the profile.</span></span> 
  
<span data-ttu-id="1ecee-145">作成したメッセージ サービスの**MAPIUID**を取得するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="1ecee-145">To retrieve the **MAPIUID** for the created message service, use the following procedure:</span></span> 
  
1. <span data-ttu-id="1ecee-146">メッセージ サービスの管理テーブルを取得する[IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1ecee-146">Call the [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) method to get the message service administration table.</span></span> 
    
2. <span data-ttu-id="1ecee-147">メッセージ サービスの名前を**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) のプロパティに一致するテーブルに制限を配置することでメッセージ サービスを表す行を検索します。</span><span class="sxs-lookup"><span data-stu-id="1ecee-147">Locate the row that represents the message service by placing a restriction on the table that matches the **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) property with the name of the message service.</span></span> 
    
3. <span data-ttu-id="1ecee-148">サービスの**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) のプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="1ecee-148">Retrieve the service's **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property.</span></span> 
    
4. <span data-ttu-id="1ecee-149">**PR_SERVICE_UID**プロパティの値を_lpUid_パラメーターでメソッドに渡す、 [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)サービスを構成します。</span><span class="sxs-lookup"><span data-stu-id="1ecee-149">Pass the value of the **PR_SERVICE_UID** property in the  _lpUid_ parameter to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method to configure the service.</span></span> 
    
> [!CAUTION]
> <span data-ttu-id="1ecee-150">MAPI サブシステムの Microsoft Outlook 2010 の実装は、MAPI_UNICODE をサポートしていませんし、使用されている場合は失敗します。</span><span class="sxs-lookup"><span data-stu-id="1ecee-150">The Microsoft Outlook 2010 implementation of the MAPI subsystem does not support MAPI_UNICODE and will fail if it is used.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="1ecee-151">_UlFlags_ SERVICE_NO_RESTART_WARNING は、現在あるダウンロード可能なヘッダー ファイルで定義されていない可能性があります、場合に追加できます、次の値を使用してコード: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`</span><span class="sxs-lookup"><span data-stu-id="1ecee-151">The  _ulFlags_ SERVICE_NO_RESTART_WARNING might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define SERVICE_NO_RESTART_WARNING 0x00000080`</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1ecee-152">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="1ecee-152">MFCMAPI reference</span></span>

<span data-ttu-id="1ecee-153">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="1ecee-153">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1ecee-154">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="1ecee-154">**File**</span></span>|<span data-ttu-id="1ecee-155">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="1ecee-155">**Function**</span></span>|<span data-ttu-id="1ecee-156">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="1ecee-156">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1ecee-157">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="1ecee-157">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="1ecee-158">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="1ecee-158">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="1ecee-159">MFCMAPI では、 **IMsgServiceAdmin::CreateMsgService**メソッドを使用して、プロファイルにサービスを追加します。</span><span class="sxs-lookup"><span data-stu-id="1ecee-159">MFCMAPI uses the **IMsgServiceAdmin::CreateMsgService** method to add a service to a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1ecee-160">関連項目</span><span class="sxs-lookup"><span data-stu-id="1ecee-160">See also</span></span>



[<span data-ttu-id="1ecee-161">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1ecee-161">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


<span data-ttu-id="1ecee-162">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="1ecee-162">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

