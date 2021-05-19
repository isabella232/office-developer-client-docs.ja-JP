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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e7d30c1aba8ddc1419045c1caa8524f7d2063dc5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434978"
---
# <a name="imsgserviceadmincreatemsgservice"></a><span data-ttu-id="05b60-103">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="05b60-103">IMsgServiceAdmin::CreateMsgService</span></span>

  
  
<span data-ttu-id="05b60-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05b60-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05b60-105">非推奨: [IMsgServiceAdmin2::CreateMsgServiceEx の使用をお](imsgserviceadmin2-createmsgserviceex.md) 勧めします。</span><span class="sxs-lookup"><span data-stu-id="05b60-105">Deprecated: The use of [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) is recommended.</span></span> <span data-ttu-id="05b60-106">現在のプロファイルにメッセージ サービスを追加します。</span><span class="sxs-lookup"><span data-stu-id="05b60-106">Adds a message service to the current profile.</span></span> 
  
```cpp
HRESULT CreateMsgService(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags    
);
```

## <a name="parameters"></a><span data-ttu-id="05b60-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="05b60-107">Parameters</span></span>

 <span data-ttu-id="05b60-108">_lpszService_</span><span class="sxs-lookup"><span data-stu-id="05b60-108">_lpszService_</span></span>
  
> <span data-ttu-id="05b60-109">[in]追加するメッセージ サービスの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="05b60-109">[in] A pointer to the name of the message service to add.</span></span> <span data-ttu-id="05b60-110">このメッセージ サービス名は、MapiSvc.inf ファイル **の [Services]** セクションに表示される必要があります。</span><span class="sxs-lookup"><span data-stu-id="05b60-110">This message service name must appear in the **[Services]** section of the MapiSvc.inf file.</span></span> 
    
 <span data-ttu-id="05b60-111">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="05b60-111">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="05b60-112">[in]追加するメッセージ サービスの表示名へのポインター。</span><span class="sxs-lookup"><span data-stu-id="05b60-112">[in] A pointer to the display name of the message service to add.</span></span> <span data-ttu-id="05b60-113">メッセージ サービスが MapiSvc.inf ファイルの PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティを設定している場合 _、lpszDisplayName_ パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="05b60-113">The  _lpszDisplayName_ parameter is ignored if the message service has set the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MapiSvc.inf file.</span></span>
    
 <span data-ttu-id="05b60-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="05b60-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="05b60-115">[in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="05b60-115">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="05b60-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="05b60-116">_ulFlags_</span></span>
  
> <span data-ttu-id="05b60-117">[in]メッセージ サービスのインストール方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="05b60-117">[in] A bitmask of flags that controls how the message service is installed.</span></span> <span data-ttu-id="05b60-118">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="05b60-118">The following flags can be set:</span></span>
    
<span data-ttu-id="05b60-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="05b60-119">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="05b60-120">lpszService パラメーターと lpszDisplayName パラメーターを LPWSTR にキャストし、Unicode 文字列として解釈する必要があります。</span><span class="sxs-lookup"><span data-stu-id="05b60-120">The lpszService and the lpszDisplayName parameters should be cast to LPWSTR and interpreted as Unicode strings.</span></span>
    
<span data-ttu-id="05b60-121">SERVICE_NO_RESTART_WARNING</span><span class="sxs-lookup"><span data-stu-id="05b60-121">SERVICE_NO_RESTART_WARNING</span></span>
  
> <span data-ttu-id="05b60-122">プロファイルに新しいメッセージ サービスを追加する場合、MAPI サブシステムは、さまざまな状況と条件に基づいて、多くの場合、このアクションでプロファイルの再起動が必要Outlook。</span><span class="sxs-lookup"><span data-stu-id="05b60-122">When adding a new message service to the profile, the MAPI subsystem, based on various circumstances and criteria, often determines that this action requires a restart of Outlook.</span></span> <span data-ttu-id="05b60-123">SERVICE_NO_RESTART_WARNING フラグが含まれていない場合に、SERVICE_UI_ALWAYS フラグと SERVICE_UI_ALLOWED フラグに基づいて UI が許可され、少なくとも 1 つのプロセスが現在のプロファイルにログオンしている場合、この関数は「これらの変更を有効にするために Outlook を再起動する必要があります」というメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="05b60-123">If the SERVICE_NO_RESTART_WARNING flag is not included and UI is allowed - based on the SERVICE_UI_ALWAYS and SERVICE_UI_ALLOWED flags - and at least one process is logged onto the current profile, this function displays the message "You must restart Outlook for these changes to take effect."</span></span> <span data-ttu-id="05b60-124">フラグをSERVICE_NO_RESTART_WARNINGすると、その警告メッセージの表示が抑制されます。</span><span class="sxs-lookup"><span data-stu-id="05b60-124">Including the SERVICE_NO_RESTART_WARNING flag suppresses the display of that warning message.</span></span>
    
<span data-ttu-id="05b60-125">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="05b60-125">SERVICE_UI_ALLOWED</span></span>
  
> <span data-ttu-id="05b60-126">必要に応じて、メッセージ サービス構成 UI を使用できます。</span><span class="sxs-lookup"><span data-stu-id="05b60-126">The message service configuration UI is allowed if needed.</span></span>
    
<span data-ttu-id="05b60-127">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="05b60-127">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="05b60-128">メッセージ サービスは、構成プロパティ シートを表示します。</span><span class="sxs-lookup"><span data-stu-id="05b60-128">The message service displays its configuration property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="05b60-129">戻り値</span><span class="sxs-lookup"><span data-stu-id="05b60-129">Return value</span></span>

<span data-ttu-id="05b60-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="05b60-130">S_OK</span></span> 
  
> <span data-ttu-id="05b60-131">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="05b60-131">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="05b60-132">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="05b60-132">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="05b60-133">メッセージ サービス名は MapiSvc.inf の **[Services]** セクションに含めではありません。</span><span class="sxs-lookup"><span data-stu-id="05b60-133">The message service name is not in the **[Services]** section of MapiSvc.inf.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="05b60-134">注釈</span><span class="sxs-lookup"><span data-stu-id="05b60-134">Remarks</span></span>

<span data-ttu-id="05b60-135">**IMsgServiceAdmin::CreateMsgService** メソッドは、現在のプロファイルにメッセージ サービスを追加します。</span><span class="sxs-lookup"><span data-stu-id="05b60-135">The **IMsgServiceAdmin::CreateMsgService** method adds a message service to the current profile.</span></span> <span data-ttu-id="05b60-136">**CreateMsgService は** 、メッセージ サービスのエントリ ポイント関数を呼び出して、サービス固有の構成タスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="05b60-136">**CreateMsgService** calls the message service's entry point function to perform any service-specific configuration tasks.</span></span> <span data-ttu-id="05b60-137">_ulFlags_ パラメーター SERVICE_UI_ALLOWEDフラグが設定されている場合、インストールされているメッセージ サービスはプロパティ シートを表示して、ユーザーが設定を構成できます。</span><span class="sxs-lookup"><span data-stu-id="05b60-137">If the SERVICE_UI_ALLOWED flag is set in the  _ulFlags_ parameter, the message service being installed can display a property sheet to enable the user to configure its settings.</span></span> 
  
<span data-ttu-id="05b60-138">MapiSvc.inf ファイルには、メッセージ サービスを構成するプロバイダーの一覧と、それぞれのプロパティが含まれる。</span><span class="sxs-lookup"><span data-stu-id="05b60-138">The MapiSvc.inf file contains the list of providers that make up a message service and the properties for each.</span></span> <span data-ttu-id="05b60-139">**CreateMsgService** は、まずメッセージ サービスの新しいプロファイル セクションを作成し、そのサービスのすべての情報を MapiSvc.inf ファイルからプロファイルにコピーし、プロバイダーごとに新しいセクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="05b60-139">**CreateMsgService** first creates a new profile section for the message service and then copies all of the information for that service from the MapiSvc.inf file into the profile, creating new sections for each provider.</span></span> 
  
<span data-ttu-id="05b60-140">MapiSvc.inf からすべての情報がコピーされた後、メッセージ サービスのエントリ ポイント関数が呼び出され  _、ulContext_ パラメーターに MSG_SERVICE_CREATE 値が設定されます。</span><span class="sxs-lookup"><span data-stu-id="05b60-140">After all the information has been copied from MapiSvc.inf, the message service's entry point function is called with the MSG_SERVICE_CREATE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="05b60-141">**CreateMsgService** メソッドの _ulFlags_ パラメーターで SERVICE_UI_ALLOWED フラグが設定されている場合、メッセージ サービスのエントリ ポイント関数が呼び出された場合 _、ulUIParam_ パラメーターと _ulFlags_ パラメーターの値も渡されます。</span><span class="sxs-lookup"><span data-stu-id="05b60-141">If the SERVICE_UI_ALLOWED flag is set in the **CreateMsgService** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed when the message service's entry point function is called.</span></span> <span data-ttu-id="05b60-142">サービス プロバイダーは、ユーザーがメッセージ サービスを構成できるよう、構成プロパティ シートを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="05b60-142">Service providers should display their configuration property sheets so users can configure the message service.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="05b60-143">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="05b60-143">Notes to callers</span></span>

 <span data-ttu-id="05b60-144">**CreateMsgService** は、プロファイルに追加されたメッセージ サービスの [MAPIUID](mapiuid.md) 構造を返します。</span><span class="sxs-lookup"><span data-stu-id="05b60-144">**CreateMsgService** does not return the [MAPIUID](mapiuid.md) structure for the message service that was added to the profile.</span></span> 
  
<span data-ttu-id="05b60-145">作成したメッセージ **サービスの MAPIUID** を取得するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="05b60-145">To retrieve the **MAPIUID** for the created message service, use the following procedure:</span></span> 
  
1. <span data-ttu-id="05b60-146">メッセージ サービス [管理テーブルを取得するには、IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="05b60-146">Call the [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) method to get the message service administration table.</span></span> 
    
2. <span data-ttu-id="05b60-147">メッセージ サービスの名前を持つ **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) プロパティに一致するテーブルに制限を設定して、メッセージ サービスを表す行を探します。</span><span class="sxs-lookup"><span data-stu-id="05b60-147">Locate the row that represents the message service by placing a restriction on the table that matches the **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) property with the name of the message service.</span></span> 
    
3. <span data-ttu-id="05b60-148">サービスのプロパティ [(PidTagServiceUid)](pidtagserviceuid-canonical-property.md) **PR_SERVICE_UIDプロパティ** を取得します。</span><span class="sxs-lookup"><span data-stu-id="05b60-148">Retrieve the service's **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property.</span></span> 
    
4. <span data-ttu-id="05b60-149">_lpUid_ パラメーターの **PR_SERVICE_UID** プロパティの値を [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)メソッドに渡して、サービスを構成します。</span><span class="sxs-lookup"><span data-stu-id="05b60-149">Pass the value of the **PR_SERVICE_UID** property in the  _lpUid_ parameter to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method to configure the service.</span></span> 
    
> [!CAUTION]
> <span data-ttu-id="05b60-150">MAPI Microsoft Outlook 2010の実装では、MAPI サブシステムMAPI_UNICODEサポートされません。使用すると失敗します。</span><span class="sxs-lookup"><span data-stu-id="05b60-150">The Microsoft Outlook 2010 implementation of the MAPI subsystem does not support MAPI_UNICODE and will fail if it is used.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="05b60-151">_ulFlags_ SERVICE_NO_RESTART_WARNINGは、現在使用しているダウンロード可能なヘッダー ファイルで定義されていない可能性があります。その場合は、次の値を使用してコードに追加>`#define SERVICE_NO_RESTART_WARNING 0x00000080`</span><span class="sxs-lookup"><span data-stu-id="05b60-151">The  _ulFlags_ SERVICE_NO_RESTART_WARNING might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define SERVICE_NO_RESTART_WARNING 0x00000080`</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="05b60-152">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="05b60-152">MFCMAPI reference</span></span>

<span data-ttu-id="05b60-153">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="05b60-153">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="05b60-154">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="05b60-154">**File**</span></span>|<span data-ttu-id="05b60-155">**関数**</span><span class="sxs-lookup"><span data-stu-id="05b60-155">**Function**</span></span>|<span data-ttu-id="05b60-156">**コメント**</span><span class="sxs-lookup"><span data-stu-id="05b60-156">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="05b60-157">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="05b60-157">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="05b60-158">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="05b60-158">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="05b60-159">MFCMAPI は **、IMsgServiceAdmin::CreateMsgService** メソッドを使用して、サービスをプロファイルに追加します。</span><span class="sxs-lookup"><span data-stu-id="05b60-159">MFCMAPI uses the **IMsgServiceAdmin::CreateMsgService** method to add a service to a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="05b60-160">関連項目</span><span class="sxs-lookup"><span data-stu-id="05b60-160">See also</span></span>



[<span data-ttu-id="05b60-161">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="05b60-161">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


<span data-ttu-id="05b60-162">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="05b60-162">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

