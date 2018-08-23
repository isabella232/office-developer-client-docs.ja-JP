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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c702e4063bf5e5a06a9e476a02172a780c7e326a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800892"
---
# <a name="imessageopenattach"></a><span data-ttu-id="f7e24-103">IMessage::OpenAttach</span><span class="sxs-lookup"><span data-stu-id="f7e24-103">IMessage::OpenAttach</span></span>

  
  
<span data-ttu-id="f7e24-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f7e24-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f7e24-105">添付ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="f7e24-105">Opens an attachment.</span></span> 
  
```cpp
HRESULT OpenAttach(
  ULONG ulAttachmentNum,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a><span data-ttu-id="f7e24-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7e24-106">Parameters</span></span>

 <span data-ttu-id="f7e24-107">_ulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="f7e24-107">_ulAttachmentNum_</span></span>
  
> <span data-ttu-id="f7e24-108">[in]開くには、添付ファイルの**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) のプロパティに格納されている添付ファイルのインデックス番号です。</span><span class="sxs-lookup"><span data-stu-id="f7e24-108">[in] Index number of the attachment to open, as stored in the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span> <span data-ttu-id="f7e24-109">このインデックス番号を一意に、メッセージの添付ファイルを識別し、メッセージのコンテキストでのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="f7e24-109">This index number uniquely identifies the attachment in the message and is valid only in the context of the message.</span></span>
    
 <span data-ttu-id="f7e24-110">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="f7e24-110">_lpInterface_</span></span>
  
> <span data-ttu-id="f7e24-111">[in]添付ファイルにアクセスするために使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f7e24-111">[in] Pointer to the interface identifier (IID) representing the interface to be used to access the attachment.</span></span> <span data-ttu-id="f7e24-112">パラメーターに NULL が返される添付ファイルの標準的なインタ フェース、または**IAttach**、発生します。</span><span class="sxs-lookup"><span data-stu-id="f7e24-112">Passing NULL results in the attachment's standard interface, or **IAttach**, being returned.</span></span> 
    
 <span data-ttu-id="f7e24-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f7e24-113">_ulFlags_</span></span>
  
> <span data-ttu-id="f7e24-114">[in]添付ファイルを開く方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="f7e24-114">[in] Bitmask of flags that controls how the attachment is opened.</span></span> <span data-ttu-id="f7e24-115">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="f7e24-115">The following flags can be set:</span></span> 
    
<span data-ttu-id="f7e24-116">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="f7e24-116">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="f7e24-117">ユーザーおよび最大のクライアント アプリケーションへのアクセスに使用される最大ネットワークのアクセス許可を持つ添付ファイルを開くことを要求します。</span><span class="sxs-lookup"><span data-stu-id="f7e24-117">Requests that the attachment be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="f7e24-118">たとえば、クライアントに読み取り/書き込み権限がある場合は、添付ファイル開く必要があります読み取り/書き込みアクセス許可を持つクライアントに読み取り専用アクセスがある場合は、読み取り専用アクセス権を持つ添付ファイルを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7e24-118">For example, if the client has read/write permission, the attachment should be opened with read/write permission; if the client has read-only access, the attachment should be opened with read-only access.</span></span> 
    
<span data-ttu-id="f7e24-119">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="f7e24-119">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="f7e24-120">正常に戻す、可能性のある添付ファイルは、呼び出し側のクライアントに完全に利用できる前に**OpenAttach**を使用できます。</span><span class="sxs-lookup"><span data-stu-id="f7e24-120">Allows **OpenAttach** to return successfully, possibly before the attachment is fully available to the calling client.</span></span> <span data-ttu-id="f7e24-121">添付ファイルが利用できない場合は、それ以降の呼び出しを行うとエラーが発生することができます。</span><span class="sxs-lookup"><span data-stu-id="f7e24-121">If the attachment is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="f7e24-122">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="f7e24-122">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="f7e24-123">要求の読み取り/書き込みのアクセス許可</span><span class="sxs-lookup"><span data-stu-id="f7e24-123">Requests read/write permission.</span></span> <span data-ttu-id="f7e24-124">既定では、添付ファイルは、読み取り専用アクセスで開くし、クライアントが読み取り/書き込みアクセス許可が付与されていることを前提に動作しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7e24-124">By default, attachments are opened with read-only access, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="f7e24-125">_lppAttach_</span><span class="sxs-lookup"><span data-stu-id="f7e24-125">_lppAttach_</span></span>
  
> <span data-ttu-id="f7e24-126">[out]開いている添付ファイルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="f7e24-126">[out] Pointer to a pointer to the open attachment.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f7e24-127">�߂�l</span><span class="sxs-lookup"><span data-stu-id="f7e24-127">Return value</span></span>

<span data-ttu-id="f7e24-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="f7e24-128">S_OK</span></span> 
  
> <span data-ttu-id="f7e24-129">添付ファイルが正常に開かれました。</span><span class="sxs-lookup"><span data-stu-id="f7e24-129">The attachment was successfully opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f7e24-130">注釈</span><span class="sxs-lookup"><span data-stu-id="f7e24-130">Remarks</span></span>

<span data-ttu-id="f7e24-131">**IMessage::OpenAttach**メソッドは、メッセージの添付ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="f7e24-131">The **IMessage::OpenAttach** method opens a message's attachment.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f7e24-132">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="f7e24-132">Notes to callers</span></span>

<span data-ttu-id="f7e24-133">添付ファイルを開くには、その添付ファイルの数や**PR_ATTACH_NUM**のプロパティへのアクセスが必要です。</span><span class="sxs-lookup"><span data-stu-id="f7e24-133">To open an attachment, you must have access to its attachment number or **PR_ATTACH_NUM** property.</span></span> <span data-ttu-id="f7e24-134">メッセージの添付ファイル テーブルを取得し、添付ファイルを開くことを表す行を探し、 [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f7e24-134">Call [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) to retrieve the message's attachment table and locate the row that represents the attachment to be opened.</span></span> <span data-ttu-id="f7e24-135">詳細については、[添付ファイルを開く](opening-an-attachment.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f7e24-135">See [Opening an Attachment](opening-an-attachment.md) for more information.</span></span> 
  
<span data-ttu-id="f7e24-136">複数回 1 つの添付ファイルを開くしないでください。結果は不定であり、メッセージ ストア プロバイダーに依存しているです。</span><span class="sxs-lookup"><span data-stu-id="f7e24-136">Do not try to open one attachment multiple times; the results are undefined and dependent on the message store provider.</span></span>
  
<span data-ttu-id="f7e24-137">添付ファイルは、既定の読み取り専用モードではなく、読み取り/書き込みモードで開くことを要求することができます。</span><span class="sxs-lookup"><span data-stu-id="f7e24-137">You can request that the attachment be opened in read/write mode, instead of the default read-only mode.</span></span> <span data-ttu-id="f7e24-138">ただし、添付ファイルは実際には、開かれているか読み取り/書き込みモードでは、メッセージ ストア プロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="f7e24-138">However, whether the attachment will actually be opened in read/write mode is up to the message store provider.</span></span> <span data-ttu-id="f7e24-139">できます、添付ファイルを変更しようとすると、可能性のある障害を処理または使用可能になる場合、添付ファイルの**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) のプロパティを取得することによって付与されたアクセスのレベルを確認する準備をしています。</span><span class="sxs-lookup"><span data-stu-id="f7e24-139">You can either attempt to modify the attachment, preparing to handle possible failure, or check the level of access that was granted by retrieving the attachment's **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property, if it is available.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f7e24-140">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="f7e24-140">MFCMAPI reference</span></span>

<span data-ttu-id="f7e24-141">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="f7e24-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f7e24-142">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="f7e24-142">**File**</span></span>|<span data-ttu-id="f7e24-143">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="f7e24-143">**Function**</span></span>|<span data-ttu-id="f7e24-144">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="f7e24-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f7e24-145">AttachmentsDlg.cpp をするために使用</span><span class="sxs-lookup"><span data-stu-id="f7e24-145">AttachmentsDlg.cpp Used to</span></span>  <br/> |<span data-ttu-id="f7e24-146">CAttachmentsDlg::OpenItemProp</span><span class="sxs-lookup"><span data-stu-id="f7e24-146">CAttachmentsDlg::OpenItemProp</span></span>  <br/> |<span data-ttu-id="f7e24-147">MFCMAPI を開くには、添付ファイルのオブジェクトの**IMessage::OpenAttach**メソッドを使用してください。</span><span class="sxs-lookup"><span data-stu-id="f7e24-147">MFCMAPI uses the **IMessage::OpenAttach** method to open attachment objects,</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f7e24-148">関連項目</span><span class="sxs-lookup"><span data-stu-id="f7e24-148">See also</span></span>



[<span data-ttu-id="f7e24-149">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f7e24-149">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


<span data-ttu-id="f7e24-150">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="f7e24-150">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

