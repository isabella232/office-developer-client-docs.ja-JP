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
ms.openlocfilehash: e7d30c1aba8ddc1419045c1caa8524f7d2063dc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317400"
---
# <a name="imsgserviceadmincreatemsgservice"></a><span data-ttu-id="8b567-103">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="8b567-103">IMsgServiceAdmin::CreateMsgService</span></span>

  
  
<span data-ttu-id="8b567-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b567-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b567-105">非推奨: [IMsgServiceAdmin2:: CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md)を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8b567-105">Deprecated: The use of [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) is recommended.</span></span> <span data-ttu-id="8b567-106">現在のプロファイルにメッセージサービスを追加します。</span><span class="sxs-lookup"><span data-stu-id="8b567-106">Adds a message service to the current profile.</span></span> 
  
```cpp
HRESULT CreateMsgService(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags    
);
```

## <a name="parameters"></a><span data-ttu-id="8b567-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8b567-107">Parameters</span></span>

 <span data-ttu-id="8b567-108">_lpszservice_</span><span class="sxs-lookup"><span data-stu-id="8b567-108">_lpszService_</span></span>
  
> <span data-ttu-id="8b567-109">順番追加するメッセージサービスの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8b567-109">[in] A pointer to the name of the message service to add.</span></span> <span data-ttu-id="8b567-110">このメッセージサービス名は、mapisvc.inf ファイルの **[Services]** セクションに表示される必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b567-110">This message service name must appear in the **[Services]** section of the MapiSvc.inf file.</span></span> 
    
 <span data-ttu-id="8b567-111">_lpszdisplayname_</span><span class="sxs-lookup"><span data-stu-id="8b567-111">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="8b567-112">順番追加するメッセージサービスの表示名へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8b567-112">[in] A pointer to the display name of the message service to add.</span></span> <span data-ttu-id="8b567-113">メッセージサービスが mapisvc.inf ファイルで**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティを設定している場合、 _lpszdisplayname_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="8b567-113">The  _lpszDisplayName_ parameter is ignored if the message service has set the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MapiSvc.inf file.</span></span>
    
 <span data-ttu-id="8b567-114">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="8b567-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="8b567-115">順番このメソッドが表示する任意のダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="8b567-115">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="8b567-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8b567-116">_ulFlags_</span></span>
  
> <span data-ttu-id="8b567-117">順番メッセージサービスのインストール方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="8b567-117">[in] A bitmask of flags that controls how the message service is installed.</span></span> <span data-ttu-id="8b567-118">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="8b567-118">The following flags can be set:</span></span>
    
<span data-ttu-id="8b567-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8b567-119">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="8b567-120">lpszservice および lpszservice パラメーターは、LPWSTR にキャストし、Unicode 文字列として解釈される必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b567-120">The lpszService and the lpszDisplayName parameters should be cast to LPWSTR and interpreted as Unicode strings.</span></span>
    
<span data-ttu-id="8b567-121">SERVICE_NO_RESTART_WARNING</span><span class="sxs-lookup"><span data-stu-id="8b567-121">SERVICE_NO_RESTART_WARNING</span></span>
  
> <span data-ttu-id="8b567-122">プロファイルに新しいメッセージサービスを追加すると、さまざまな状況や条件に基づいて MAPI サブシステムが、Outlook の再起動が必要であると判断されることがよくあります。</span><span class="sxs-lookup"><span data-stu-id="8b567-122">When adding a new message service to the profile, the MAPI subsystem, based on various circumstances and criteria, often determines that this action requires a restart of Outlook.</span></span> <span data-ttu-id="8b567-123">SERVICE_NO_RESTART_WARNING フラグが含まれておらず、SERVICE_UI_ALWAYS と SERVICE_UI_ALLOWED フラグに基づいて UI が許可されていて、少なくとも1つのプロセスが現在のプロファイルに記録されている場合、この関数は "Outlook を再起動する必要があります。" というメッセージを表示します。これらの変更は有効になります。</span><span class="sxs-lookup"><span data-stu-id="8b567-123">If the SERVICE_NO_RESTART_WARNING flag is not included and UI is allowed - based on the SERVICE_UI_ALWAYS and SERVICE_UI_ALLOWED flags - and at least one process is logged onto the current profile, this function displays the message "You must restart Outlook for these changes to take effect."</span></span> <span data-ttu-id="8b567-124">SERVICE_NO_RESTART_WARNING フラグを含めると、その警告メッセージの表示が抑制されます。</span><span class="sxs-lookup"><span data-stu-id="8b567-124">Including the SERVICE_NO_RESTART_WARNING flag suppresses the display of that warning message.</span></span>
    
<span data-ttu-id="8b567-125">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="8b567-125">SERVICE_UI_ALLOWED</span></span>
  
> <span data-ttu-id="8b567-126">必要に応じて、メッセージサービス構成 UI を使用できます。</span><span class="sxs-lookup"><span data-stu-id="8b567-126">The message service configuration UI is allowed if needed.</span></span>
    
<span data-ttu-id="8b567-127">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="8b567-127">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="8b567-128">メッセージサービスには、その構成プロパティシートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8b567-128">The message service displays its configuration property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8b567-129">戻り値</span><span class="sxs-lookup"><span data-stu-id="8b567-129">Return value</span></span>

<span data-ttu-id="8b567-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="8b567-130">S_OK</span></span> 
  
> <span data-ttu-id="8b567-131">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="8b567-131">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="8b567-132">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="8b567-132">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="8b567-133">メッセージサービス名が mapisvc.inf の **[Services]** セクションにありません。</span><span class="sxs-lookup"><span data-stu-id="8b567-133">The message service name is not in the **[Services]** section of MapiSvc.inf.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8b567-134">解説</span><span class="sxs-lookup"><span data-stu-id="8b567-134">Remarks</span></span>

<span data-ttu-id="8b567-135">**IMsgServiceAdmin:: CreateMsgService**メソッドは、現在のプロファイルにメッセージサービスを追加します。</span><span class="sxs-lookup"><span data-stu-id="8b567-135">The **IMsgServiceAdmin::CreateMsgService** method adds a message service to the current profile.</span></span> <span data-ttu-id="8b567-136">**CreateMsgService**は、メッセージサービスのエントリポイント関数を呼び出して、サービス固有の構成タスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="8b567-136">**CreateMsgService** calls the message service's entry point function to perform any service-specific configuration tasks.</span></span> <span data-ttu-id="8b567-137">SERVICE_UI_ALLOWED フラグが_ulflags_パラメーターで設定されている場合は、インストールされているメッセージサービスにプロパティシートを表示して、ユーザーがその設定を構成できるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="8b567-137">If the SERVICE_UI_ALLOWED flag is set in the  _ulFlags_ parameter, the message service being installed can display a property sheet to enable the user to configure its settings.</span></span> 
  
<span data-ttu-id="8b567-138">mapisvc.inf ファイルには、メッセージサービスを構成するプロバイダーの一覧とそれぞれのプロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8b567-138">The MapiSvc.inf file contains the list of providers that make up a message service and the properties for each.</span></span> <span data-ttu-id="8b567-139">**CreateMsgService**は、最初にメッセージサービス用の新しいプロファイルセクションを作成し、そのサービスのすべての情報を mapisvc.inf ファイルからプロファイルにコピーして、各プロバイダーに新しいセクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="8b567-139">**CreateMsgService** first creates a new profile section for the message service and then copies all of the information for that service from the MapiSvc.inf file into the profile, creating new sections for each provider.</span></span> 
  
<span data-ttu-id="8b567-140">すべての情報が mapisvc.inf からコピーされた後、メッセージサービスのエントリポイント関数が、 _ulcontext_パラメーターで設定された MSG_SERVICE_CREATE 値を使用して呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8b567-140">After all the information has been copied from MapiSvc.inf, the message service's entry point function is called with the MSG_SERVICE_CREATE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="8b567-141">SERVICE_UI_ALLOWED フラグが**CreateMsgService**メソッドの_ulflags_パラメーターで設定されている場合は、メッセージサービスのエントリポイント関数が呼び出されたときに、 _uluiparam_パラメーターと_ulflags_パラメーターの値も渡されます。</span><span class="sxs-lookup"><span data-stu-id="8b567-141">If the SERVICE_UI_ALLOWED flag is set in the **CreateMsgService** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed when the message service's entry point function is called.</span></span> <span data-ttu-id="8b567-142">サービスプロバイダーは、ユーザーがメッセージサービスを構成できるように、その構成プロパティシートを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b567-142">Service providers should display their configuration property sheets so users can configure the message service.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8b567-143">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="8b567-143">Notes to callers</span></span>

 <span data-ttu-id="8b567-144">**CreateMsgService**は、プロファイルに追加されたメッセージサービスの[MAPIUID](mapiuid.md)構造を返しません。</span><span class="sxs-lookup"><span data-stu-id="8b567-144">**CreateMsgService** does not return the [MAPIUID](mapiuid.md) structure for the message service that was added to the profile.</span></span> 
  
<span data-ttu-id="8b567-145">作成されたメッセージサービスの**MAPIUID**を取得するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="8b567-145">To retrieve the **MAPIUID** for the created message service, use the following procedure:</span></span> 
  
1. <span data-ttu-id="8b567-146">[IMsgServiceAdmin:: getmsgservicetable](imsgserviceadmin-getmsgservicetable.md)メソッドを呼び出して、メッセージサービス管理テーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="8b567-146">Call the [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) method to get the message service administration table.</span></span> 
    
2. <span data-ttu-id="8b567-147">**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) プロパティとメッセージサービスの名前を一致させる制限をテーブルに配置することによって、メッセージサービスを表す行を見つけます。</span><span class="sxs-lookup"><span data-stu-id="8b567-147">Locate the row that represents the message service by placing a restriction on the table that matches the **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) property with the name of the message service.</span></span> 
    
3. <span data-ttu-id="8b567-148">サービスの**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="8b567-148">Retrieve the service's **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property.</span></span> 
    
4. <span data-ttu-id="8b567-149">_lpuid_パラメーターの**PR_SERVICE_UID**プロパティの値を[IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)メソッドに渡して、サービスを構成します。</span><span class="sxs-lookup"><span data-stu-id="8b567-149">Pass the value of the **PR_SERVICE_UID** property in the  _lpUid_ parameter to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method to configure the service.</span></span> 
    
> [!CAUTION]
> <span data-ttu-id="8b567-150">MAPI サブシステムの Microsoft Outlook 2010 実装は MAPI_UNICODE をサポートしていないため、使用されている場合は失敗します。</span><span class="sxs-lookup"><span data-stu-id="8b567-150">The Microsoft Outlook 2010 implementation of the MAPI subsystem does not support MAPI_UNICODE and will fail if it is used.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="8b567-151">_ulflags_ SERVICE_NO_RESTART_WARNING は、現在のダウンロード可能なヘッダーファイルでは定義されていない場合があります。その場合は、次の値を使用してコードに追加できます。 >`#define SERVICE_NO_RESTART_WARNING 0x00000080`</span><span class="sxs-lookup"><span data-stu-id="8b567-151">The  _ulFlags_ SERVICE_NO_RESTART_WARNING might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define SERVICE_NO_RESTART_WARNING 0x00000080`</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8b567-152">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="8b567-152">MFCMAPI reference</span></span>

<span data-ttu-id="8b567-153">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b567-153">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8b567-154">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="8b567-154">**File**</span></span>|<span data-ttu-id="8b567-155">**関数**</span><span class="sxs-lookup"><span data-stu-id="8b567-155">**Function**</span></span>|<span data-ttu-id="8b567-156">**コメント**</span><span class="sxs-lookup"><span data-stu-id="8b567-156">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8b567-157">MAPIProfileFunctions</span><span class="sxs-lookup"><span data-stu-id="8b567-157">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="8b567-158">hraddservicetoprofile</span><span class="sxs-lookup"><span data-stu-id="8b567-158">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="8b567-159">mfcmapi は、 **IMsgServiceAdmin:: CreateMsgService**メソッドを使用して、プロファイルにサービスを追加します。</span><span class="sxs-lookup"><span data-stu-id="8b567-159">MFCMAPI uses the **IMsgServiceAdmin::CreateMsgService** method to add a service to a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8b567-160">関連項目</span><span class="sxs-lookup"><span data-stu-id="8b567-160">See also</span></span>



[<span data-ttu-id="8b567-161">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8b567-161">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


<span data-ttu-id="8b567-162">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="8b567-162">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

