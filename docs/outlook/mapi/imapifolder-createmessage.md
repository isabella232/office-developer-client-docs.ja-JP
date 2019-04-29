---
title: IMAPIFolderCreateMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CreateMessage
api_type:
- COM
ms.assetid: e0222afa-c148-4735-a603-cac7be6c91f9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4d38648f5e3084c8342fca8d18f0bd3efc915155
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412633"
---
# <a name="imapifoldercreatemessage"></a><span data-ttu-id="c8436-103">IMAPIFolder::CreateMessage</span><span class="sxs-lookup"><span data-stu-id="c8436-103">IMAPIFolder::CreateMessage</span></span>

  
  
<span data-ttu-id="c8436-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8436-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8436-105">新しいメッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="c8436-105">Creates a new message.</span></span>
  
```cpp
HRESULT CreateMessage(
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMessage
);
```

## <a name="parameters"></a><span data-ttu-id="c8436-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c8436-106">Parameters</span></span>

 <span data-ttu-id="c8436-107">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="c8436-107">_lpInterface_</span></span>
  
> <span data-ttu-id="c8436-108">順番新しいメッセージへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c8436-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the new message.</span></span> <span data-ttu-id="c8436-109">有効なインターフェイス識別子には、IID_IUnknown、IID_IMAPIProp、IID_IMAPIContainer、および IID_IMAPIFolder があります。</span><span class="sxs-lookup"><span data-stu-id="c8436-109">Valid interface identifiers include IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, and IID_IMAPIFolder.</span></span> <span data-ttu-id="c8436-110">NULL を渡すと、メッセージストアプロバイダーは標準のメッセージインターフェイス[IMessage: imapiprop](imessageimapiprop.md)を返します。</span><span class="sxs-lookup"><span data-stu-id="c8436-110">Passing NULL causes the message store provider to return the standard message interface, [IMessage : IMAPIProp](imessageimapiprop.md).</span></span> 
    
 <span data-ttu-id="c8436-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c8436-111">_ulFlags_</span></span>
  
> <span data-ttu-id="c8436-112">順番メッセージの作成方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="c8436-112">[in] A bitmask of flags that controls how the message is created.</span></span> <span data-ttu-id="c8436-113">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="c8436-113">The following flags can be set:</span></span>
    
<span data-ttu-id="c8436-114">ITEMPROC_FORCE</span><span class="sxs-lookup"><span data-stu-id="c8436-114">ITEMPROC_FORCE</span></span>
  
> <span data-ttu-id="c8436-115">ストアが新しいメッセージの到着をリッスンしているクライアントに通知する前に、そのメッセージがルール処理の対象となっていることを個人用フォルダーストア (PST) に示します。</span><span class="sxs-lookup"><span data-stu-id="c8436-115">Indicates to the personal folder store (PST) that the message is eligible for rules processing before the store notifies any listening client of the arrival of the new message.</span></span> <span data-ttu-id="c8436-116">ルール処理は、Microsoft exchange server 以外のサーバー上に作成された新しいメッセージにのみ適用されます。 exchange server は、サーバー上のメッセージのルールを処理するからです。</span><span class="sxs-lookup"><span data-stu-id="c8436-116">Rules processing only applies to new messages that are created on a server that is not a Microsoft Exchange Server, because Exchange Server processes rules for messages on the server.</span></span> <span data-ttu-id="c8436-117">そのため、メッセージを作成するプロバイダーまたはクライアントは、 [IMAPIPProp:: SaveChanges](imapiprop-savechanges.md)を使用して、サーバーが Exchange サーバーではないことを示す NON_EMS_XP_SAVE を使用してメッセージを保存することにより、このフラグを渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8436-117">Therefore, the provider or client creating the message must pass this flag in combination with saving a message with [IMAPIPProp::SaveChanges](imapiprop-savechanges.md) using NON_EMS_XP_SAVE, which indicates that the server is not an Exchange Server.</span></span> 
    
<span data-ttu-id="c8436-118">MAPI_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="c8436-118">MAPI_ASSOCIATED</span></span> 
  
> <span data-ttu-id="c8436-119">作成されるメッセージは、標準の contents テーブルではなく、関連付けられた contents テーブルに含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8436-119">The message to be created should be included in the associated contents table instead of the standard contents table.</span></span> <span data-ttu-id="c8436-120">関連付けられたメッセージは、ユーザーの操作から非表示になります。</span><span class="sxs-lookup"><span data-stu-id="c8436-120">Associated messages are hidden from user interaction.</span></span>
    
<span data-ttu-id="c8436-121">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="c8436-121">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="c8436-122">**CreateMessage**は、作成操作が完全に完了していない場合でも、成功することができます。</span><span class="sxs-lookup"><span data-stu-id="c8436-122">**CreateMessage** is allowed to succeed even if the create operation has not fully completed.</span></span> <span data-ttu-id="c8436-123">これは、新しいメッセージがすぐに発信者に対して使用できなくなる可能性があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="c8436-123">This implies that the new message might not be immediately available to the caller.</span></span> 
    
 <span data-ttu-id="c8436-124">_lppmessage_</span><span class="sxs-lookup"><span data-stu-id="c8436-124">_lppMessage_</span></span>
  
> <span data-ttu-id="c8436-125">読み上げ新しく作成されたメッセージへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c8436-125">[out] A pointer to a pointer to the newly created message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c8436-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="c8436-126">Return value</span></span>

<span data-ttu-id="c8436-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="c8436-127">S_OK</span></span> 
  
> <span data-ttu-id="c8436-128">メッセージが正常に作成されました。</span><span class="sxs-lookup"><span data-stu-id="c8436-128">The message was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c8436-129">注釈</span><span class="sxs-lookup"><span data-stu-id="c8436-129">Remarks</span></span>

<span data-ttu-id="c8436-130">**imapifolder:: CreateMessage**メソッドは、標準または関連付けられたコンテンツを含む新しいメッセージを作成し、エントリ識別子を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="c8436-130">The **IMAPIFolder::CreateMessage** method creates a new message with generic or associated content and assigns an entry identifier.</span></span> <span data-ttu-id="c8436-131">エントリ識別子は、メッセージストアプロバイダーと個別のメッセージを表すパーツから構成されます。</span><span class="sxs-lookup"><span data-stu-id="c8436-131">The entry identifier consists of a part that represents the message store provider and a part that represents the individual message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c8436-132">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="c8436-132">Notes to implementers</span></span>

<span data-ttu-id="c8436-133">**CreateMessage**ですべての必要なメッセージプロパティを設定するか、またはメッセージの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドで設定するかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="c8436-133">You can choose whether to set all of the required message properties in **CreateMessage** or in the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="c8436-134">正常な保存が行われるまで、これらのプロパティを使用できないようにする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c8436-134">You do not have to make these properties available until a successful save has occurred.</span></span> 
  
<span data-ttu-id="c8436-135">関連情報の操作方法の詳細については、「[フォルダーに関連付けられた情報の表](folder-associated-information-tables.md)と内容」の[表](contents-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8436-135">For more information about how to work with associated information, see [Folder-Associated Information Tables](folder-associated-information-tables.md) and [Contents Tables](contents-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c8436-136">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="c8436-136">Notes to callers</span></span>

<span data-ttu-id="c8436-137">一部のメッセージストアプロバイダーでは、 **CreateMessage**が戻ると、すぐに新しいメッセージのエントリ識別子を使用できるようにすることができます。その他のメッセージストアプロバイダーは、メッセージが保存されるまで、可用性を遅らせます。</span><span class="sxs-lookup"><span data-stu-id="c8436-137">Some message store providers allow the entry identifier of the new message to be available immediately after **CreateMessage** returns; other message store providers delay its availability until the message is saved.</span></span> <span data-ttu-id="c8436-138">メッセージの**imapiprop:: SaveChanges**メソッドを呼び出しない限り、すべてのメッセージストアプロバイダーが新しいメッセージのエントリ識別子を生成しないため、 **CreateMessage**が戻るときに、エントリ id にアクセスできない場合があります。</span><span class="sxs-lookup"><span data-stu-id="c8436-138">Because not all message store providers generate an entry identifier for a new message until you have called the message's **IMAPIProp::SaveChanges** method, you may be unable to access the entry identifier when **CreateMessage** returns.</span></span> <span data-ttu-id="c8436-139">また、新しいメッセージは、保存が行われるまでフォルダーの contents テーブルに含まれない場合があります。</span><span class="sxs-lookup"><span data-stu-id="c8436-139">Also, the new message may not be included in the folder's contents table until the save occurs.</span></span> 
  
<span data-ttu-id="c8436-140">新しいメッセージに割り当てられたエントリ識別子は、現在のメッセージストアだけでなく、同時に開いているすべてのメッセージストアにわたって一意であると想定します。</span><span class="sxs-lookup"><span data-stu-id="c8436-140">Expect the entry identifier assigned to the new message to be unique not only in the current message store, but most likely across all of the message stores that are open at the same time.</span></span> <span data-ttu-id="c8436-141">このルールの1つの例外は、メッセージストアの複数のエントリがプロファイルに表示される場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="c8436-141">One exception to this rule occurs when multiple entries for a message store appear in the profile.</span></span> <span data-ttu-id="c8436-142">これにより、メッセージストアが複数回開かれ、エントリ識別子が複製されます。</span><span class="sxs-lookup"><span data-stu-id="c8436-142">This causes the message store to be opened multiple times and entry identifiers to be duplicated.</span></span> 
  
<span data-ttu-id="c8436-143">送信メッセージを作成するには、送信トレイフォルダーの**imapifolder:: CreateMessage**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c8436-143">To create an outgoing message, call the Outbox folder's **IMAPIFolder::CreateMessage** method.</span></span> 
  
<span data-ttu-id="c8436-144">メッセージが保存される前に新しいメッセージを含むフォルダーを削除すると、結果は未定義となります。</span><span class="sxs-lookup"><span data-stu-id="c8436-144">If you delete a folder that contains a new message before the message is saved, the results are undefined.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c8436-145">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="c8436-145">MFCMAPI reference</span></span>

<span data-ttu-id="c8436-146">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8436-146">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c8436-147">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="c8436-147">**File**</span></span>|<span data-ttu-id="c8436-148">**関数**</span><span class="sxs-lookup"><span data-stu-id="c8436-148">**Function**</span></span>|<span data-ttu-id="c8436-149">**コメント**</span><span class="sxs-lookup"><span data-stu-id="c8436-149">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c8436-150">folderdlg</span><span class="sxs-lookup"><span data-stu-id="c8436-150">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="c8436-151">cfolder:: onnewmessage</span><span class="sxs-lookup"><span data-stu-id="c8436-151">CFolder::OnNewMessage</span></span>  <br/> |<span data-ttu-id="c8436-152">mfcmapi は、 **imapifolder:: CreateMessage**メソッドを使用して、新しいメッセージを作成して保存します。</span><span class="sxs-lookup"><span data-stu-id="c8436-152">MFCMAPI uses the **IMAPIFolder::CreateMessage** method to create and save a new message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c8436-153">関連項目</span><span class="sxs-lookup"><span data-stu-id="c8436-153">See also</span></span>



[<span data-ttu-id="c8436-154">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="c8436-154">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="c8436-155">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="c8436-155">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


<span data-ttu-id="c8436-156">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="c8436-156">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

