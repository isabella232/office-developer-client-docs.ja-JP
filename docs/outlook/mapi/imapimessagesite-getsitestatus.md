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
# <a name="imapimessagesitegetsitestatus"></a><span data-ttu-id="33721-103">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="33721-103">IMAPIMessageSite::GetSiteStatus</span></span>

  
  
<span data-ttu-id="33721-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33721-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33721-105">現在のメッセージのメッセージサイトの機能に関する情報をメッセージサイトオブジェクトから返します。</span><span class="sxs-lookup"><span data-stu-id="33721-105">Returns information from a message site object about the message site's capabilities for the current message.</span></span>
  
```cpp
HRESULT GetSiteStatus(
  ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a><span data-ttu-id="33721-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="33721-106">Parameters</span></span>

 <span data-ttu-id="33721-107">_lアウト状態_</span><span class="sxs-lookup"><span data-stu-id="33721-107">_lpulStatus_</span></span>
  
> <span data-ttu-id="33721-108">読み上げメッセージの状態に関する情報を提供するフラグのビットマスクへのポインター。</span><span class="sxs-lookup"><span data-stu-id="33721-108">[out] A pointer to a bitmask of flags that provides information about message status.</span></span> <span data-ttu-id="33721-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="33721-109">The following flags can be set:</span></span>
    
<span data-ttu-id="33721-110">VCSTATUS_COPY</span><span class="sxs-lookup"><span data-stu-id="33721-110">VCSTATUS_COPY</span></span> 
  
> <span data-ttu-id="33721-111">メッセージをコピーできます。</span><span class="sxs-lookup"><span data-stu-id="33721-111">The message can be copied.</span></span> 
    
<span data-ttu-id="33721-112">VCSTATUS_DELETE</span><span class="sxs-lookup"><span data-stu-id="33721-112">VCSTATUS_DELETE</span></span> 
  
> <span data-ttu-id="33721-113">メッセージを削除できます。</span><span class="sxs-lookup"><span data-stu-id="33721-113">The message can be deleted.</span></span>
    
<span data-ttu-id="33721-114">VCSTATUS_DELETE_IS_MOVE</span><span class="sxs-lookup"><span data-stu-id="33721-114">VCSTATUS_DELETE_IS_MOVE</span></span> 
  
> <span data-ttu-id="33721-115">削除されると、メッセージはメッセージストアからすぐに削除されるのではなく、メッセージストア内の**削除済みアイテム**フォルダーに移動されます。</span><span class="sxs-lookup"><span data-stu-id="33721-115">When deleted, a message is moved to a **Deleted Items** folder in its message store instead of being immediately removed from its message store.</span></span> 
    
<span data-ttu-id="33721-116">VCSTATUS_MOVE</span><span class="sxs-lookup"><span data-stu-id="33721-116">VCSTATUS_MOVE</span></span> 
  
> <span data-ttu-id="33721-117">メッセージを移動できます。</span><span class="sxs-lookup"><span data-stu-id="33721-117">The message can be moved.</span></span>
    
<span data-ttu-id="33721-118">VCSTATUS_NEW_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="33721-118">VCSTATUS_NEW_MESSAGE</span></span> 
  
> <span data-ttu-id="33721-119">新しいメッセージを作成できます。</span><span class="sxs-lookup"><span data-stu-id="33721-119">A new message can be created.</span></span>
    
<span data-ttu-id="33721-120">VCSTATUS_SAVE</span><span class="sxs-lookup"><span data-stu-id="33721-120">VCSTATUS_SAVE</span></span> 
  
> <span data-ttu-id="33721-121">メッセージを保存できます。</span><span class="sxs-lookup"><span data-stu-id="33721-121">The message can be saved.</span></span>
    
<span data-ttu-id="33721-122">VCSTATUS_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="33721-122">VCSTATUS_SUBMIT</span></span> 
  
> <span data-ttu-id="33721-123">メッセージを送信できます。</span><span class="sxs-lookup"><span data-stu-id="33721-123">The message can be submitted.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="33721-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="33721-124">Return value</span></span>

<span data-ttu-id="33721-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="33721-125">S_OK</span></span> 
  
> <span data-ttu-id="33721-126">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="33721-126">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="33721-127">注釈</span><span class="sxs-lookup"><span data-stu-id="33721-127">Remarks</span></span>

<span data-ttu-id="33721-128">Form オブジェクトは**IMAPIMessageSite:: getsitestatus**メソッドを呼び出して、現在のメッセージのメッセージサイトオブジェクトの機能を取得します。</span><span class="sxs-lookup"><span data-stu-id="33721-128">Form objects call the **IMAPIMessageSite::GetSiteStatus** method to obtain the message site object's capabilities for the current message.</span></span> <span data-ttu-id="33721-129">_lアウト status_パラメーターで返されるフラグは、メッセージサイトに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="33721-129">The flags returned in the  _lpulStatus_ parameter provide information about the message site.</span></span> <span data-ttu-id="33721-130">通常、フォームは、フラグがメッセージサイト実装の機能について提供する情報に応じて、メニューコマンドを有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="33721-130">Typically, a form enables or disables menu commands, depending on information the flags provide about the capabilities of the message site implementation.</span></span> <span data-ttu-id="33721-131">[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md)メソッドまたは[IPersistMessage:: Load](ipersistmessage-load.md)メソッドによってフォームに新しいメッセージが読み込まれた場合は、状態フラグをチェックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="33721-131">If a new message is loaded into a form by the [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method or the [IPersistMessage::Load](ipersistmessage-load.md) method, the status flags must be checked.</span></span> <span data-ttu-id="33721-132">一部のメッセージサイトオブジェクト (特に読み取り専用オブジェクト) では、メッセージを保存または削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="33721-132">Some message site objects, especially read-only objects, do not allow messages to be saved or deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="33721-133">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="33721-133">Notes to implementers</span></span>

<span data-ttu-id="33721-134">**IMAPIMessageSite:: getsitestatus**メソッドでは、現在のメッセージに対して実行可能な操作と実行できない操作を決定するために、クライアントアプリケーションが計算を実行することが必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="33721-134">The **IMAPIMessageSite::GetSiteStatus** method may require the client application to do some calculation to determine what operations can or cannot be performed on the current message.</span></span> <span data-ttu-id="33721-135">通常は、現在のメッセージのメッセージストアプロバイダーの状態行を参照するか、ストアプロバイダーに照会して、メッセージストアを使用してクライアントアプリケーションが実行できるアクションを確認します。</span><span class="sxs-lookup"><span data-stu-id="33721-135">Typically, that involves looking at the status row for the current message's message store provider, or querying the store provider to determine which actions the client application can perform by using the message store.</span></span> <span data-ttu-id="33721-136">たとえば、MAPI_DELETE_IS_MOVE フラグを返すかどうかを判断するには、メッセージストアオブジェクトの**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) プロパティを調べて、**削除済みアイテム**フォルダーがあるかどうかを確認します。メッセージストア。</span><span class="sxs-lookup"><span data-stu-id="33721-136">For example, to determine whether to return the MAPI_DELETE_IS_MOVE flag, check the message store object's **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) property to see whether there is a **Deleted Items** folder in the message store.</span></span> 
  
<span data-ttu-id="33721-137">フォームサーバーに関連するインターフェイスの一覧については、「 [MAPI フォームインターフェイス](mapi-form-interfaces.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="33721-137">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="33721-138">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="33721-138">MFCMAPI reference</span></span>

<span data-ttu-id="33721-139">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="33721-139">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="33721-140">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="33721-140">**File**</span></span>|<span data-ttu-id="33721-141">**関数**</span><span class="sxs-lookup"><span data-stu-id="33721-141">**Function**</span></span>|<span data-ttu-id="33721-142">**コメント**</span><span class="sxs-lookup"><span data-stu-id="33721-142">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="33721-143">MyMAPIFormViewer</span><span class="sxs-lookup"><span data-stu-id="33721-143">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="33721-144">cmymapiformviewer:: getsitestatus</span><span class="sxs-lookup"><span data-stu-id="33721-144">CMyMAPIFormViewer::GetSiteStatus</span></span>  <br/> |<span data-ttu-id="33721-145">mfcmapi は、 **IMAPIMessageSite:: getsitestatus**メソッドを使用して、指定されたサイトの状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="33721-145">MFCMAPI uses the **IMAPIMessageSite::GetSiteStatus** method to get the status of the specified site.</span></span> <span data-ttu-id="33721-146">VCSTATUS_NEW_MESSAGE、VCSTATUS_SAVE、または VCSTATUS_SUBMIT を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="33721-146">It can return VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE, or VCSTATUS_SUBMIT.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="33721-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="33721-147">See also</span></span>



[<span data-ttu-id="33721-148">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="33721-148">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="33721-149">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="33721-149">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="33721-150">PidTagIpmWastebasketEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="33721-150">PidTagIpmWastebasketEntryId Canonical Property</span></span>](pidtagipmwastebasketentryid-canonical-property.md)
  
[<span data-ttu-id="33721-151">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="33721-151">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


<span data-ttu-id="33721-152">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="33721-152">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="33721-153">MAPI フォームインターフェイス</span><span class="sxs-lookup"><span data-stu-id="33721-153">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

