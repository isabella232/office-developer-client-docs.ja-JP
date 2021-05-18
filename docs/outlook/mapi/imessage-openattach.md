---
title: IMessageOpenAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.OpenAttach
api_type:
- COM
ms.assetid: b680f5a7-0df3-4e7b-bf3b-f149eb42be8d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e0c3747b48526b715f976e7bf3c142097c85f29a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405899"
---
# <a name="imessageopenattach"></a><span data-ttu-id="637a3-103">IMessage::OpenAttach</span><span class="sxs-lookup"><span data-stu-id="637a3-103">IMessage::OpenAttach</span></span>

  
  
<span data-ttu-id="637a3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="637a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="637a3-105">添付ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="637a3-105">Opens an attachment.</span></span> 
  
```cpp
HRESULT OpenAttach(
  ULONG ulAttachmentNum,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a><span data-ttu-id="637a3-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="637a3-106">Parameters</span></span>

 <span data-ttu-id="637a3-107">_ulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="637a3-107">_ulAttachmentNum_</span></span>
  
> <span data-ttu-id="637a3-108">[in]添付ファイルのプロパティ ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md) **)** プロパティに格納されている、開く添付PR_ATTACH_NUMインデックス番号。</span><span class="sxs-lookup"><span data-stu-id="637a3-108">[in] Index number of the attachment to open, as stored in the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span> <span data-ttu-id="637a3-109">このインデックス番号は、メッセージ内の添付ファイルを一意に識別し、メッセージのコンテキストでのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="637a3-109">This index number uniquely identifies the attachment in the message and is valid only in the context of the message.</span></span>
    
 <span data-ttu-id="637a3-110">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="637a3-110">_lpInterface_</span></span>
  
> <span data-ttu-id="637a3-111">[in]添付ファイルへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="637a3-111">[in] Pointer to the interface identifier (IID) representing the interface to be used to access the attachment.</span></span> <span data-ttu-id="637a3-112">NULL を渡すと、添付ファイルの標準インターフェイス **(IAttach)** が返されます。</span><span class="sxs-lookup"><span data-stu-id="637a3-112">Passing NULL results in the attachment's standard interface, or **IAttach**, being returned.</span></span> 
    
 <span data-ttu-id="637a3-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="637a3-113">_ulFlags_</span></span>
  
> <span data-ttu-id="637a3-114">[in]添付ファイルの開き方を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="637a3-114">[in] Bitmask of flags that controls how the attachment is opened.</span></span> <span data-ttu-id="637a3-115">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="637a3-115">The following flags can be set:</span></span> 
    
<span data-ttu-id="637a3-116">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="637a3-116">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="637a3-117">ユーザーに許可される最大ネットワークアクセス許可と最大クライアント アプリケーション アクセス権を使用して添付ファイルを開く要求。</span><span class="sxs-lookup"><span data-stu-id="637a3-117">Requests that the attachment be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="637a3-118">たとえば、クライアントに読み取り/書き込みアクセス許可がある場合、添付ファイルを読み取り/書き込みアクセス許可で開く必要があります。クライアントに読み取り専用アクセス権がある場合は、読み取り専用アクセスで添付ファイルを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="637a3-118">For example, if the client has read/write permission, the attachment should be opened with read/write permission; if the client has read-only access, the attachment should be opened with read-only access.</span></span> 
    
<span data-ttu-id="637a3-119">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="637a3-119">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="637a3-120">**OpenAttach が正常** に返されるのを許可します。おそらく、添付ファイルが呼び出し元のクライアントで完全に利用できる前に。</span><span class="sxs-lookup"><span data-stu-id="637a3-120">Allows **OpenAttach** to return successfully, possibly before the attachment is fully available to the calling client.</span></span> <span data-ttu-id="637a3-121">添付ファイルを使用できない場合は、後続の呼び出しでエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="637a3-121">If the attachment is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="637a3-122">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="637a3-122">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="637a3-123">読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="637a3-123">Requests read/write permission.</span></span> <span data-ttu-id="637a3-124">既定では、添付ファイルは読み取り専用アクセスで開かれません。クライアントは、読み取り/書き込みアクセス許可が付与されているという前提で動作しません。</span><span class="sxs-lookup"><span data-stu-id="637a3-124">By default, attachments are opened with read-only access, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="637a3-125">_lppAttach_</span><span class="sxs-lookup"><span data-stu-id="637a3-125">_lppAttach_</span></span>
  
> <span data-ttu-id="637a3-126">[out]開いている添付ファイルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="637a3-126">[out] Pointer to a pointer to the open attachment.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="637a3-127">戻り値</span><span class="sxs-lookup"><span data-stu-id="637a3-127">Return value</span></span>

<span data-ttu-id="637a3-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="637a3-128">S_OK</span></span> 
  
> <span data-ttu-id="637a3-129">添付ファイルが正常に開かされました。</span><span class="sxs-lookup"><span data-stu-id="637a3-129">The attachment was successfully opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="637a3-130">注釈</span><span class="sxs-lookup"><span data-stu-id="637a3-130">Remarks</span></span>

<span data-ttu-id="637a3-131">**IMessage::OpenAttach メソッドは**、メッセージの添付ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="637a3-131">The **IMessage::OpenAttach** method opens a message's attachment.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="637a3-132">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="637a3-132">Notes to callers</span></span>

<span data-ttu-id="637a3-133">添付ファイルを開くには、添付ファイル番号または添付ファイルプロパティに **アクセスPR_ATTACH_NUM** 必要があります。</span><span class="sxs-lookup"><span data-stu-id="637a3-133">To open an attachment, you must have access to its attachment number or **PR_ATTACH_NUM** property.</span></span> <span data-ttu-id="637a3-134">[IMessage::GetAttachmentTable](imessage-getattachmenttable.md)を呼び出して、メッセージの添付ファイル テーブルを取得し、開く添付ファイルを表す行を探します。</span><span class="sxs-lookup"><span data-stu-id="637a3-134">Call [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) to retrieve the message's attachment table and locate the row that represents the attachment to be opened.</span></span> <span data-ttu-id="637a3-135">詳細 [については、「添付ファイルを開く](opening-an-attachment.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="637a3-135">See [Opening an Attachment](opening-an-attachment.md) for more information.</span></span> 
  
<span data-ttu-id="637a3-136">1 つの添付ファイルを複数回開かれません。結果は未定義であり、メッセージ ストア プロバイダーに依存します。</span><span class="sxs-lookup"><span data-stu-id="637a3-136">Do not try to open one attachment multiple times; the results are undefined and dependent on the message store provider.</span></span>
  
<span data-ttu-id="637a3-137">既定の読み取り専用モードではなく、読み取り/書き込みモードで添付ファイルを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="637a3-137">You can request that the attachment be opened in read/write mode, instead of the default read-only mode.</span></span> <span data-ttu-id="637a3-138">ただし、添付ファイルを実際に読み取り/書き込みモードで開くかどうかは、メッセージ ストア プロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="637a3-138">However, whether the attachment will actually be opened in read/write mode is up to the message store provider.</span></span> <span data-ttu-id="637a3-139">使用可能な場合は、添付ファイルの変更、エラーの処理の準備、または添付ファイルの **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) プロパティを取得して付与されたアクセスのレベルを確認できます。</span><span class="sxs-lookup"><span data-stu-id="637a3-139">You can either attempt to modify the attachment, preparing to handle possible failure, or check the level of access that was granted by retrieving the attachment's **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property, if it is available.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="637a3-140">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="637a3-140">MFCMAPI reference</span></span>

<span data-ttu-id="637a3-141">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="637a3-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="637a3-142">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="637a3-142">**File**</span></span>|<span data-ttu-id="637a3-143">**関数**</span><span class="sxs-lookup"><span data-stu-id="637a3-143">**Function**</span></span>|<span data-ttu-id="637a3-144">**コメント**</span><span class="sxs-lookup"><span data-stu-id="637a3-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="637a3-145">AttachmentsDlg.cpp 使用する</span><span class="sxs-lookup"><span data-stu-id="637a3-145">AttachmentsDlg.cpp Used to</span></span>  <br/> |<span data-ttu-id="637a3-146">CAttachmentsDlg::OpenItemProp</span><span class="sxs-lookup"><span data-stu-id="637a3-146">CAttachmentsDlg::OpenItemProp</span></span>  <br/> |<span data-ttu-id="637a3-147">MFCMAPI は **、IMessage::OpenAttach** メソッドを使用して添付ファイル オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="637a3-147">MFCMAPI uses the **IMessage::OpenAttach** method to open attachment objects,</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="637a3-148">関連項目</span><span class="sxs-lookup"><span data-stu-id="637a3-148">See also</span></span>



[<span data-ttu-id="637a3-149">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="637a3-149">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


<span data-ttu-id="637a3-150">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="637a3-150">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

