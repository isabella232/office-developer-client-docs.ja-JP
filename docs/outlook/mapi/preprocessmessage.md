---
title: PreprocessMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PreprocessMessage
api_type:
- COM
ms.assetid: dda50325-74b3-445e-986e-115f6536561f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a3982520cb1c745874a938962ece075a294b6257
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437246"
---
# <a name="preprocessmessage"></a><span data-ttu-id="c3e51-103">PreprocessMessage</span><span class="sxs-lookup"><span data-stu-id="c3e51-103">PreprocessMessage</span></span>

  
  
<span data-ttu-id="c3e51-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3e51-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3e51-105">メッセージの内容またはメッセージの形式を前にする関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="c3e51-105">Defines a function that preprocesses message contents or the format of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c3e51-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="c3e51-106">Header file:</span></span>  <br/> |<span data-ttu-id="c3e51-107">Mapispi</span><span class="sxs-lookup"><span data-stu-id="c3e51-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="c3e51-108">定義された関数の実装:</span><span class="sxs-lookup"><span data-stu-id="c3e51-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="c3e51-109">トランスポートプロバイダー</span><span class="sxs-lookup"><span data-stu-id="c3e51-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="c3e51-110">によって呼び出された定義済み関数:</span><span class="sxs-lookup"><span data-stu-id="c3e51-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="c3e51-111">MAPI スプーラー</span><span class="sxs-lookup"><span data-stu-id="c3e51-111">MAPI spooler</span></span>  <br/> |
   
```cpp
HRESULT PreprocessMessage(
  LPVOID lpvSession,
  LPMESSAGE lpMessage,
  LPADRBOOK lpAdrBook,
  LPMAPIFOLDER lpFolder,
  LPALLOCATEBUFFER AllocateBuffer,
  LPALLOCATEMORE AllocateMore,
  LPFREEBUFFER FreeBuffer,
  ULONG FAR * lpcOutbound,
  LPMESSAGE FAR * FAR * lpppMessage,
  LPADRLIST FAR * lppRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="c3e51-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c3e51-112">Parameters</span></span>

 <span data-ttu-id="c3e51-113">_lpvsession_</span><span class="sxs-lookup"><span data-stu-id="c3e51-113">_lpvSession_</span></span>
  
> <span data-ttu-id="c3e51-114">順番使用するセッションへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c3e51-114">[in] Pointer to the session to be used.</span></span> 
    
 <span data-ttu-id="c3e51-115">_lpmessage_</span><span class="sxs-lookup"><span data-stu-id="c3e51-115">_lpMessage_</span></span>
  
> <span data-ttu-id="c3e51-116">順番前処理するメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c3e51-116">[in] Pointer to the message to be preprocessed.</span></span> 
    
 <span data-ttu-id="c3e51-117">_lpadrbook_</span><span class="sxs-lookup"><span data-stu-id="c3e51-117">_lpAdrBook_</span></span>
  
> <span data-ttu-id="c3e51-118">順番ユーザーがメッセージの受信者を選択する必要があるアドレス帳へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c3e51-118">[in] Pointer to the address book from which the user should select recipients for the message.</span></span> 
    
 <span data-ttu-id="c3e51-119">_lpfolder_</span><span class="sxs-lookup"><span data-stu-id="c3e51-119">_lpFolder_</span></span>
  
> <span data-ttu-id="c3e51-120">[入力]フォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c3e51-120">[in, out] Pointer to a folder.</span></span> <span data-ttu-id="c3e51-121">入力時に_lpfolder_パラメーターは、前処理するメッセージを含むフォルダーを指します。</span><span class="sxs-lookup"><span data-stu-id="c3e51-121">On input, the  _lpFolder_ parameter points to the folder that contains messages to be preprocessed.</span></span> <span data-ttu-id="c3e51-122">出力時に、 _lpfolder_はプリプロセスされたメッセージが配置されたフォルダーを指します。</span><span class="sxs-lookup"><span data-stu-id="c3e51-122">On output,  _lpFolder_ points to the folder where preprocessed messages have been placed.</span></span> 
    
 <span data-ttu-id="c3e51-123">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="c3e51-123">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="c3e51-124">順番メモリの割り当てに使用される[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c3e51-124">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="c3e51-125">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="c3e51-125">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="c3e51-126">順番必要なときに追加のメモリを割り当てるために使用される[MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c3e51-126">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory where required.</span></span> 
    
 <span data-ttu-id="c3e51-127">_lpfreebuffer_</span><span class="sxs-lookup"><span data-stu-id="c3e51-127">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="c3e51-128">順番メモリを解放するために使用される[MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c3e51-128">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="c3e51-129">_lpcOutbound_</span><span class="sxs-lookup"><span data-stu-id="c3e51-129">_lpcOutbound_</span></span>
  
> <span data-ttu-id="c3e51-130">読み上げ_lpppMessage_パラメーターによって指定された配列内のメッセージ数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c3e51-130">[out] Pointer to the number of messages in the array pointed to by the  _lpppMessage_ parameter.</span></span> 
    
 <span data-ttu-id="c3e51-131">_lpppMessage_</span><span class="sxs-lookup"><span data-stu-id="c3e51-131">_lpppMessage_</span></span>
  
> <span data-ttu-id="c3e51-132">読み上げプリプロセスされた、または生成されたメッセージへのポインターの配列へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c3e51-132">[out] Pointer to a pointer to an array of pointers to preprocessed or otherwise generated messages.</span></span> 
    
 <span data-ttu-id="c3e51-133">_lppRecipList_</span><span class="sxs-lookup"><span data-stu-id="c3e51-133">_lppRecipList_</span></span>
  
> <span data-ttu-id="c3e51-134">読み上げメッセージが配信できない、プリプロセッサが検出された受信者を一覧表示する、オプションで返される[adrlist](adrlist.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c3e51-134">[out] Pointer to an optional returned [ADRLIST](adrlist.md) structure, listing preprocessor-detected recipients for which the message is undeliverable.</span></span> <span data-ttu-id="c3e51-135">このリストの内容の詳細については、 [imapisupport:: StatusRecips](imapisupport-statusrecips.md)メソッドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c3e51-135">For more information about the contents of this list, see the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c3e51-136">戻り値</span><span class="sxs-lookup"><span data-stu-id="c3e51-136">Return value</span></span>

<span data-ttu-id="c3e51-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="c3e51-137">S_OK</span></span>
  
> <span data-ttu-id="c3e51-138">メッセージの内容が正常に前処理されました。</span><span class="sxs-lookup"><span data-stu-id="c3e51-138">Message contents were successfully preprocessed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c3e51-139">注釈</span><span class="sxs-lookup"><span data-stu-id="c3e51-139">Remarks</span></span>

<span data-ttu-id="c3e51-140">トランスポートプロバイダメッセージプリプロセッサは、メッセージの前処理中に進行状況インジケーターを表示できます。</span><span class="sxs-lookup"><span data-stu-id="c3e51-140">A transport-provider message preprocessor can present a progress indicator during message preprocessing.</span></span> <span data-ttu-id="c3e51-141">ただし、メッセージ前処理中のユーザー操作を必要とするダイアログボックスを表示する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c3e51-141">However, it should never present a dialog box requiring user interaction during message preprocessing.</span></span> 
  
<span data-ttu-id="c3e51-142">プリプロセッサが送信メッセージに大量のデータを追加するときは、特定の手順に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3e51-142">When a preprocessor adds large amounts of data to an outbound message, certain procedures should be followed.</span></span> <span data-ttu-id="c3e51-143">この種のメッセージをサーバーベースのメッセージストアに格納することにより、プリプロセッサがリモートストアにアクセスします。時間がかかるプロシージャです。</span><span class="sxs-lookup"><span data-stu-id="c3e51-143">This type of message can be stored in a server-based message store, causing the preprocessor to access a remote store, a time-consuming procedure.</span></span> <span data-ttu-id="c3e51-144">これを回避するために、プリプロセッサには、ローカルメッセージストアで大量の領域を必要とするデータを格納し、メッセージにそのローカルストアへの参照を提供できるオプションが用意されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3e51-144">To avoid having to do so, the preprocessor should have an option that enables it to store data that takes a large amount of space in a local message store and to provide a reference to that local store in the message.</span></span> 
  
<span data-ttu-id="c3e51-145">プリプロセッサは、元の**PreprocessMessage**ベースの関数に渡されたオブジェクトを解放してはなりません。</span><span class="sxs-lookup"><span data-stu-id="c3e51-145">The preprocessor should not release any of the objects originally passed to the **PreprocessMessage** based function.</span></span> 
  
<span data-ttu-id="c3e51-146">MAPI スプーラーで**PreprocessMessage**関数を呼び出せるようにするには、トランスポートプロバイダーが[imapisupport:: registerpreprocessor プロセッサ](imapisupport-registerpreprocessor.md)メソッドへの呼び出しに関数を登録している必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3e51-146">Before the MAPI spooler can call a **PreprocessMessage** function, the transport provider must have registered the function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> <span data-ttu-id="c3e51-147">**PreprocessMessage**関数を呼び出した後、スプーラーは、関数が戻るまで、メッセージの送信を続行できません。</span><span class="sxs-lookup"><span data-stu-id="c3e51-147">After calling a **PreprocessMessage** function, the spooler cannot continue submitting a message until the function returns.</span></span> 
  
<span data-ttu-id="c3e51-148">MAPI スプーラーは、メッセージを送信するタスクを所有しています。</span><span class="sxs-lookup"><span data-stu-id="c3e51-148">The MAPI spooler owns the task of submitting messages.</span></span> <span data-ttu-id="c3e51-149">これは、元のメッセージがメッセージポインターの配列に配置されることはないため、 **submitmessage**メソッドへの呼び出しが必要になることはありません。</span><span class="sxs-lookup"><span data-stu-id="c3e51-149">This means the original message is never placed in an array of message pointers and that a call to the **SubmitMessage** methods is never required.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c3e51-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="c3e51-150">See also</span></span>



[<span data-ttu-id="c3e51-151">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c3e51-151">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="c3e51-152">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="c3e51-152">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="c3e51-153">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c3e51-153">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

