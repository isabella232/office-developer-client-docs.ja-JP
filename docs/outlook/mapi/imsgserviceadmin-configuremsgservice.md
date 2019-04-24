---
title: IMsgServiceAdminConfigureMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.ConfigureMsgService
api_type:
- COM
ms.assetid: a08f5905-2585-49ca-abb7-a77f2736f604
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 87ac394f9ab77b092cdfcd44f65b040a039319e7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317410"
---
# <a name="imsgserviceadminconfiguremsgservice"></a><span data-ttu-id="af48d-103">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="af48d-103">IMsgServiceAdmin::ConfigureMsgService</span></span>

  
  
<span data-ttu-id="af48d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af48d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af48d-105">メッセージサービスを再構成します。</span><span class="sxs-lookup"><span data-stu-id="af48d-105">Reconfigures a message service.</span></span>
  
```cpp
HRESULT ConfigureMsgService(
  LPMAPIUID lpUID,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a><span data-ttu-id="af48d-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="af48d-106">Parameters</span></span>

 <span data-ttu-id="af48d-107">_lpuid_</span><span class="sxs-lookup"><span data-stu-id="af48d-107">_lpUID_</span></span>
  
> <span data-ttu-id="af48d-108">順番構成するメッセージサービスの一意の識別子を含む[MAPIUID](mapiuid.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="af48d-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to configure.</span></span> 
    
 <span data-ttu-id="af48d-109">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="af48d-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="af48d-110">順番構成プロパティシートの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="af48d-110">[in] A handle to the parent window of the configuration property sheet.</span></span>
    
 <span data-ttu-id="af48d-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="af48d-111">_ulFlags_</span></span>
  
> <span data-ttu-id="af48d-112">順番プロパティシートの表示を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="af48d-112">[in] A bitmask of flags that controls the display of the property sheet.</span></span> <span data-ttu-id="af48d-113">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="af48d-113">The following flags can be set:</span></span>
    
<span data-ttu-id="af48d-114">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="af48d-114">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="af48d-115">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="af48d-115">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="af48d-116">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="af48d-116">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="af48d-117">MSG_SERVICE_UI_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="af48d-117">MSG_SERVICE_UI_READ_ONLY</span></span> 
  
> <span data-ttu-id="af48d-118">メッセージサービスには、その構成プロパティシートが表示されますが、ユーザーが変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="af48d-118">The message service should display its configuration property sheet but not enable the user to change it.</span></span> <span data-ttu-id="af48d-119">ほとんどのメッセージサービスでは、このフラグは無視します。</span><span class="sxs-lookup"><span data-stu-id="af48d-119">Most message services ignore this flag.</span></span>
    
<span data-ttu-id="af48d-120">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="af48d-120">SERVICE_UI_ALLOWED</span></span> 
  
> <span data-ttu-id="af48d-121">サービスが完全に構成されていない場合にのみ、メッセージサービスにその構成プロパティシートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="af48d-121">The message service should display its configuration property sheet only if the service is not completely configured.</span></span>
    
<span data-ttu-id="af48d-122">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="af48d-122">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="af48d-123">メッセージサービスには、常にその構成プロパティシートが表示されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="af48d-123">The message service must always display its configuration property sheet.</span></span> <span data-ttu-id="af48d-124">SERVICE_UI_ALWAYS が設定されていない場合でも、SERVICE_UI_ALLOWED が設定されていて、有効な構成情報が_lpprops_パラメーターのプロパティ値の配列から利用できない場合、構成プロパティシートが表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="af48d-124">If SERVICE_UI_ALWAYS is not set, a configuration property sheet can still be displayed if SERVICE_UI_ALLOWED is set and valid configuration information is not available from the property value array in the  _lpProps_ parameter.</span></span> <span data-ttu-id="af48d-125">プロパティシートが表示されるようにするには、SERVICE_UI_ALLOWED または SERVICE_UI_ALWAYS のいずれかを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="af48d-125">Either SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS must be set for a property sheet to be displayed.</span></span> 
    
 <span data-ttu-id="af48d-126">_cvalues_</span><span class="sxs-lookup"><span data-stu-id="af48d-126">_cValues_</span></span>
  
> <span data-ttu-id="af48d-127">順番_lpprops_によってポイントされた[spropvalue](spropvalue.md)構造のプロパティ値の数。</span><span class="sxs-lookup"><span data-stu-id="af48d-127">[in] The count of property values in the [SPropValue](spropvalue.md) structure pointed to by  _lpProps_.</span></span> 
    
 <span data-ttu-id="af48d-128">_lpprops_</span><span class="sxs-lookup"><span data-stu-id="af48d-128">_lpProps_</span></span>
  
> <span data-ttu-id="af48d-129">順番プロパティシートに表示されるプロパティを説明するプロパティ値の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="af48d-129">[in] A pointer to an array of property values that describe the properties to display in the property sheet.</span></span> <span data-ttu-id="af48d-130">メッセージサービスをユーザーインターフェイスなしで構成する必要がある場合は、 _lpprops_パラメーターを NULL にしないでください。</span><span class="sxs-lookup"><span data-stu-id="af48d-130">The  _lpProps_ parameter should not be NULL if the message service should be configured without a user interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="af48d-131">戻り値</span><span class="sxs-lookup"><span data-stu-id="af48d-131">Return value</span></span>

<span data-ttu-id="af48d-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="af48d-132">S_OK</span></span> 
  
> <span data-ttu-id="af48d-133">メッセージサービスが正常に構成されました。</span><span class="sxs-lookup"><span data-stu-id="af48d-133">The message service was successfully configured.</span></span>
    
<span data-ttu-id="af48d-134">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="af48d-134">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="af48d-135">メッセージサービスに固有のエラー。</span><span class="sxs-lookup"><span data-stu-id="af48d-135">An error specific to a message service.</span></span> <span data-ttu-id="af48d-136">エラーを説明する[MAPIERROR](mapierror.md)構造を取得するには、クライアントアプリケーションは[IMsgServiceAdmin:: GetLastError](imsgserviceadmin-getlasterror.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="af48d-136">To get the [MAPIERROR](mapierror.md) structure that describes the error, the client application should call the [IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="af48d-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="af48d-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="af48d-138">_lpuid_が指す**MAPIUID**が、既存のメッセージサービスのものと一致しません。</span><span class="sxs-lookup"><span data-stu-id="af48d-138">The **MAPIUID** pointed to by  _lpUID_ does not match that of an existing message service.</span></span> 
    
<span data-ttu-id="af48d-139">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="af48d-139">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="af48d-140">メッセージサービスにエントリポイント関数がありません。</span><span class="sxs-lookup"><span data-stu-id="af48d-140">The message service does not have an entry point function.</span></span>
    
<span data-ttu-id="af48d-141">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="af48d-141">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="af48d-142">ユーザーが操作をキャンセルしました。通常は、プロパティシートの **[キャンセル**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="af48d-142">The user canceled the operation, typically by clicking the **Cancel** button in the property sheet.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="af48d-143">解説</span><span class="sxs-lookup"><span data-stu-id="af48d-143">Remarks</span></span>

<span data-ttu-id="af48d-144">**IMsgServiceAdmin:: ConfigureMsgService**メソッドを使用すると、構成プロパティシートの有無にかかわらず、メッセージサービスを構成できます。</span><span class="sxs-lookup"><span data-stu-id="af48d-144">The **IMsgServiceAdmin::ConfigureMsgService** method enables a message service to be configured, with or without a configuration property sheet.</span></span> 
  
<span data-ttu-id="af48d-145">プロパティシートが表示されない構成を許可する場合、通常、メッセージサービスは、必要なすべてのプロパティとその値の定数を含むヘッダーファイルを準備します。</span><span class="sxs-lookup"><span data-stu-id="af48d-145">To allow configuration without a property sheet display, message services typically prepare a header file that includes constants for all the required and optional properties and their values.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="af48d-146">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="af48d-146">Notes to callers</span></span>

<span data-ttu-id="af48d-147">構成するメッセージサービスの**MAPIUID**構造を取得するには、メッセージサービステーブルのメッセージサービスの行から [ **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))] 列を取得します。</span><span class="sxs-lookup"><span data-stu-id="af48d-147">To retrieve the **MAPIUID** structure for the message service to configure, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column from the message service's row in the message service table.</span></span> <span data-ttu-id="af48d-148">詳細については、 [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md)メソッドに記載されている手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="af48d-148">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
<span data-ttu-id="af48d-149">設定するプロパティ値に関する詳細情報がある場合にのみ、ユーザーにプロパティシートを表示せずに、メッセージサービスを構成できます。</span><span class="sxs-lookup"><span data-stu-id="af48d-149">You can configure a message service without displaying a property sheet to a user only if you have advance information about the property values to be set.</span></span> <span data-ttu-id="af48d-150">プロパティシートを表示せずにメッセージサービスを構成する場合は、 _lpprops_パラメーターに有効なプロパティ値を渡し、MSG_SERVICE_UI_READ_ONLY、SERVICE_UI_ALLOWED、または SERVICE_UI_ALWAYS フラグは設定しません。</span><span class="sxs-lookup"><span data-stu-id="af48d-150">If you are configuring a message service without displaying a property sheet, pass valid property values in the  _lpProps_ parameter and do not set the MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED, or SERVICE_UI_ALWAYS flags.</span></span> 
  
<span data-ttu-id="af48d-151">プロパティシートを使用して、ユーザーから構成情報の全部または一部を受け取った場合は、 _ulflags_で SERVICE_UI_ALLOWED を設定します。</span><span class="sxs-lookup"><span data-stu-id="af48d-151">If you receive all or some of the configuration information from the user by way of a property sheet, set SERVICE_UI_ALLOWED in  _ulFlags_.</span></span> <span data-ttu-id="af48d-152">既存のプロパティ情報のみを使用して既定の設定を確立し、ユーザーが設定を変更できる場合は、 _ulflags_で SERVICE_UI_ALWAYS を設定します。</span><span class="sxs-lookup"><span data-stu-id="af48d-152">If you use existing property information only to establish default settings and the user is able to change the settings, set SERVICE_UI_ALWAYS in  _ulFlags_.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="af48d-153">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="af48d-153">MFCMAPI reference</span></span>

<span data-ttu-id="af48d-154">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="af48d-154">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="af48d-155">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="af48d-155">**File**</span></span>|<span data-ttu-id="af48d-156">**関数**</span><span class="sxs-lookup"><span data-stu-id="af48d-156">**Function**</span></span>|<span data-ttu-id="af48d-157">**コメント**</span><span class="sxs-lookup"><span data-stu-id="af48d-157">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="af48d-158">MAPIProfileFunctions</span><span class="sxs-lookup"><span data-stu-id="af48d-158">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="af48d-159">hraddservicetoprofile</span><span class="sxs-lookup"><span data-stu-id="af48d-159">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="af48d-160">mfcmapi は、 **IMsgServiceAdmin:: ConfigureMsgService**メソッドを使用して、プロファイルに追加されたサービスを構成します。</span><span class="sxs-lookup"><span data-stu-id="af48d-160">MFCMAPI uses the **IMsgServiceAdmin::ConfigureMsgService** method to configure a service that has been added to a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="af48d-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="af48d-161">See also</span></span>



[<span data-ttu-id="af48d-162">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="af48d-162">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="af48d-163">SPropValue</span><span class="sxs-lookup"><span data-stu-id="af48d-163">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="af48d-164">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="af48d-164">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


<span data-ttu-id="af48d-165">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="af48d-165">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

