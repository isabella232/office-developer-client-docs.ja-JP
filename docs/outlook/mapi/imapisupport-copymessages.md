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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9cc4e3ba77395e09a6b95e8381fa402fc3cdff61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405157"
---
# <a name="imapisupportcopymessages"></a><span data-ttu-id="1dbe5-103">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="1dbe5-103">IMAPISupport::CopyMessages</span></span>

  
  
<span data-ttu-id="1dbe5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1dbe5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1dbe5-105">メッセージを 1 つのフォルダーから別のフォルダーにコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="1dbe5-105">Copies or moves messages from one folder to another folder.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="1dbe5-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1dbe5-106">Parameters</span></span>

 <span data-ttu-id="1dbe5-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="1dbe5-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="1dbe5-108">[in]コピーまたは移動するメッセージを含むフォルダーにアクセスするために使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1dbe5-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the folder that contains the messages to be copied or moved.</span></span>
    
 <span data-ttu-id="1dbe5-109">_lpSrcFolder_</span><span class="sxs-lookup"><span data-stu-id="1dbe5-109">_lpSrcFolder_</span></span>
  
> <span data-ttu-id="1dbe5-110">[in]コピーまたは移動するメッセージを含むフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1dbe5-110">[in] A pointer to the folder that contains the messages to be copied or moved.</span></span>
    
 <span data-ttu-id="1dbe5-111">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="1dbe5-111">_lpMsgList_</span></span>
  
> <span data-ttu-id="1dbe5-112">[in]コピーまたは移動するメッセージを識別するエントリ識別子の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1dbe5-112">[in] A pointer to an array of entry identifiers that identify the messages to be copied or moved.</span></span> 
    
 <span data-ttu-id="1dbe5-113">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="1dbe5-113">_lpDestInterface_</span></span>
  
> <span data-ttu-id="1dbe5-114">[in]コピーまたは移動されたメッセージの移動先フォルダーにアクセスするために使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1dbe5-114">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the destination folder for the copied or moved messages.</span></span>
    
 <span data-ttu-id="1dbe5-115">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="1dbe5-115">_lpDestFolder_</span></span>
  
> <span data-ttu-id="1dbe5-116">[in]コピーまたは移動されたメッセージの移動先フォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1dbe5-116">[in] A pointer to the destination folder for the copied or moved messages.</span></span> <span data-ttu-id="1dbe5-117">このフォルダーは開いている必要があります。</span><span class="sxs-lookup"><span data-stu-id="1dbe5-117">This folder must be open.</span></span>
    
 <span data-ttu-id="1dbe5-118">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1dbe5-118">_ulUIParam_</span></span>
  
> <span data-ttu-id="1dbe5-119">[in]進行状況インジケーターを表示する進行状況オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1dbe5-119">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="1dbe5-120">_lpProgress_ で NULL が渡された場合、メッセージ ストア プロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="1dbe5-120">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="1dbe5-121">_lpProgress パラメーター_ は _、ulFlags_ で MESSAGE_DIALOGフラグが設定されていない限り無視されます。</span><span class="sxs-lookup"><span data-stu-id="1dbe5-121">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="1dbe5-122">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="1dbe5-122">_lpProgress_</span></span>
  
> <span data-ttu-id="1dbe5-123">[in]進行状況インジケーターを表示する進行状況オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1dbe5-123">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="1dbe5-124">_lpProgress_ で NULL が渡された場合、メッセージ ストア プロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="1dbe5-124">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="1dbe5-125">_lpProgress パラメーター_ は _、ulFlags_ で MESSAGE_DIALOGフラグが設定されていない限り無視されます。</span><span class="sxs-lookup"><span data-stu-id="1dbe5-125">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="1dbe5-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1dbe5-126">_ulFlags_</span></span>
  
> <span data-ttu-id="1dbe5-127">[in]コピーまたは移動操作の実行方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="1dbe5-127">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="1dbe5-128">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="1dbe5-128">The following flags can be set:</span></span>
    
<span data-ttu-id="1dbe5-129">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="1dbe5-129">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="1dbe5-130">進行状況インジケーターの表示を要求します。</span><span class="sxs-lookup"><span data-stu-id="1dbe5-130">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="1dbe5-131">MESSAGE_MOVE</span><span class="sxs-lookup"><span data-stu-id="1dbe5-131">MESSAGE_MOVE</span></span> 
  
> <span data-ttu-id="1dbe5-132">メッセージはコピーの代わりに移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1dbe5-132">The messages should be moved, instead of copied.</span></span> <span data-ttu-id="1dbe5-133">このMESSAGE_MOVE設定されていない場合は、メッセージがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="1dbe5-133">If MESSAGE_MOVE is not set, the messages are copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1dbe5-134">戻り値</span><span class="sxs-lookup"><span data-stu-id="1dbe5-134">Return value</span></span>

<span data-ttu-id="1dbe5-135">S_OK</span><span class="sxs-lookup"><span data-stu-id="1dbe5-135">S_OK</span></span> 
  
> <span data-ttu-id="1dbe5-136">コピー操作または移動操作が成功しました。</span><span class="sxs-lookup"><span data-stu-id="1dbe5-136">The copy or move operation was successful.</span></span>
    
<span data-ttu-id="1dbe5-137">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="1dbe5-137">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="1dbe5-138">通常、ユーザーはダイアログ ボックスの [キャンセル] ボタンをクリック **して操作を** キャンセルしました。</span><span class="sxs-lookup"><span data-stu-id="1dbe5-138">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1dbe5-139">注釈</span><span class="sxs-lookup"><span data-stu-id="1dbe5-139">Remarks</span></span>

<span data-ttu-id="1dbe5-140">**IMAPISupport::CopyMessages** メソッドは、メッセージ ストア プロバイダーのサポート オブジェクトに実装されます。</span><span class="sxs-lookup"><span data-stu-id="1dbe5-140">The **IMAPISupport::CopyMessages** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="1dbe5-141">メッセージ ストア プロバイダーは [、IMAPIFolder::CopyMessages](imapifolder-copymessages.md)の実装で **IMAPISupport::CopyMessages** を呼び出して、1 つ以上のメッセージを 1 つのフォルダーから別のフォルダーにコピーまたは移動できます。</span><span class="sxs-lookup"><span data-stu-id="1dbe5-141">Message store providers can call **IMAPISupport::CopyMessages** in their implementation of [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) to copy or move one or more messages from one folder to another.</span></span> <span data-ttu-id="1dbe5-142">**IMAPISupport::CopyMessages** 呼び出しの一環として、メッセージ ストア プロバイダーは MAPI に進行状況インジケーターを表示する必要を指定できます。</span><span class="sxs-lookup"><span data-stu-id="1dbe5-142">As part of the **IMAPISupport::CopyMessages** call, the message store provider can specify that MAPI should display a progress indicator.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1dbe5-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="1dbe5-143">See also</span></span>



[<span data-ttu-id="1dbe5-144">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="1dbe5-144">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="1dbe5-145">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1dbe5-145">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

