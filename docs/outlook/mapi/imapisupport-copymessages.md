---
title: IMAPISupportCopyMessages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CopyMessages
api_type:
- COM
ms.assetid: 70f67614-af0d-43f6-99f6-391a2f5673cb
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0d3f540a14c833e0ee0ed212f6f3b3b709d72ec0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591038"
---
# <a name="imapisupportcopymessages"></a><span data-ttu-id="a84de-103">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="a84de-103">IMAPISupport::CopyMessages</span></span>

  
  
<span data-ttu-id="a84de-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a84de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a84de-105">別のフォルダーに 1 つのフォルダーからのコピーや移動メッセージです。</span><span class="sxs-lookup"><span data-stu-id="a84de-105">Copies or moves messages from one folder to another folder.</span></span>
  
```cpp
HRESULT CopyMessages(
  LPCIID lpSrcInterface,
  LPVOID lpSrcFolder,
  LPENTRYLIST lpMsgList,
  LPCIID lpDestInterface,
  LPVOID lpDestFolder,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a84de-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a84de-106">Parameters</span></span>

 <span data-ttu-id="a84de-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="a84de-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="a84de-108">[in]コピーまたは移動するメッセージを含むフォルダーへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a84de-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the folder that contains the messages to be copied or moved.</span></span>
    
 <span data-ttu-id="a84de-109">_lpSrcFolder_</span><span class="sxs-lookup"><span data-stu-id="a84de-109">_lpSrcFolder_</span></span>
  
> <span data-ttu-id="a84de-110">[in]コピーまたは移動するメッセージを含むフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a84de-110">[in] A pointer to the folder that contains the messages to be copied or moved.</span></span>
    
 <span data-ttu-id="a84de-111">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="a84de-111">_lpMsgList_</span></span>
  
> <span data-ttu-id="a84de-112">[in]コピーまたは移動するメッセージを識別するエントリの識別子の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a84de-112">[in] A pointer to an array of entry identifiers that identify the messages to be copied or moved.</span></span> 
    
 <span data-ttu-id="a84de-113">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="a84de-113">_lpDestInterface_</span></span>
  
> <span data-ttu-id="a84de-114">[in]コピーまたは移動されたメッセージのコピー先フォルダーへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a84de-114">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the destination folder for the copied or moved messages.</span></span>
    
 <span data-ttu-id="a84de-115">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="a84de-115">_lpDestFolder_</span></span>
  
> <span data-ttu-id="a84de-116">[in]先のフォルダーにコピーまたは移動されたメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a84de-116">[in] A pointer to the destination folder for the copied or moved messages.</span></span> <span data-ttu-id="a84de-117">このフォルダーを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="a84de-117">This folder must be open.</span></span>
    
 <span data-ttu-id="a84de-118">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a84de-118">_ulUIParam_</span></span>
  
> <span data-ttu-id="a84de-119">[in]進行状況インジケーターを表示する進行中のオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a84de-119">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="a84de-120">_LpProgress_に NULL を渡した場合、メッセージ ストア プロバイダーは、MAPI 処理中のオブジェクトの実装を使用して進行状況のインジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="a84de-120">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="a84de-121">_UlFlags_に MESSAGE_DIALOG フラグが設定されていない限り、 _lpProgress_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="a84de-121">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="a84de-122">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="a84de-122">_lpProgress_</span></span>
  
> <span data-ttu-id="a84de-123">[in]進行状況インジケーターを表示する進行中のオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a84de-123">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="a84de-124">_LpProgress_に NULL を渡した場合、メッセージ ストア プロバイダーは、MAPI 処理中のオブジェクトの実装を使用して進行状況のインジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="a84de-124">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="a84de-125">_UlFlags_に MESSAGE_DIALOG フラグが設定されていない限り、 _lpProgress_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="a84de-125">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="a84de-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a84de-126">_ulFlags_</span></span>
  
> <span data-ttu-id="a84de-127">[in]コピーまたは移動操作を実現する方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="a84de-127">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="a84de-128">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="a84de-128">The following flags can be set:</span></span>
    
<span data-ttu-id="a84de-129">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="a84de-129">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="a84de-130">進行状況インジケーターの表示を要求します。</span><span class="sxs-lookup"><span data-stu-id="a84de-130">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="a84de-131">MESSAGE_MOVE</span><span class="sxs-lookup"><span data-stu-id="a84de-131">MESSAGE_MOVE</span></span> 
  
> <span data-ttu-id="a84de-132">メッセージを移動する必要があるのではなくコピーします。</span><span class="sxs-lookup"><span data-stu-id="a84de-132">The messages should be moved, instead of copied.</span></span> <span data-ttu-id="a84de-133">MESSAGE_MOVE が設定されていない場合、メッセージがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="a84de-133">If MESSAGE_MOVE is not set, the messages are copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a84de-134">�߂�l</span><span class="sxs-lookup"><span data-stu-id="a84de-134">Return value</span></span>

<span data-ttu-id="a84de-135">S_OK</span><span class="sxs-lookup"><span data-stu-id="a84de-135">S_OK</span></span> 
  
> <span data-ttu-id="a84de-136">コピーまたは移動操作が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="a84de-136">The copy or move operation was successful.</span></span>
    
<span data-ttu-id="a84de-137">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="a84de-137">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="a84de-138">ユーザー操作がキャンセルされました、通常ダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。</span><span class="sxs-lookup"><span data-stu-id="a84de-138">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a84de-139">注釈</span><span class="sxs-lookup"><span data-stu-id="a84de-139">Remarks</span></span>

<span data-ttu-id="a84de-140">メッセージ ストア プロバイダーのサポート オブジェクトの**IMAPISupport::CopyMessages**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="a84de-140">The **IMAPISupport::CopyMessages** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="a84de-141">メッセージ ストア プロバイダーは、コピーまたは別の 1 つのフォルダーから 1 つまたは複数のメッセージを移動するのには、 [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)の実装では、 **IMAPISupport::CopyMessages**を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="a84de-141">Message store providers can call **IMAPISupport::CopyMessages** in their implementation of [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) to copy or move one or more messages from one folder to another.</span></span> <span data-ttu-id="a84de-142">**IMAPISupport::CopyMessages**の呼び出しの一部として、メッセージ ストア プロバイダーが、MAPI は、進行状況インジケーターを表示することを指定できます。</span><span class="sxs-lookup"><span data-stu-id="a84de-142">As part of the **IMAPISupport::CopyMessages** call, the message store provider can specify that MAPI should display a progress indicator.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a84de-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="a84de-143">See also</span></span>



[<span data-ttu-id="a84de-144">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="a84de-144">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="a84de-145">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a84de-145">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

