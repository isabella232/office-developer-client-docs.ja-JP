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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: f58d0f5cd7dfe74d3859d4f06a41aad6c3a55ac4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800959"
---
# <a name="imsgserviceadminconfiguremsgservice"></a><span data-ttu-id="e8168-103">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="e8168-103">IMsgServiceAdmin::ConfigureMsgService</span></span>

  
  
<span data-ttu-id="e8168-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e8168-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e8168-105">メッセージ サービスを再構成します。</span><span class="sxs-lookup"><span data-stu-id="e8168-105">Reconfigures a message service.</span></span>
  
```cpp
HRESULT ConfigureMsgService(
  LPMAPIUID lpUID,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a><span data-ttu-id="e8168-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="e8168-106">Parameters</span></span>

 <span data-ttu-id="e8168-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="e8168-107">_lpUID_</span></span>
  
> <span data-ttu-id="e8168-108">[in]メッセージ サービス構成の一意の識別子を格納する[MAPIUID](mapiuid.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e8168-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to configure.</span></span> 
    
 <span data-ttu-id="e8168-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="e8168-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="e8168-110">[in]構成のプロパティ シートの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="e8168-110">[in] A handle to the parent window of the configuration property sheet.</span></span>
    
 <span data-ttu-id="e8168-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e8168-111">_ulFlags_</span></span>
  
> <span data-ttu-id="e8168-112">[in]プロパティ シートの表示を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="e8168-112">[in] A bitmask of flags that controls the display of the property sheet.</span></span> <span data-ttu-id="e8168-113">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="e8168-113">The following flags can be set:</span></span>
    
<span data-ttu-id="e8168-114">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e8168-114">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e8168-115">渡された文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="e8168-115">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="e8168-116">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="e8168-116">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="e8168-117">MSG_SERVICE_UI_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="e8168-117">MSG_SERVICE_UI_READ_ONLY</span></span> 
  
> <span data-ttu-id="e8168-118">メッセージ サービスは、構成のプロパティ シートを表示する必要がありますですが、それを変更するユーザーを有効にします。</span><span class="sxs-lookup"><span data-stu-id="e8168-118">The message service should display its configuration property sheet but not enable the user to change it.</span></span> <span data-ttu-id="e8168-119">メッセージ サービスのほとんどは、このフラグを無視します。</span><span class="sxs-lookup"><span data-stu-id="e8168-119">Most message services ignore this flag.</span></span>
    
<span data-ttu-id="e8168-120">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="e8168-120">SERVICE_UI_ALLOWED</span></span> 
  
> <span data-ttu-id="e8168-121">メッセージ サービスは、サービスが完全に構成されていない場合にのみ、構成プロパティ シートを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8168-121">The message service should display its configuration property sheet only if the service is not completely configured.</span></span>
    
<span data-ttu-id="e8168-122">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="e8168-122">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="e8168-123">メッセージ サービスは、[設定] プロパティ シートを常に表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8168-123">The message service must always display its configuration property sheet.</span></span> <span data-ttu-id="e8168-124">SERVICE_UI_ALWAYS が設定されていない SERVICE_UI_ALLOWED を設定し、 _lpProps_パラメーターで、プロパティ値の配列の有効な構成情報がない場合、[設定] プロパティ シートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e8168-124">If SERVICE_UI_ALWAYS is not set, a configuration property sheet can still be displayed if SERVICE_UI_ALLOWED is set and valid configuration information is not available from the property value array in the  _lpProps_ parameter.</span></span> <span data-ttu-id="e8168-125">プロパティ シートを表示するのには、SERVICE_UI_ALLOWED または SERVICE_UI_ALWAYS のいずれかを設定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="e8168-125">Either SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS must be set for a property sheet to be displayed.</span></span> 
    
 <span data-ttu-id="e8168-126">_あう_</span><span class="sxs-lookup"><span data-stu-id="e8168-126">_cValues_</span></span>
  
> <span data-ttu-id="e8168-127">[in]_LpProps_が指す[SPropValue](spropvalue.md)構造体のプロパティ値の数です。</span><span class="sxs-lookup"><span data-stu-id="e8168-127">[in] The count of property values in the [SPropValue](spropvalue.md) structure pointed to by  _lpProps_.</span></span> 
    
 <span data-ttu-id="e8168-128">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="e8168-128">_lpProps_</span></span>
  
> <span data-ttu-id="e8168-129">[in]プロパティ シートに表示するプロパティを記述するプロパティ値の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e8168-129">[in] A pointer to an array of property values that describe the properties to display in the property sheet.</span></span> <span data-ttu-id="e8168-130">ユーザー インターフェイスを持たないメッセージ サービスを構成する必要がある場合、 _lpProps_パラメーターは NULL をしないでください。</span><span class="sxs-lookup"><span data-stu-id="e8168-130">The  _lpProps_ parameter should not be NULL if the message service should be configured without a user interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e8168-131">�߂�l</span><span class="sxs-lookup"><span data-stu-id="e8168-131">Return value</span></span>

<span data-ttu-id="e8168-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="e8168-132">S_OK</span></span> 
  
> <span data-ttu-id="e8168-133">メッセージ サービスが正常に構成されました。</span><span class="sxs-lookup"><span data-stu-id="e8168-133">The message service was successfully configured.</span></span>
    
<span data-ttu-id="e8168-134">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="e8168-134">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="e8168-135">メッセージ サービスに固有のエラーです。</span><span class="sxs-lookup"><span data-stu-id="e8168-135">An error specific to a message service.</span></span> <span data-ttu-id="e8168-136">エラーを説明する[MAPIERROR](mapierror.md)構造体を取得するには、クライアント アプリケーションは、 [IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8168-136">To get the [MAPIERROR](mapierror.md) structure that describes the error, the client application should call the [IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="e8168-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="e8168-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="e8168-138">メッセージの既存のサービスの_lpUID_で示される**MAPIUID**が一致しません。</span><span class="sxs-lookup"><span data-stu-id="e8168-138">The **MAPIUID** pointed to by  _lpUID_ does not match that of an existing message service.</span></span> 
    
<span data-ttu-id="e8168-139">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="e8168-139">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="e8168-140">メッセージ サービスには、エントリ ポイント関数がありません。</span><span class="sxs-lookup"><span data-stu-id="e8168-140">The message service does not have an entry point function.</span></span>
    
<span data-ttu-id="e8168-141">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="e8168-141">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="e8168-142">ユーザー操作がキャンセルされました、通常プロパティ シートで [**キャンセル**] ボタンをクリックするとします。</span><span class="sxs-lookup"><span data-stu-id="e8168-142">The user canceled the operation, typically by clicking the **Cancel** button in the property sheet.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e8168-143">備考</span><span class="sxs-lookup"><span data-stu-id="e8168-143">Remarks</span></span>

<span data-ttu-id="e8168-144">**IMsgServiceAdmin::ConfigureMsgService**メソッドは、構成のプロパティ シートの有無にかかわらず、設定するメッセージ サービスを使用できます。</span><span class="sxs-lookup"><span data-stu-id="e8168-144">The **IMsgServiceAdmin::ConfigureMsgService** method enables a message service to be configured, with or without a configuration property sheet.</span></span> 
  
<span data-ttu-id="e8168-145">プロパティ シートを表示せずに構成できるように、メッセージ サービスは通常、すべての必須および省略可能なプロパティとその値の定数を含むヘッダー ファイルの準備をします。</span><span class="sxs-lookup"><span data-stu-id="e8168-145">To allow configuration without a property sheet display, message services typically prepare a header file that includes constants for all the required and optional properties and their values.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="e8168-146">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="e8168-146">Notes to callers</span></span>

<span data-ttu-id="e8168-147">メッセージ サービスを構成するのには、構造体の**MAPIUID**を取得するには、メッセージ サービスのテーブルの行のメッセージ サービスから**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) の列を取得します。</span><span class="sxs-lookup"><span data-stu-id="e8168-147">To retrieve the **MAPIUID** structure for the message service to configure, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column from the message service's row in the message service table.</span></span> <span data-ttu-id="e8168-148">詳細については、 [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)メソッドで説明する手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e8168-148">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
<span data-ttu-id="e8168-149">設定するプロパティの値に関する情報を事前にある場合にのみユーザーにプロパティ シートを表示せず、メッセージ サービスを構成できます。</span><span class="sxs-lookup"><span data-stu-id="e8168-149">You can configure a message service without displaying a property sheet to a user only if you have advance information about the property values to be set.</span></span> <span data-ttu-id="e8168-150">プロパティ シートを表示せず、メッセージ サービスを構成する場合、 _lpProps_パラメーターに有効なプロパティの値を渡すし、MSG_SERVICE_UI_READ_ONLY、SERVICE_UI_ALLOWED、または SERVICE_UI_ALWAYS フラグを設定しません。</span><span class="sxs-lookup"><span data-stu-id="e8168-150">If you are configuring a message service without displaying a property sheet, pass valid property values in the  _lpProps_ parameter and do not set the MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED, or SERVICE_UI_ALWAYS flags.</span></span> 
  
<span data-ttu-id="e8168-151">プロパティ シートを使用してユーザーの構成情報の一部またはすべてを受信する場合は、 _ulFlags_で SERVICE_UI_ALLOWED を設定します。</span><span class="sxs-lookup"><span data-stu-id="e8168-151">If you receive all or some of the configuration information from the user by way of a property sheet, set SERVICE_UI_ALLOWED in  _ulFlags_.</span></span> <span data-ttu-id="e8168-152">既定の設定を確立するためだけに既存のプロパティ情報を使用すると、ユーザー設定を変更することは、 _ulFlags_で SERVICE_UI_ALWAYS を設定します。</span><span class="sxs-lookup"><span data-stu-id="e8168-152">If you use existing property information only to establish default settings and the user is able to change the settings, set SERVICE_UI_ALWAYS in  _ulFlags_.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e8168-153">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="e8168-153">MFCMAPI reference</span></span>

<span data-ttu-id="e8168-154">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="e8168-154">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e8168-155">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="e8168-155">**File**</span></span>|<span data-ttu-id="e8168-156">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="e8168-156">**Function**</span></span>|<span data-ttu-id="e8168-157">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="e8168-157">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e8168-158">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="e8168-158">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="e8168-159">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="e8168-159">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="e8168-160">MFCMAPI では、 **IMsgServiceAdmin::ConfigureMsgService**メソッドを使用して、プロファイルに追加されたサービスを構成します。</span><span class="sxs-lookup"><span data-stu-id="e8168-160">MFCMAPI uses the **IMsgServiceAdmin::ConfigureMsgService** method to configure a service that has been added to a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e8168-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="e8168-161">See also</span></span>



[<span data-ttu-id="e8168-162">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="e8168-162">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="e8168-163">SPropValue</span><span class="sxs-lookup"><span data-stu-id="e8168-163">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="e8168-164">IMsgServiceAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e8168-164">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


<span data-ttu-id="e8168-165">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="e8168-165">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

