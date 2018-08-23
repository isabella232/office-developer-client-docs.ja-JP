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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 22562e1177c9a649bc66b25b5e8e9e6ecc8e397c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803687"
---
# <a name="preprocessmessage"></a><span data-ttu-id="fb374-103">PreprocessMessage</span><span class="sxs-lookup"><span data-stu-id="fb374-103">PreprocessMessage</span></span>

  
  
<span data-ttu-id="fb374-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fb374-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fb374-105">メッセージの内容またはメッセージの形式を指定する関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="fb374-105">Defines a function that preprocesses message contents or the format of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fb374-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="fb374-106">Header file:</span></span>  <br/> |<span data-ttu-id="fb374-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="fb374-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="fb374-108">によって実装される関数の定義:</span><span class="sxs-lookup"><span data-stu-id="fb374-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="fb374-109">トランスポート プロバイダー</span><span class="sxs-lookup"><span data-stu-id="fb374-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="fb374-110">によって呼び出される関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="fb374-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="fb374-111">MAPI スプーラー</span><span class="sxs-lookup"><span data-stu-id="fb374-111">MAPI spooler</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="fb374-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fb374-112">Parameters</span></span>

 <span data-ttu-id="fb374-113">_lpvSession_</span><span class="sxs-lookup"><span data-stu-id="fb374-113">_lpvSession_</span></span>
  
> <span data-ttu-id="fb374-114">[in]使用するセッションへのポインター。</span><span class="sxs-lookup"><span data-stu-id="fb374-114">[in] Pointer to the session to be used.</span></span> 
    
 <span data-ttu-id="fb374-115">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="fb374-115">_lpMessage_</span></span>
  
> <span data-ttu-id="fb374-116">[in]前処理が必要にメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="fb374-116">[in] Pointer to the message to be preprocessed.</span></span> 
    
 <span data-ttu-id="fb374-117">_lpAdrBook_</span><span class="sxs-lookup"><span data-stu-id="fb374-117">_lpAdrBook_</span></span>
  
> <span data-ttu-id="fb374-118">[in]ユーザーがメッセージの受信者を選択する必要があります、アドレス帳へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fb374-118">[in] Pointer to the address book from which the user should select recipients for the message.</span></span> 
    
 <span data-ttu-id="fb374-119">_lpFolder_</span><span class="sxs-lookup"><span data-stu-id="fb374-119">_lpFolder_</span></span>
  
> <span data-ttu-id="fb374-120">[で [チェック アウト]フォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="fb374-120">[in, out] Pointer to a folder.</span></span> <span data-ttu-id="fb374-121">入力では、 _lpFolder_のパラメーターは、前処理が必要にメッセージを含むフォルダーにポイントです。</span><span class="sxs-lookup"><span data-stu-id="fb374-121">On input, the  _lpFolder_ parameter points to the folder that contains messages to be preprocessed.</span></span> <span data-ttu-id="fb374-122">出力では、 _lpFolder_は、プリプロセス済みのメッセージが設定されているフォルダーをポイントします。</span><span class="sxs-lookup"><span data-stu-id="fb374-122">On output,  _lpFolder_ points to the folder where preprocessed messages have been placed.</span></span> 
    
 <span data-ttu-id="fb374-123">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="fb374-123">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="fb374-124">[in]メモリの割り当てに使用する[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fb374-124">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="fb374-125">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="fb374-125">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="fb374-126">[in]追加メモリの割り当てに使用する[MAPIAllocateMore](mapiallocatemore.md)関数へのポインターに必要な場所です。</span><span class="sxs-lookup"><span data-stu-id="fb374-126">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory where required.</span></span> 
    
 <span data-ttu-id="fb374-127">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="fb374-127">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="fb374-128">[in]メモリを解放するために使用する、 [MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fb374-128">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="fb374-129">_lpcOutbound_</span><span class="sxs-lookup"><span data-stu-id="fb374-129">_lpcOutbound_</span></span>
  
> <span data-ttu-id="fb374-130">[out]_LpppMessage_パラメーターが指す配列内のメッセージの数へのポインターです。</span><span class="sxs-lookup"><span data-stu-id="fb374-130">[out] Pointer to the number of messages in the array pointed to by the  _lpppMessage_ parameter.</span></span> 
    
 <span data-ttu-id="fb374-131">_lpppMessage_</span><span class="sxs-lookup"><span data-stu-id="fb374-131">_lpppMessage_</span></span>
  
> <span data-ttu-id="fb374-132">[out]ポインターの配列へのポインターへのポインターでは、前処理またはそれ以外の場合にメッセージを生成します。</span><span class="sxs-lookup"><span data-stu-id="fb374-132">[out] Pointer to a pointer to an array of pointers to preprocessed or otherwise generated messages.</span></span> 
    
 <span data-ttu-id="fb374-133">_lppRecipList_</span><span class="sxs-lookup"><span data-stu-id="fb374-133">_lppRecipList_</span></span>
  
> <span data-ttu-id="fb374-134">[out]オプションへのポインターには、メッセージが配信できなかった、プリプロセッサが検出された受信者を一覧表示、 [ADRLIST](adrlist.md)構造体が返されます。</span><span class="sxs-lookup"><span data-stu-id="fb374-134">[out] Pointer to an optional returned [ADRLIST](adrlist.md) structure, listing preprocessor-detected recipients for which the message is undeliverable.</span></span> <span data-ttu-id="fb374-135">このリストの内容の詳細については、 [IMAPISupport::StatusRecips](imapisupport-statusrecips.md)メソッドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fb374-135">For more information about the contents of this list, see the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fb374-136">�߂�l</span><span class="sxs-lookup"><span data-stu-id="fb374-136">Return value</span></span>

<span data-ttu-id="fb374-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="fb374-137">S_OK</span></span>
  
> <span data-ttu-id="fb374-138">メッセージの内容は、正常にプリプロセス済みでした。</span><span class="sxs-lookup"><span data-stu-id="fb374-138">Message contents were successfully preprocessed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fb374-139">注釈</span><span class="sxs-lookup"><span data-stu-id="fb374-139">Remarks</span></span>

<span data-ttu-id="fb374-140">メッセージ トランスポート プロバイダー プリプロセッサでは、メッセージのプリプロセス中に進行状況のインジケーターを表示できます。</span><span class="sxs-lookup"><span data-stu-id="fb374-140">A transport-provider message preprocessor can present a progress indicator during message preprocessing.</span></span> <span data-ttu-id="fb374-141">ただし、メッセージのプリプロセス中にユーザーとの対話を必要とするダイアログ ボックスが表示されない必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb374-141">However, it should never present a dialog box requiring user interaction during message preprocessing.</span></span> 
  
<span data-ttu-id="fb374-142">プリプロセッサでは、大量のデータを送信メッセージに追加するときは、特定の手順を行ってください。</span><span class="sxs-lookup"><span data-stu-id="fb374-142">When a preprocessor adds large amounts of data to an outbound message, certain procedures should be followed.</span></span> <span data-ttu-id="fb374-143">この種類のメッセージは、時間のかかる処理をリモート ストアにアクセスするのにはプリプロセッサの原因で、サーバー ベースのメッセージ ・ ストアに格納できます。</span><span class="sxs-lookup"><span data-stu-id="fb374-143">This type of message can be stored in a server-based message store, causing the preprocessor to access a remote store, a time-consuming procedure.</span></span> <span data-ttu-id="fb374-144">これを行うことを避けるためには、プリプロセッサの大量の領域は、ローカル メッセージ ストアのデータを格納し、メッセージのローカル ストアへの参照を提供することを可能にするオプションが必要です。</span><span class="sxs-lookup"><span data-stu-id="fb374-144">To avoid having to do so, the preprocessor should have an option that enables it to store data that takes a large amount of space in a local message store and to provide a reference to that local store in the message.</span></span> 
  
<span data-ttu-id="fb374-145">プリプロセッサは最初**PreprocessMessage**ベースの関数に渡されたオブジェクトのいずれかを開放しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="fb374-145">The preprocessor should not release any of the objects originally passed to the **PreprocessMessage** based function.</span></span> 
  
<span data-ttu-id="fb374-146">MAPI スプーラーは、 **PreprocessMessage**関数を呼び出すことができます、前にトランスポート プロバイダーは、必要がありますに登録されている関数、 [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md)メソッドを呼び出す。</span><span class="sxs-lookup"><span data-stu-id="fb374-146">Before the MAPI spooler can call a **PreprocessMessage** function, the transport provider must have registered the function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> <span data-ttu-id="fb374-147">**PreprocessMessage**関数を呼び出すと、関数が戻るまでにメッセージを送信する、スプーラーを続行できません。</span><span class="sxs-lookup"><span data-stu-id="fb374-147">After calling a **PreprocessMessage** function, the spooler cannot continue submitting a message until the function returns.</span></span> 
  
<span data-ttu-id="fb374-148">MAPI スプーラーは、メッセージを送信するタスクを所有しています。</span><span class="sxs-lookup"><span data-stu-id="fb374-148">The MAPI spooler owns the task of submitting messages.</span></span> <span data-ttu-id="fb374-149">これは、元のメッセージがメッセージのポインターの配列に配置されることはありませんし、 **SubmitMessage**メソッドの呼び出しが必要ではないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="fb374-149">This means the original message is never placed in an array of message pointers and that a call to the **SubmitMessage** methods is never required.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fb374-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="fb374-150">See also</span></span>



[<span data-ttu-id="fb374-151">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="fb374-151">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="fb374-152">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="fb374-152">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="fb374-153">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="fb374-153">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

