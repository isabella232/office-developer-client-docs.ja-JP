---
title: IMsgServiceAdminDeleteMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.DeleteMsgService
api_type:
- COM
ms.assetid: 3a6b34eb-9d46-488f-8d02-91b27c35de67
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e0d3d669982bee309901f913612ac1fb1622e60a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571144"
---
# <a name="imsgserviceadmindeletemsgservice"></a><span data-ttu-id="ebfee-103">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="ebfee-103">IMsgServiceAdmin::DeleteMsgService</span></span>

  
  
<span data-ttu-id="ebfee-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ebfee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ebfee-105">メッセージ サービスをプロファイルから削除します。</span><span class="sxs-lookup"><span data-stu-id="ebfee-105">Deletes a message service from a profile.</span></span>
  
```cpp
HRESULT DeleteMsgService(
  LPMAPIUID lpuid
);
```

## <a name="parameters"></a><span data-ttu-id="ebfee-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ebfee-106">Parameters</span></span>

 <span data-ttu-id="ebfee-107">_lpuid_</span><span class="sxs-lookup"><span data-stu-id="ebfee-107">_lpuid_</span></span>
  
> <span data-ttu-id="ebfee-108">[in]削除するメッセージ サービスの一意の識別子を格納する[MAPIUID](mapiuid.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ebfee-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to delete.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ebfee-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ebfee-109">Return value</span></span>

<span data-ttu-id="ebfee-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="ebfee-110">S_OK</span></span> 
  
> <span data-ttu-id="ebfee-111">メッセージ サービスが削除されました。</span><span class="sxs-lookup"><span data-stu-id="ebfee-111">The message service was deleted.</span></span>
    
<span data-ttu-id="ebfee-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ebfee-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ebfee-113">_Lpuid_で指定された**MAPIUID**では、既存のメッセージ サービスが一致しません。</span><span class="sxs-lookup"><span data-stu-id="ebfee-113">The **MAPIUID** pointed to by  _lpuid_ does not match an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ebfee-114">注釈</span><span class="sxs-lookup"><span data-stu-id="ebfee-114">Remarks</span></span>

<span data-ttu-id="ebfee-115">**IMsgServiceAdmin::DeleteMsgService**メソッドは、メッセージ サービスをプロファイルから削除します。</span><span class="sxs-lookup"><span data-stu-id="ebfee-115">The **IMsgServiceAdmin::DeleteMsgService** method deletes a message service from a profile.</span></span> <span data-ttu-id="ebfee-116">**DeleteMsgService**は、メッセージ サービスに関連するすべてのプロファイル セクションを削除します。</span><span class="sxs-lookup"><span data-stu-id="ebfee-116">**DeleteMsgService** removes all profile sections related to the message service.</span></span> 
  
 <span data-ttu-id="ebfee-117">**DeleteMsgService**は、メッセージ サービスを削除するのには次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ebfee-117">**DeleteMsgService** performs the following steps to delete the message service:</span></span> 
  
1. <span data-ttu-id="ebfee-118">プロファイルのセクションを削除する前に MSG_SERVICE_DELETE を設定する_ulContext_パラメーターを使用して、メッセージ サービスのエントリ ポイント関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ebfee-118">Calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE before the profile sections are removed.</span></span> <span data-ttu-id="ebfee-119">これにより、サービスに固有のタスクを実行するサービスです。</span><span class="sxs-lookup"><span data-stu-id="ebfee-119">This allows the service to perform any service-specific tasks.</span></span> 
    
2. <span data-ttu-id="ebfee-120">メッセージ サービスを削除します。</span><span class="sxs-lookup"><span data-stu-id="ebfee-120">Deletes the message service.</span></span>
    
3. <span data-ttu-id="ebfee-121">メッセージ サービスのプロファイル セクションを削除します。</span><span class="sxs-lookup"><span data-stu-id="ebfee-121">Deletes the message service's profile section.</span></span>
    
<span data-ttu-id="ebfee-122">サービスが削除された後、メッセージ サービスのエントリ ポイント関数は再び呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="ebfee-122">The message service's entry point function is not called again after the service has been deleted.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="ebfee-123">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="ebfee-123">Notes to callers</span></span>

<span data-ttu-id="ebfee-124">メッセージ サービスを削除するのには、 **MAPIUID**構造体を取得するには、メッセージ サービスのテーブルの行のメッセージ サービスから**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) のプロパティの列を取得します。</span><span class="sxs-lookup"><span data-stu-id="ebfee-124">To retrieve the **MAPIUID** structure for the message service to delete, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property column from the message service's row in the message service table.</span></span> <span data-ttu-id="ebfee-125">詳細については、 [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)メソッドで説明する手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ebfee-125">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ebfee-126">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="ebfee-126">MFCMAPI reference</span></span>

<span data-ttu-id="ebfee-127">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="ebfee-127">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ebfee-128">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="ebfee-128">**File**</span></span>|<span data-ttu-id="ebfee-129">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="ebfee-129">**Function**</span></span>|<span data-ttu-id="ebfee-130">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="ebfee-130">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ebfee-131">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="ebfee-131">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="ebfee-132">CMsgServiceTableDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="ebfee-132">CMsgServiceTableDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="ebfee-133">MFCMAPI では、 **IMsgServiceAdmin::DeleteMsgService**メソッドを使用して、選択したサービスを削除します。</span><span class="sxs-lookup"><span data-stu-id="ebfee-133">MFCMAPI uses the **IMsgServiceAdmin::DeleteMsgService** method to delete the selected service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ebfee-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="ebfee-134">See also</span></span>



[<span data-ttu-id="ebfee-135">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="ebfee-135">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="ebfee-136">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ebfee-136">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


<span data-ttu-id="ebfee-137">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="ebfee-137">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

