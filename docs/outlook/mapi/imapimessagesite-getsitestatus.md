---
title: IMAPIMessageSiteGetSiteStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetSiteStatus
api_type:
- COM
ms.assetid: 02718898-7857-4e43-8f46-622269f812e6
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9b804728541b0f2a0499bbf0078bfee2e5aed6ee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563808"
---
# <a name="imapimessagesitegetsitestatus"></a><span data-ttu-id="be90c-103">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="be90c-103">IMAPIMessageSite::GetSiteStatus</span></span>

  
  
<span data-ttu-id="be90c-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be90c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be90c-105">メッセージに関するメッセージのサイト オブジェクトの現在のメッセージのサイトの機能に対応する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="be90c-105">Returns information from a message site object about the message site's capabilities for the current message.</span></span>
  
```cpp
HRESULT GetSiteStatus(
  ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a><span data-ttu-id="be90c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="be90c-106">Parameters</span></span>

 <span data-ttu-id="be90c-107">_lpulStatus_</span><span class="sxs-lookup"><span data-stu-id="be90c-107">_lpulStatus_</span></span>
  
> <span data-ttu-id="be90c-108">[out]フラグのビットマスクであり、メッセージの状態に関する情報を提供へのポインター。</span><span class="sxs-lookup"><span data-stu-id="be90c-108">[out] A pointer to a bitmask of flags that provides information about message status.</span></span> <span data-ttu-id="be90c-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="be90c-109">The following flags can be set:</span></span>
    
<span data-ttu-id="be90c-110">VCSTATUS_COPY</span><span class="sxs-lookup"><span data-stu-id="be90c-110">VCSTATUS_COPY</span></span> 
  
> <span data-ttu-id="be90c-111">メッセージをコピーすることができます。</span><span class="sxs-lookup"><span data-stu-id="be90c-111">The message can be copied.</span></span> 
    
<span data-ttu-id="be90c-112">VCSTATUS_DELETE</span><span class="sxs-lookup"><span data-stu-id="be90c-112">VCSTATUS_DELETE</span></span> 
  
> <span data-ttu-id="be90c-113">メッセージを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="be90c-113">The message can be deleted.</span></span>
    
<span data-ttu-id="be90c-114">VCSTATUS_DELETE_IS_MOVE</span><span class="sxs-lookup"><span data-stu-id="be90c-114">VCSTATUS_DELETE_IS_MOVE</span></span> 
  
> <span data-ttu-id="be90c-115">削除されると、メッセージは、メッセージ ・ ストアからすぐに削除されているのではなく、メッセージ ・ ストア内の**削除済みアイテム**フォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="be90c-115">When deleted, a message is moved to a **Deleted Items** folder in its message store instead of being immediately removed from its message store.</span></span> 
    
<span data-ttu-id="be90c-116">VCSTATUS_MOVE</span><span class="sxs-lookup"><span data-stu-id="be90c-116">VCSTATUS_MOVE</span></span> 
  
> <span data-ttu-id="be90c-117">メッセージを移動することができます。</span><span class="sxs-lookup"><span data-stu-id="be90c-117">The message can be moved.</span></span>
    
<span data-ttu-id="be90c-118">VCSTATUS_NEW_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="be90c-118">VCSTATUS_NEW_MESSAGE</span></span> 
  
> <span data-ttu-id="be90c-119">新しいメッセージを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="be90c-119">A new message can be created.</span></span>
    
<span data-ttu-id="be90c-120">VCSTATUS_SAVE</span><span class="sxs-lookup"><span data-stu-id="be90c-120">VCSTATUS_SAVE</span></span> 
  
> <span data-ttu-id="be90c-121">メッセージを保存することができます。</span><span class="sxs-lookup"><span data-stu-id="be90c-121">The message can be saved.</span></span>
    
<span data-ttu-id="be90c-122">VCSTATUS_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="be90c-122">VCSTATUS_SUBMIT</span></span> 
  
> <span data-ttu-id="be90c-123">メッセージを送信することができます。</span><span class="sxs-lookup"><span data-stu-id="be90c-123">The message can be submitted.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="be90c-124">�߂�l</span><span class="sxs-lookup"><span data-stu-id="be90c-124">Return value</span></span>

<span data-ttu-id="be90c-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="be90c-125">S_OK</span></span> 
  
> <span data-ttu-id="be90c-126">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="be90c-126">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="be90c-127">����</span><span class="sxs-lookup"><span data-stu-id="be90c-127">Remarks</span></span>

<span data-ttu-id="be90c-128">フォーム オブジェクトは、現在のメッセージのメッセージ サイト オブジェクトの機能を取得する**IMAPIMessageSite::GetSiteStatus**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="be90c-128">Form objects call the **IMAPIMessageSite::GetSiteStatus** method to obtain the message site object's capabilities for the current message.</span></span> <span data-ttu-id="be90c-129">_LpulStatus_パラメーターで返されるフラグは、メッセージのサイトに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="be90c-129">The flags returned in the  _lpulStatus_ parameter provide information about the message site.</span></span> <span data-ttu-id="be90c-130">通常、フォームは、有効または、フラグが提供する機能に関する情報のサイトのメッセージの実装によって、メニュー コマンドを無効にします。</span><span class="sxs-lookup"><span data-stu-id="be90c-130">Typically, a form enables or disables menu commands, depending on information the flags provide about the capabilities of the message site implementation.</span></span> <span data-ttu-id="be90c-131">新しいメッセージは、 [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)メソッドまたは[IPersistMessage::Load](ipersistmessage-load.md)メソッドによってフォームに読み込まれている場合は、ステータス フラグを選択してください。</span><span class="sxs-lookup"><span data-stu-id="be90c-131">If a new message is loaded into a form by the [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method or the [IPersistMessage::Load](ipersistmessage-load.md) method, the status flags must be checked.</span></span> <span data-ttu-id="be90c-132">いくつかのメッセージ サイト オブジェクト、特に読み取り専用オブジェクトは、メッセージを保存または削除を許可しません。</span><span class="sxs-lookup"><span data-stu-id="be90c-132">Some message site objects, especially read-only objects, do not allow messages to be saved or deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="be90c-133">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="be90c-133">Notes to implementers</span></span>

<span data-ttu-id="be90c-134">**IMAPIMessageSite::GetSiteStatus**メソッドには、どのような操作したり、現在のメッセージに対しては実行できませんを決定するいくつかの計算を実行するクライアント アプリケーションが必要です。</span><span class="sxs-lookup"><span data-stu-id="be90c-134">The **IMAPIMessageSite::GetSiteStatus** method may require the client application to do some calculation to determine what operations can or cannot be performed on the current message.</span></span> <span data-ttu-id="be90c-135">通常、ステータス行に現在のメッセージのメッセージ ストア プロバイダーを探してに関連するまたはどのアクションを決定するのには、ストア プロバイダーのクエリを実行するクライアント アプリケーションはメッセージ ストアを使用して実行できます。</span><span class="sxs-lookup"><span data-stu-id="be90c-135">Typically, that involves looking at the status row for the current message's message store provider, or querying the store provider to determine which actions the client application can perform by using the message store.</span></span> <span data-ttu-id="be90c-136">たとえば、MAPI_DELETE_IS_MOVE フラグを返すかどうかを決定するには、内の**削除済みアイテム**フォルダーがあるかどうかを確認するメッセージ ストア オブジェクトの**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) のプロパティをチェックしますメッセージ ・ ストアです。</span><span class="sxs-lookup"><span data-stu-id="be90c-136">For example, to determine whether to return the MAPI_DELETE_IS_MOVE flag, check the message store object's **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) property to see whether there is a **Deleted Items** folder in the message store.</span></span> 
  
<span data-ttu-id="be90c-137">フォームのサーバーに関連するインターフェイスの一覧は、 [MAPI フォームのインタ フェース](mapi-form-interfaces.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="be90c-137">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="be90c-138">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="be90c-138">MFCMAPI reference</span></span>

<span data-ttu-id="be90c-139">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="be90c-139">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="be90c-140">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="be90c-140">**File**</span></span>|<span data-ttu-id="be90c-141">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="be90c-141">**Function**</span></span>|<span data-ttu-id="be90c-142">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="be90c-142">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="be90c-143">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="be90c-143">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="be90c-144">CMyMAPIFormViewer::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="be90c-144">CMyMAPIFormViewer::GetSiteStatus</span></span>  <br/> |<span data-ttu-id="be90c-145">MFCMAPI では、 **IMAPIMessageSite::GetSiteStatus**メソッドを使用して、指定したサイトのステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="be90c-145">MFCMAPI uses the **IMAPIMessageSite::GetSiteStatus** method to get the status of the specified site.</span></span> <span data-ttu-id="be90c-146">それは、VCSTATUS_NEW_MESSAGE、VCSTATUS_SAVE、または VCSTATUS_SUBMIT を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="be90c-146">It can return VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE, or VCSTATUS_SUBMIT.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="be90c-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="be90c-147">See also</span></span>



[<span data-ttu-id="be90c-148">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="be90c-148">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="be90c-149">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="be90c-149">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="be90c-150">PidTagIpmWastebasketEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="be90c-150">PidTagIpmWastebasketEntryId Canonical Property</span></span>](pidtagipmwastebasketentryid-canonical-property.md)
  
[<span data-ttu-id="be90c-151">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="be90c-151">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


<span data-ttu-id="be90c-152">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="be90c-152">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="be90c-153">MAPI フォーム インターフェイス</span><span class="sxs-lookup"><span data-stu-id="be90c-153">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

