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
# <a name="preprocessmessage"></a><span data-ttu-id="78591-103">PreprocessMessage</span><span class="sxs-lookup"><span data-stu-id="78591-103">PreprocessMessage</span></span>

  
  
<span data-ttu-id="78591-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78591-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78591-105">メッセージの内容またはメッセージの形式を前処理する関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="78591-105">Defines a function that preprocesses message contents or the format of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="78591-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="78591-106">Header file:</span></span>  <br/> |<span data-ttu-id="78591-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="78591-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="78591-108">定義された関数は、次の方法で実装されます。</span><span class="sxs-lookup"><span data-stu-id="78591-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="78591-109">トランスポート プロバイダー</span><span class="sxs-lookup"><span data-stu-id="78591-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="78591-110">によって呼び出される定義済み関数:</span><span class="sxs-lookup"><span data-stu-id="78591-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="78591-111">MAPI スプーラー</span><span class="sxs-lookup"><span data-stu-id="78591-111">MAPI spooler</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="78591-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="78591-112">Parameters</span></span>

 <span data-ttu-id="78591-113">_lpvSession_</span><span class="sxs-lookup"><span data-stu-id="78591-113">_lpvSession_</span></span>
  
> <span data-ttu-id="78591-114">[in]使用するセッションへのポインター。</span><span class="sxs-lookup"><span data-stu-id="78591-114">[in] Pointer to the session to be used.</span></span> 
    
 <span data-ttu-id="78591-115">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="78591-115">_lpMessage_</span></span>
  
> <span data-ttu-id="78591-116">[in]前処理するメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="78591-116">[in] Pointer to the message to be preprocessed.</span></span> 
    
 <span data-ttu-id="78591-117">_lpAdrBook_</span><span class="sxs-lookup"><span data-stu-id="78591-117">_lpAdrBook_</span></span>
  
> <span data-ttu-id="78591-118">[in]ユーザーがメッセージの受信者を選択するアドレス帳へのポインター。</span><span class="sxs-lookup"><span data-stu-id="78591-118">[in] Pointer to the address book from which the user should select recipients for the message.</span></span> 
    
 <span data-ttu-id="78591-119">_lpFolder_</span><span class="sxs-lookup"><span data-stu-id="78591-119">_lpFolder_</span></span>
  
> <span data-ttu-id="78591-120">[in, out]フォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="78591-120">[in, out] Pointer to a folder.</span></span> <span data-ttu-id="78591-121">入力時に  _、lpFolder_ パラメーターは、前処理するメッセージを含むフォルダーをポイントします。</span><span class="sxs-lookup"><span data-stu-id="78591-121">On input, the  _lpFolder_ parameter points to the folder that contains messages to be preprocessed.</span></span> <span data-ttu-id="78591-122">出力時に  _、lpFolder は_ 、前処理されたメッセージが配置されたフォルダーをポイントします。</span><span class="sxs-lookup"><span data-stu-id="78591-122">On output,  _lpFolder_ points to the folder where preprocessed messages have been placed.</span></span> 
    
 <span data-ttu-id="78591-123">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="78591-123">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="78591-124">[in]メモリの割 [り当てに使用する MAPIAllocateBuffer](mapiallocatebuffer.md) 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="78591-124">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="78591-125">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="78591-125">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="78591-126">[in]必要に応じて追加のメモリを割り当てるのに使用する [MAPIAllocateMore](mapiallocatemore.md) 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="78591-126">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory where required.</span></span> 
    
 <span data-ttu-id="78591-127">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="78591-127">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="78591-128">[in]メモリを解放するために使用する [MAPIFreeBuffer](mapifreebuffer.md) 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="78591-128">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="78591-129">_lpcOutbound_</span><span class="sxs-lookup"><span data-stu-id="78591-129">_lpcOutbound_</span></span>
  
> <span data-ttu-id="78591-130">[out]  _lpppMessage_ パラメーターが指す配列内のメッセージ数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="78591-130">[out] Pointer to the number of messages in the array pointed to by the  _lpppMessage_ parameter.</span></span> 
    
 <span data-ttu-id="78591-131">_lpppMessage_</span><span class="sxs-lookup"><span data-stu-id="78591-131">_lpppMessage_</span></span>
  
> <span data-ttu-id="78591-132">[out]プリプロセスまたはそれ以外の方法で生成されたメッセージへのポインターの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="78591-132">[out] Pointer to a pointer to an array of pointers to preprocessed or otherwise generated messages.</span></span> 
    
 <span data-ttu-id="78591-133">_lppRecipList_</span><span class="sxs-lookup"><span data-stu-id="78591-133">_lppRecipList_</span></span>
  
> <span data-ttu-id="78591-134">[out]メッセージが配信不能であるプリプロセッサが検出した受信者を一覧する、オプションで返される [ADRLIST](adrlist.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="78591-134">[out] Pointer to an optional returned [ADRLIST](adrlist.md) structure, listing preprocessor-detected recipients for which the message is undeliverable.</span></span> <span data-ttu-id="78591-135">このリストの内容の詳細については [、「IMAPISupport::StatusRecips メソッド」を参照](imapisupport-statusrecips.md) してください。</span><span class="sxs-lookup"><span data-stu-id="78591-135">For more information about the contents of this list, see the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="78591-136">戻り値</span><span class="sxs-lookup"><span data-stu-id="78591-136">Return value</span></span>

<span data-ttu-id="78591-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="78591-137">S_OK</span></span>
  
> <span data-ttu-id="78591-138">メッセージの内容が正常に前処理されました。</span><span class="sxs-lookup"><span data-stu-id="78591-138">Message contents were successfully preprocessed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="78591-139">注釈</span><span class="sxs-lookup"><span data-stu-id="78591-139">Remarks</span></span>

<span data-ttu-id="78591-140">トランスポート プロバイダー のメッセージ プリプロセッサは、メッセージの前処理中に進行状況インジケーターを表示できます。</span><span class="sxs-lookup"><span data-stu-id="78591-140">A transport-provider message preprocessor can present a progress indicator during message preprocessing.</span></span> <span data-ttu-id="78591-141">ただし、メッセージの前処理中にユーザー操作を必要とするダイアログ ボックスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="78591-141">However, it should never present a dialog box requiring user interaction during message preprocessing.</span></span> 
  
<span data-ttu-id="78591-142">プリプロセッサが大量のデータを送信メッセージに追加する場合は、特定の手順に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="78591-142">When a preprocessor adds large amounts of data to an outbound message, certain procedures should be followed.</span></span> <span data-ttu-id="78591-143">この種類のメッセージはサーバー ベースのメッセージ ストアに格納できます。これにより、プリプロセッサはリモート ストアにアクセスします。時間のかかる手順です。</span><span class="sxs-lookup"><span data-stu-id="78591-143">This type of message can be stored in a server-based message store, causing the preprocessor to access a remote store, a time-consuming procedure.</span></span> <span data-ttu-id="78591-144">これを避けるために、プリプロセッサには、ローカル メッセージ ストアに大量の領域を取るデータを格納し、メッセージ内のローカル ストアへの参照を提供できるオプションが必要です。</span><span class="sxs-lookup"><span data-stu-id="78591-144">To avoid having to do so, the preprocessor should have an option that enables it to store data that takes a large amount of space in a local message store and to provide a reference to that local store in the message.</span></span> 
  
<span data-ttu-id="78591-145">プリプロセッサは **、PreprocessMessage** ベースの関数に最初に渡されたオブジェクトを解放しません。</span><span class="sxs-lookup"><span data-stu-id="78591-145">The preprocessor should not release any of the objects originally passed to the **PreprocessMessage** based function.</span></span> 
  
<span data-ttu-id="78591-146">MAPI スプーラーが **PreprocessMessage** 関数を呼び出す前に、トランスポート プロバイダーは [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) メソッドの呼び出しで関数を登録している必要があります。</span><span class="sxs-lookup"><span data-stu-id="78591-146">Before the MAPI spooler can call a **PreprocessMessage** function, the transport provider must have registered the function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> <span data-ttu-id="78591-147">**PreprocessMessage 関数を呼び出** した後、スプーラーは、関数が返されるまでメッセージの送信を続行できません。</span><span class="sxs-lookup"><span data-stu-id="78591-147">After calling a **PreprocessMessage** function, the spooler cannot continue submitting a message until the function returns.</span></span> 
  
<span data-ttu-id="78591-148">MAPI スプーラーは、メッセージを送信するタスクを所有します。</span><span class="sxs-lookup"><span data-stu-id="78591-148">The MAPI spooler owns the task of submitting messages.</span></span> <span data-ttu-id="78591-149">つまり、元のメッセージはメッセージ ポインターの配列に配置されません **。SubmitMessage** メソッドの呼び出しは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="78591-149">This means the original message is never placed in an array of message pointers and that a call to the **SubmitMessage** methods is never required.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="78591-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="78591-150">See also</span></span>



[<span data-ttu-id="78591-151">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="78591-151">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="78591-152">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="78591-152">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="78591-153">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="78591-153">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

