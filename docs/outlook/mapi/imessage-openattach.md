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
# <a name="imessageopenattach"></a><span data-ttu-id="ab89c-103">IMessage::OpenAttach</span><span class="sxs-lookup"><span data-stu-id="ab89c-103">IMessage::OpenAttach</span></span>

  
  
<span data-ttu-id="ab89c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab89c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab89c-105">添付ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="ab89c-105">Opens an attachment.</span></span> 
  
```cpp
HRESULT OpenAttach(
  ULONG ulAttachmentNum,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a><span data-ttu-id="ab89c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ab89c-106">Parameters</span></span>

 <span data-ttu-id="ab89c-107">_ulattachmentnum_</span><span class="sxs-lookup"><span data-stu-id="ab89c-107">_ulAttachmentNum_</span></span>
  
> <span data-ttu-id="ab89c-108">順番添付ファイルの**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティに格納されている、開く添付ファイルのインデックス番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="ab89c-108">[in] Index number of the attachment to open, as stored in the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span> <span data-ttu-id="ab89c-109">このインデックス番号は、メッセージの添付ファイルを一意に識別するもので、メッセージのコンテキストでのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="ab89c-109">This index number uniquely identifies the attachment in the message and is valid only in the context of the message.</span></span>
    
 <span data-ttu-id="ab89c-110">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="ab89c-110">_lpInterface_</span></span>
  
> <span data-ttu-id="ab89c-111">順番添付ファイルへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ab89c-111">[in] Pointer to the interface identifier (IID) representing the interface to be used to access the attachment.</span></span> <span data-ttu-id="ab89c-112">NULL 結果を添付ファイルの標準インターフェイスまたは**iattach**に渡すと、返されます。</span><span class="sxs-lookup"><span data-stu-id="ab89c-112">Passing NULL results in the attachment's standard interface, or **IAttach**, being returned.</span></span> 
    
 <span data-ttu-id="ab89c-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ab89c-113">_ulFlags_</span></span>
  
> <span data-ttu-id="ab89c-114">順番添付ファイルを開く方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="ab89c-114">[in] Bitmask of flags that controls how the attachment is opened.</span></span> <span data-ttu-id="ab89c-115">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="ab89c-115">The following flags can be set:</span></span> 
    
<span data-ttu-id="ab89c-116">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="ab89c-116">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="ab89c-117">ユーザーに対して許可される最大のネットワークアクセス許可と、クライアントアプリケーションの最大アクセス権を使用して、添付ファイルを開くように要求します。</span><span class="sxs-lookup"><span data-stu-id="ab89c-117">Requests that the attachment be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="ab89c-118">たとえば、クライアントに読み取り/書き込みアクセス許可がある場合、添付ファイルは読み取り/書き込みアクセス許可を使用して開く必要があります。クライアントが読み取り専用のアクセス権を持っている場合は、添付ファイルを読み取り専用アクセスで開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab89c-118">For example, if the client has read/write permission, the attachment should be opened with read/write permission; if the client has read-only access, the attachment should be opened with read-only access.</span></span> 
    
<span data-ttu-id="ab89c-119">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="ab89c-119">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="ab89c-120">添付ファイルが呼び出し元クライアントに完全に使用可能になる前に、 **openattach**を正常に返すことができるようにします。</span><span class="sxs-lookup"><span data-stu-id="ab89c-120">Allows **OpenAttach** to return successfully, possibly before the attachment is fully available to the calling client.</span></span> <span data-ttu-id="ab89c-121">添付ファイルを使用できない場合は、その後の呼び出しを行うとエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ab89c-121">If the attachment is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="ab89c-122">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="ab89c-122">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="ab89c-123">読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="ab89c-123">Requests read/write permission.</span></span> <span data-ttu-id="ab89c-124">既定では、添付ファイルは読み取り専用アクセスで開かれ、読み取り/書き込みアクセス許可が付与されているという前提でクライアントを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="ab89c-124">By default, attachments are opened with read-only access, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="ab89c-125">_lppattach_</span><span class="sxs-lookup"><span data-stu-id="ab89c-125">_lppAttach_</span></span>
  
> <span data-ttu-id="ab89c-126">読み上げ開かれた添付ファイルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ab89c-126">[out] Pointer to a pointer to the open attachment.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ab89c-127">戻り値</span><span class="sxs-lookup"><span data-stu-id="ab89c-127">Return value</span></span>

<span data-ttu-id="ab89c-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="ab89c-128">S_OK</span></span> 
  
> <span data-ttu-id="ab89c-129">添付ファイルが正常に開かれました。</span><span class="sxs-lookup"><span data-stu-id="ab89c-129">The attachment was successfully opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ab89c-130">注釈</span><span class="sxs-lookup"><span data-stu-id="ab89c-130">Remarks</span></span>

<span data-ttu-id="ab89c-131">**IMessage:: openattach**メソッドは、メッセージの添付ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="ab89c-131">The **IMessage::OpenAttach** method opens a message's attachment.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ab89c-132">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="ab89c-132">Notes to callers</span></span>

<span data-ttu-id="ab89c-133">添付ファイルを開くには、添付ファイルの番号または**PR_ATTACH_NUM**プロパティにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab89c-133">To open an attachment, you must have access to its attachment number or **PR_ATTACH_NUM** property.</span></span> <span data-ttu-id="ab89c-134">[IMessage:: getattachmenttable](imessage-getattachmenttable.md)を呼び出して、メッセージの添付ファイルテーブルを取得し、開く添付ファイルを表す行を見つけます。</span><span class="sxs-lookup"><span data-stu-id="ab89c-134">Call [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) to retrieve the message's attachment table and locate the row that represents the attachment to be opened.</span></span> <span data-ttu-id="ab89c-135">詳細について[は、「添付ファイルを開く](opening-an-attachment.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab89c-135">See [Opening an Attachment](opening-an-attachment.md) for more information.</span></span> 
  
<span data-ttu-id="ab89c-136">1つの添付ファイルを複数回開いてはいけません。結果は未定義で、メッセージストアプロバイダーに依存します。</span><span class="sxs-lookup"><span data-stu-id="ab89c-136">Do not try to open one attachment multiple times; the results are undefined and dependent on the message store provider.</span></span>
  
<span data-ttu-id="ab89c-137">既定の読み取り専用モードではなく、読み取り/書き込みモードで添付ファイルを開くように要求することができます。</span><span class="sxs-lookup"><span data-stu-id="ab89c-137">You can request that the attachment be opened in read/write mode, instead of the default read-only mode.</span></span> <span data-ttu-id="ab89c-138">ただし、添付ファイルが実際に読み取り/書き込みモードで開かれるかどうかは、メッセージストアプロバイダーによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="ab89c-138">However, whether the attachment will actually be opened in read/write mode is up to the message store provider.</span></span> <span data-ttu-id="ab89c-139">添付ファイルを変更するか、起こり得るエラーを処理するための準備を試みるか、添付ファイルの**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) プロパティを取得することによって付与されたアクセスのレベルを確認することができます (使用可能な場合)。</span><span class="sxs-lookup"><span data-stu-id="ab89c-139">You can either attempt to modify the attachment, preparing to handle possible failure, or check the level of access that was granted by retrieving the attachment's **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property, if it is available.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ab89c-140">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="ab89c-140">MFCMAPI reference</span></span>

<span data-ttu-id="ab89c-141">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab89c-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ab89c-142">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="ab89c-142">**File**</span></span>|<span data-ttu-id="ab89c-143">**関数**</span><span class="sxs-lookup"><span data-stu-id="ab89c-143">**Function**</span></span>|<span data-ttu-id="ab89c-144">**コメント**</span><span class="sxs-lookup"><span data-stu-id="ab89c-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ab89c-145">AttachmentsDlg に使用する</span><span class="sxs-lookup"><span data-stu-id="ab89c-145">AttachmentsDlg.cpp Used to</span></span>  <br/> |<span data-ttu-id="ab89c-146">CAttachmentsDlg:: openitemprop</span><span class="sxs-lookup"><span data-stu-id="ab89c-146">CAttachmentsDlg::OpenItemProp</span></span>  <br/> |<span data-ttu-id="ab89c-147">mfcmapi は、 **IMessage:: openattach**メソッドを使用して添付ファイルオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="ab89c-147">MFCMAPI uses the **IMessage::OpenAttach** method to open attachment objects,</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ab89c-148">関連項目</span><span class="sxs-lookup"><span data-stu-id="ab89c-148">See also</span></span>



[<span data-ttu-id="ab89c-149">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ab89c-149">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


<span data-ttu-id="ab89c-150">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="ab89c-150">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

