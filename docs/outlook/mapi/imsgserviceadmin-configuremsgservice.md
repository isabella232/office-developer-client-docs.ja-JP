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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 87ac394f9ab77b092cdfcd44f65b040a039319e7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422188"
---
# <a name="imsgserviceadminconfiguremsgservice"></a><span data-ttu-id="4bcea-103">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="4bcea-103">IMsgServiceAdmin::ConfigureMsgService</span></span>

  
  
<span data-ttu-id="4bcea-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4bcea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4bcea-105">メッセージ サービスを再構成します。</span><span class="sxs-lookup"><span data-stu-id="4bcea-105">Reconfigures a message service.</span></span>
  
```cpp
HRESULT ConfigureMsgService(
  LPMAPIUID lpUID,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a><span data-ttu-id="4bcea-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4bcea-106">Parameters</span></span>

 <span data-ttu-id="4bcea-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="4bcea-107">_lpUID_</span></span>
  
> <span data-ttu-id="4bcea-108">[in]構成するメッセージ サービスの一意の識別子を含む [MAPIUID](mapiuid.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4bcea-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to configure.</span></span> 
    
 <span data-ttu-id="4bcea-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="4bcea-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="4bcea-110">[in]構成プロパティ シートの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="4bcea-110">[in] A handle to the parent window of the configuration property sheet.</span></span>
    
 <span data-ttu-id="4bcea-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4bcea-111">_ulFlags_</span></span>
  
> <span data-ttu-id="4bcea-112">[in]プロパティ シートの表示を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="4bcea-112">[in] A bitmask of flags that controls the display of the property sheet.</span></span> <span data-ttu-id="4bcea-113">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="4bcea-113">The following flags can be set:</span></span>
    
<span data-ttu-id="4bcea-114">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4bcea-114">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="4bcea-115">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="4bcea-115">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="4bcea-116">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="4bcea-116">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="4bcea-117">MSG_SERVICE_UI_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="4bcea-117">MSG_SERVICE_UI_READ_ONLY</span></span> 
  
> <span data-ttu-id="4bcea-118">メッセージ サービスは構成プロパティ シートを表示しますが、ユーザーが変更を有効にしない必要があります。</span><span class="sxs-lookup"><span data-stu-id="4bcea-118">The message service should display its configuration property sheet but not enable the user to change it.</span></span> <span data-ttu-id="4bcea-119">ほとんどのメッセージ サービスでは、このフラグは無視されます。</span><span class="sxs-lookup"><span data-stu-id="4bcea-119">Most message services ignore this flag.</span></span>
    
<span data-ttu-id="4bcea-120">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="4bcea-120">SERVICE_UI_ALLOWED</span></span> 
  
> <span data-ttu-id="4bcea-121">メッセージ サービスは、サービスが完全に構成されていない場合にのみ、構成プロパティ シートを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4bcea-121">The message service should display its configuration property sheet only if the service is not completely configured.</span></span>
    
<span data-ttu-id="4bcea-122">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="4bcea-122">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="4bcea-123">メッセージ サービスは常に構成プロパティ シートを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4bcea-123">The message service must always display its configuration property sheet.</span></span> <span data-ttu-id="4bcea-124">このSERVICE_UI_ALWAYS設定されていない場合、SERVICE_UI_ALLOWED が設定されている場合でも  _、lpProps_ パラメーターのプロパティ値配列から有効な構成情報を使用できない場合は、構成プロパティ シートを表示できます。</span><span class="sxs-lookup"><span data-stu-id="4bcea-124">If SERVICE_UI_ALWAYS is not set, a configuration property sheet can still be displayed if SERVICE_UI_ALLOWED is set and valid configuration information is not available from the property value array in the  _lpProps_ parameter.</span></span> <span data-ttu-id="4bcea-125">プロパティ SERVICE_UI_ALLOWED表示SERVICE_UI_ALWAYS設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4bcea-125">Either SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS must be set for a property sheet to be displayed.</span></span> 
    
 <span data-ttu-id="4bcea-126">_cValues_</span><span class="sxs-lookup"><span data-stu-id="4bcea-126">_cValues_</span></span>
  
> <span data-ttu-id="4bcea-127">[in]lpProps が指す [SPropValue](spropvalue.md) 構造体のプロパティ値  _の数_ です。</span><span class="sxs-lookup"><span data-stu-id="4bcea-127">[in] The count of property values in the [SPropValue](spropvalue.md) structure pointed to by  _lpProps_.</span></span> 
    
 <span data-ttu-id="4bcea-128">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="4bcea-128">_lpProps_</span></span>
  
> <span data-ttu-id="4bcea-129">[in]プロパティ シートに表示するプロパティを表すプロパティ値の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4bcea-129">[in] A pointer to an array of property values that describe the properties to display in the property sheet.</span></span> <span data-ttu-id="4bcea-130">メッセージ サービスをユーザー インターフェイスなしで構成する必要がある場合は  _、lpProps_ パラメーターを NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="4bcea-130">The  _lpProps_ parameter should not be NULL if the message service should be configured without a user interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4bcea-131">戻り値</span><span class="sxs-lookup"><span data-stu-id="4bcea-131">Return value</span></span>

<span data-ttu-id="4bcea-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="4bcea-132">S_OK</span></span> 
  
> <span data-ttu-id="4bcea-133">メッセージ サービスが正常に構成されました。</span><span class="sxs-lookup"><span data-stu-id="4bcea-133">The message service was successfully configured.</span></span>
    
<span data-ttu-id="4bcea-134">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="4bcea-134">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="4bcea-135">メッセージ サービスに固有のエラー。</span><span class="sxs-lookup"><span data-stu-id="4bcea-135">An error specific to a message service.</span></span> <span data-ttu-id="4bcea-136">エラーを [説明する MAPIERROR](mapierror.md) 構造を取得するには、クライアント アプリケーションが [IMsgServiceAdmin::GetLastError メソッドを呼び出す必要](imsgserviceadmin-getlasterror.md) があります。</span><span class="sxs-lookup"><span data-stu-id="4bcea-136">To get the [MAPIERROR](mapierror.md) structure that describes the error, the client application should call the [IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="4bcea-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="4bcea-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="4bcea-138">lpUID が指す _MAPIUID_ は、既存のメッセージ サービスの **MAPIUID** と一致しません。</span><span class="sxs-lookup"><span data-stu-id="4bcea-138">The **MAPIUID** pointed to by  _lpUID_ does not match that of an existing message service.</span></span> 
    
<span data-ttu-id="4bcea-139">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="4bcea-139">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="4bcea-140">メッセージ サービスにエントリ ポイント関数はありません。</span><span class="sxs-lookup"><span data-stu-id="4bcea-140">The message service does not have an entry point function.</span></span>
    
<span data-ttu-id="4bcea-141">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="4bcea-141">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="4bcea-142">ユーザーは、通常、プロパティ シートの [キャンセル] ボタンをクリック **して、操作** を取り消しました。</span><span class="sxs-lookup"><span data-stu-id="4bcea-142">The user canceled the operation, typically by clicking the **Cancel** button in the property sheet.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4bcea-143">注釈</span><span class="sxs-lookup"><span data-stu-id="4bcea-143">Remarks</span></span>

<span data-ttu-id="4bcea-144">**IMsgServiceAdmin::ConfigureMsgService** メソッドを使用すると、構成プロパティ シートの付きまたは指定なしでメッセージ サービスを構成できます。</span><span class="sxs-lookup"><span data-stu-id="4bcea-144">The **IMsgServiceAdmin::ConfigureMsgService** method enables a message service to be configured, with or without a configuration property sheet.</span></span> 
  
<span data-ttu-id="4bcea-145">プロパティ シートを表示せずに構成を許可するには、通常、メッセージ サービスは、必要なすべてのプロパティとオプションのプロパティとその値の定数を含むヘッダー ファイルを準備します。</span><span class="sxs-lookup"><span data-stu-id="4bcea-145">To allow configuration without a property sheet display, message services typically prepare a header file that includes constants for all the required and optional properties and their values.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="4bcea-146">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="4bcea-146">Notes to callers</span></span>

<span data-ttu-id="4bcea-147">構成するメッセージ サービスの **MAPIUID** 構造を取得するには、メッセージ サービス テーブルのメッセージ サービスの行から **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) 列を取得します。</span><span class="sxs-lookup"><span data-stu-id="4bcea-147">To retrieve the **MAPIUID** structure for the message service to configure, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column from the message service's row in the message service table.</span></span> <span data-ttu-id="4bcea-148">詳細については [、「IMsgServiceAdmin::CreateMsgService メソッド」で説明されている手順を参照](imsgserviceadmin-createmsgservice.md) してください。</span><span class="sxs-lookup"><span data-stu-id="4bcea-148">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
<span data-ttu-id="4bcea-149">設定するプロパティ値に関する事前情報がある場合にのみ、ユーザーにプロパティ シートを表示せずにメッセージ サービスを構成できます。</span><span class="sxs-lookup"><span data-stu-id="4bcea-149">You can configure a message service without displaying a property sheet to a user only if you have advance information about the property values to be set.</span></span> <span data-ttu-id="4bcea-150">プロパティ シートを表示せずにメッセージ サービスを構成する場合は  _、lpProps_ パラメーターに有効なプロパティ値を渡し、MSG_SERVICE_UI_READ_ONLY、SERVICE_UI_ALLOWED、または SERVICE_UI_ALWAYS フラグを設定しない。</span><span class="sxs-lookup"><span data-stu-id="4bcea-150">If you are configuring a message service without displaying a property sheet, pass valid property values in the  _lpProps_ parameter and do not set the MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED, or SERVICE_UI_ALWAYS flags.</span></span> 
  
<span data-ttu-id="4bcea-151">プロパティ シートを使用してユーザーから構成情報のすべてまたは一部を受け取る場合は  _、ulFlags_ にSERVICE_UI_ALLOWED設定します。</span><span class="sxs-lookup"><span data-stu-id="4bcea-151">If you receive all or some of the configuration information from the user by way of a property sheet, set SERVICE_UI_ALLOWED in  _ulFlags_.</span></span> <span data-ttu-id="4bcea-152">既存のプロパティ情報のみを使用して既定の設定を確立し、ユーザーが設定を変更できる場合は  _、ulFlags_ で SERVICE_UI_ALWAYSを設定します。</span><span class="sxs-lookup"><span data-stu-id="4bcea-152">If you use existing property information only to establish default settings and the user is able to change the settings, set SERVICE_UI_ALWAYS in  _ulFlags_.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4bcea-153">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="4bcea-153">MFCMAPI reference</span></span>

<span data-ttu-id="4bcea-154">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4bcea-154">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4bcea-155">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="4bcea-155">**File**</span></span>|<span data-ttu-id="4bcea-156">**関数**</span><span class="sxs-lookup"><span data-stu-id="4bcea-156">**Function**</span></span>|<span data-ttu-id="4bcea-157">**コメント**</span><span class="sxs-lookup"><span data-stu-id="4bcea-157">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4bcea-158">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="4bcea-158">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="4bcea-159">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="4bcea-159">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="4bcea-160">MFCMAPI は **、IMsgServiceAdmin::ConfigureMsgService** メソッドを使用して、プロファイルに追加されたサービスを構成します。</span><span class="sxs-lookup"><span data-stu-id="4bcea-160">MFCMAPI uses the **IMsgServiceAdmin::ConfigureMsgService** method to configure a service that has been added to a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4bcea-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="4bcea-161">See also</span></span>



[<span data-ttu-id="4bcea-162">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="4bcea-162">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="4bcea-163">SPropValue</span><span class="sxs-lookup"><span data-stu-id="4bcea-163">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="4bcea-164">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4bcea-164">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


<span data-ttu-id="4bcea-165">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="4bcea-165">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

