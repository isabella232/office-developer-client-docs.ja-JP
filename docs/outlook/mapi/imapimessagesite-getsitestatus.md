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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ab4a06a20c71943f9b649d8f22377f59223e9717
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430127"
---
# <a name="imapimessagesitegetsitestatus"></a><span data-ttu-id="57b8c-103">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="57b8c-103">IMAPIMessageSite::GetSiteStatus</span></span>

  
  
<span data-ttu-id="57b8c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57b8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57b8c-105">現在のメッセージに対するメッセージ サイトの機能に関する情報をメッセージ サイト オブジェクトから返します。</span><span class="sxs-lookup"><span data-stu-id="57b8c-105">Returns information from a message site object about the message site's capabilities for the current message.</span></span>
  
```cpp
HRESULT GetSiteStatus(
  ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a><span data-ttu-id="57b8c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="57b8c-106">Parameters</span></span>

 <span data-ttu-id="57b8c-107">_lpulStatus_</span><span class="sxs-lookup"><span data-stu-id="57b8c-107">_lpulStatus_</span></span>
  
> <span data-ttu-id="57b8c-108">[out]メッセージの状態に関する情報を提供するフラグのビットマスクへのポインター。</span><span class="sxs-lookup"><span data-stu-id="57b8c-108">[out] A pointer to a bitmask of flags that provides information about message status.</span></span> <span data-ttu-id="57b8c-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="57b8c-109">The following flags can be set:</span></span>
    
<span data-ttu-id="57b8c-110">VCSTATUS_COPY</span><span class="sxs-lookup"><span data-stu-id="57b8c-110">VCSTATUS_COPY</span></span> 
  
> <span data-ttu-id="57b8c-111">メッセージはコピーできます。</span><span class="sxs-lookup"><span data-stu-id="57b8c-111">The message can be copied.</span></span> 
    
<span data-ttu-id="57b8c-112">VCSTATUS_DELETE</span><span class="sxs-lookup"><span data-stu-id="57b8c-112">VCSTATUS_DELETE</span></span> 
  
> <span data-ttu-id="57b8c-113">メッセージは削除できます。</span><span class="sxs-lookup"><span data-stu-id="57b8c-113">The message can be deleted.</span></span>
    
<span data-ttu-id="57b8c-114">VCSTATUS_DELETE_IS_MOVE</span><span class="sxs-lookup"><span data-stu-id="57b8c-114">VCSTATUS_DELETE_IS_MOVE</span></span> 
  
> <span data-ttu-id="57b8c-115">削除されると、メッセージはメッセージ ストアからすぐに削除されるのではなく、メッセージ ストア内の削除済みアイテム フォルダーに移動されます。</span><span class="sxs-lookup"><span data-stu-id="57b8c-115">When deleted, a message is moved to a **Deleted Items** folder in its message store instead of being immediately removed from its message store.</span></span> 
    
<span data-ttu-id="57b8c-116">VCSTATUS_MOVE</span><span class="sxs-lookup"><span data-stu-id="57b8c-116">VCSTATUS_MOVE</span></span> 
  
> <span data-ttu-id="57b8c-117">メッセージは移動できます。</span><span class="sxs-lookup"><span data-stu-id="57b8c-117">The message can be moved.</span></span>
    
<span data-ttu-id="57b8c-118">VCSTATUS_NEW_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="57b8c-118">VCSTATUS_NEW_MESSAGE</span></span> 
  
> <span data-ttu-id="57b8c-119">新しいメッセージを作成できます。</span><span class="sxs-lookup"><span data-stu-id="57b8c-119">A new message can be created.</span></span>
    
<span data-ttu-id="57b8c-120">VCSTATUS_SAVE</span><span class="sxs-lookup"><span data-stu-id="57b8c-120">VCSTATUS_SAVE</span></span> 
  
> <span data-ttu-id="57b8c-121">メッセージを保存できます。</span><span class="sxs-lookup"><span data-stu-id="57b8c-121">The message can be saved.</span></span>
    
<span data-ttu-id="57b8c-122">VCSTATUS_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="57b8c-122">VCSTATUS_SUBMIT</span></span> 
  
> <span data-ttu-id="57b8c-123">メッセージは送信できます。</span><span class="sxs-lookup"><span data-stu-id="57b8c-123">The message can be submitted.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="57b8c-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="57b8c-124">Return value</span></span>

<span data-ttu-id="57b8c-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="57b8c-125">S_OK</span></span> 
  
> <span data-ttu-id="57b8c-126">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="57b8c-126">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="57b8c-127">注釈</span><span class="sxs-lookup"><span data-stu-id="57b8c-127">Remarks</span></span>

<span data-ttu-id="57b8c-128">フォーム オブジェクトは **IMAPIMessageSite::GetSiteStatus** メソッドを呼び出して、現在のメッセージに対するメッセージ サイト オブジェクトの機能を取得します。</span><span class="sxs-lookup"><span data-stu-id="57b8c-128">Form objects call the **IMAPIMessageSite::GetSiteStatus** method to obtain the message site object's capabilities for the current message.</span></span> <span data-ttu-id="57b8c-129">_lpulStatus_ パラメーターで返されるフラグは、メッセージ サイトに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="57b8c-129">The flags returned in the  _lpulStatus_ parameter provide information about the message site.</span></span> <span data-ttu-id="57b8c-130">通常、フォームは、メッセージ サイトの実装の機能に関するフラグによって提供される情報に応じて、メニュー コマンドを有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="57b8c-130">Typically, a form enables or disables menu commands, depending on information the flags provide about the capabilities of the message site implementation.</span></span> <span data-ttu-id="57b8c-131">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)メソッドまたは[IPersistMessage::Load](ipersistmessage-load.md)メソッドによって新しいメッセージがフォームに読み込まれる場合は、状態フラグをチェックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="57b8c-131">If a new message is loaded into a form by the [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method or the [IPersistMessage::Load](ipersistmessage-load.md) method, the status flags must be checked.</span></span> <span data-ttu-id="57b8c-132">一部のメッセージ サイト オブジェクト (特に読み取り専用オブジェクト) では、メッセージを保存または削除できません。</span><span class="sxs-lookup"><span data-stu-id="57b8c-132">Some message site objects, especially read-only objects, do not allow messages to be saved or deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="57b8c-133">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="57b8c-133">Notes to implementers</span></span>

<span data-ttu-id="57b8c-134">**IMAPIMessageSite::GetSiteStatus** メソッドでは、現在のメッセージに対して実行できる操作または実行できない操作を決定するために、クライアント アプリケーションが何らかの計算を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57b8c-134">The **IMAPIMessageSite::GetSiteStatus** method may require the client application to do some calculation to determine what operations can or cannot be performed on the current message.</span></span> <span data-ttu-id="57b8c-135">通常、現在のメッセージのメッセージ ストア プロバイダーの状態行を確認するか、ストア プロバイダーにクエリを実行して、メッセージ ストアを使用してクライアント アプリケーションが実行できるアクションを決定します。</span><span class="sxs-lookup"><span data-stu-id="57b8c-135">Typically, that involves looking at the status row for the current message's message store provider, or querying the store provider to determine which actions the client application can perform by using the message store.</span></span> <span data-ttu-id="57b8c-136">たとえば、MAPI_DELETE_IS_MOVE フラグを返すかどうかを判断するには、メッセージ ストア オブジェクトの **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId)](pidtagipmwastebasketentryid-canonical-property.md)プロパティを調して、メッセージ ストアに **Deleted Items** フォルダーが含されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="57b8c-136">For example, to determine whether to return the MAPI_DELETE_IS_MOVE flag, check the message store object's **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) property to see whether there is a **Deleted Items** folder in the message store.</span></span> 
  
<span data-ttu-id="57b8c-137">フォーム サーバーに関連するインターフェイスの一覧については [、「MAPI フォーム インターフェイス」を参照してください](mapi-form-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="57b8c-137">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="57b8c-138">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="57b8c-138">MFCMAPI reference</span></span>

<span data-ttu-id="57b8c-139">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="57b8c-139">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="57b8c-140">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="57b8c-140">**File**</span></span>|<span data-ttu-id="57b8c-141">**関数**</span><span class="sxs-lookup"><span data-stu-id="57b8c-141">**Function**</span></span>|<span data-ttu-id="57b8c-142">**コメント**</span><span class="sxs-lookup"><span data-stu-id="57b8c-142">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="57b8c-143">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="57b8c-143">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="57b8c-144">CMyMAPIFormViewer::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="57b8c-144">CMyMAPIFormViewer::GetSiteStatus</span></span>  <br/> |<span data-ttu-id="57b8c-145">MFCMAPI は **IMAPIMessageSite::GetSiteStatus** メソッドを使用して、指定されたサイトの状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="57b8c-145">MFCMAPI uses the **IMAPIMessageSite::GetSiteStatus** method to get the status of the specified site.</span></span> <span data-ttu-id="57b8c-146">このメソッドは、VCSTATUS_NEW_MESSAGE、VCSTATUS_SAVE、またはVCSTATUS_SUBMIT。</span><span class="sxs-lookup"><span data-stu-id="57b8c-146">It can return VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE, or VCSTATUS_SUBMIT.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="57b8c-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="57b8c-147">See also</span></span>



[<span data-ttu-id="57b8c-148">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="57b8c-148">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="57b8c-149">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="57b8c-149">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="57b8c-150">PidTagIpmWastebasketEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="57b8c-150">PidTagIpmWastebasketEntryId Canonical Property</span></span>](pidtagipmwastebasketentryid-canonical-property.md)
  
[<span data-ttu-id="57b8c-151">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="57b8c-151">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


<span data-ttu-id="57b8c-152">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="57b8c-152">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="57b8c-153">MAPI フォーム インターフェイス</span><span class="sxs-lookup"><span data-stu-id="57b8c-153">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

