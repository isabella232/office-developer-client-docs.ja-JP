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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6cef03e33abab81a407698b73a007f247ef88194
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407383"
---
# <a name="imsgserviceadmindeletemsgservice"></a><span data-ttu-id="3c696-103">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="3c696-103">IMsgServiceAdmin::DeleteMsgService</span></span>

  
  
<span data-ttu-id="3c696-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c696-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c696-105">メッセージサービスをプロファイルから削除します。</span><span class="sxs-lookup"><span data-stu-id="3c696-105">Deletes a message service from a profile.</span></span>
  
```cpp
HRESULT DeleteMsgService(
  LPMAPIUID lpuid
);
```

## <a name="parameters"></a><span data-ttu-id="3c696-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3c696-106">Parameters</span></span>

 <span data-ttu-id="3c696-107">_lpuid_</span><span class="sxs-lookup"><span data-stu-id="3c696-107">_lpuid_</span></span>
  
> <span data-ttu-id="3c696-108">順番削除するメッセージサービスの一意の識別子を含む[MAPIUID](mapiuid.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3c696-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to delete.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3c696-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="3c696-109">Return value</span></span>

<span data-ttu-id="3c696-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="3c696-110">S_OK</span></span> 
  
> <span data-ttu-id="3c696-111">メッセージサービスが削除されました。</span><span class="sxs-lookup"><span data-stu-id="3c696-111">The message service was deleted.</span></span>
    
<span data-ttu-id="3c696-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="3c696-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="3c696-113">_lpuid_が指す**MAPIUID**が、既存のメッセージサービスと一致しません。</span><span class="sxs-lookup"><span data-stu-id="3c696-113">The **MAPIUID** pointed to by  _lpuid_ does not match an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3c696-114">注釈</span><span class="sxs-lookup"><span data-stu-id="3c696-114">Remarks</span></span>

<span data-ttu-id="3c696-115">**IMsgServiceAdmin::D eletemsgservice**メソッドは、プロファイルからメッセージサービスを削除します。</span><span class="sxs-lookup"><span data-stu-id="3c696-115">The **IMsgServiceAdmin::DeleteMsgService** method deletes a message service from a profile.</span></span> <span data-ttu-id="3c696-116">**DeleteMsgService**は、メッセージサービスに関連するすべてのプロファイルセクションを削除します。</span><span class="sxs-lookup"><span data-stu-id="3c696-116">**DeleteMsgService** removes all profile sections related to the message service.</span></span> 
  
 <span data-ttu-id="3c696-117">**DeleteMsgService**は、次の手順を実行して、メッセージサービスを削除します。</span><span class="sxs-lookup"><span data-stu-id="3c696-117">**DeleteMsgService** performs the following steps to delete the message service:</span></span> 
  
1. <span data-ttu-id="3c696-118">_ulcontext_パラメーターを MSG_SERVICE_DELETE に設定してメッセージサービスのエントリポイント関数を呼び出して、プロファイルセクションが削除されるようにします。</span><span class="sxs-lookup"><span data-stu-id="3c696-118">Calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE before the profile sections are removed.</span></span> <span data-ttu-id="3c696-119">これにより、サービスはサービス固有のタスクを実行できるようになります。</span><span class="sxs-lookup"><span data-stu-id="3c696-119">This allows the service to perform any service-specific tasks.</span></span> 
    
2. <span data-ttu-id="3c696-120">メッセージサービスを削除します。</span><span class="sxs-lookup"><span data-stu-id="3c696-120">Deletes the message service.</span></span>
    
3. <span data-ttu-id="3c696-121">メッセージサービスのプロファイルセクションを削除します。</span><span class="sxs-lookup"><span data-stu-id="3c696-121">Deletes the message service's profile section.</span></span>
    
<span data-ttu-id="3c696-122">サービスが削除された後、メッセージサービスのエントリポイント関数が再度呼び出されることはありません。</span><span class="sxs-lookup"><span data-stu-id="3c696-122">The message service's entry point function is not called again after the service has been deleted.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="3c696-123">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="3c696-123">Notes to callers</span></span>

<span data-ttu-id="3c696-124">削除するメッセージサービスの**MAPIUID**構造を取得するには、メッセージサービステーブルのメッセージサービスの行から**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) プロパティ列を取得します。</span><span class="sxs-lookup"><span data-stu-id="3c696-124">To retrieve the **MAPIUID** structure for the message service to delete, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property column from the message service's row in the message service table.</span></span> <span data-ttu-id="3c696-125">詳細については、 [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md)メソッドに記載されている手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3c696-125">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3c696-126">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="3c696-126">MFCMAPI reference</span></span>

<span data-ttu-id="3c696-127">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3c696-127">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3c696-128">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="3c696-128">**File**</span></span>|<span data-ttu-id="3c696-129">**関数**</span><span class="sxs-lookup"><span data-stu-id="3c696-129">**Function**</span></span>|<span data-ttu-id="3c696-130">**コメント**</span><span class="sxs-lookup"><span data-stu-id="3c696-130">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3c696-131">MsgServiceTableDlg</span><span class="sxs-lookup"><span data-stu-id="3c696-131">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="3c696-132">CMsgServiceTableDlg:: OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="3c696-132">CMsgServiceTableDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="3c696-133">mfcmapi は、 **IMsgServiceAdmin::D eletemsgservice**メソッドを使用して、選択されているサービスを削除します。</span><span class="sxs-lookup"><span data-stu-id="3c696-133">MFCMAPI uses the **IMsgServiceAdmin::DeleteMsgService** method to delete the selected service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3c696-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="3c696-134">See also</span></span>



[<span data-ttu-id="3c696-135">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="3c696-135">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="3c696-136">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3c696-136">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


<span data-ttu-id="3c696-137">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="3c696-137">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

