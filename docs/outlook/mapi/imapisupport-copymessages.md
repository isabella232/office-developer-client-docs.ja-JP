---
title: imapisupportcopymessages
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356533"
---
# <a name="imapisupportcopymessages"></a><span data-ttu-id="ef541-103">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="ef541-103">IMAPISupport::CopyMessages</span></span>

  
  
<span data-ttu-id="ef541-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef541-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ef541-105">メッセージを1つのフォルダーから別のフォルダーにコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="ef541-105">Copies or moves messages from one folder to another folder.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="ef541-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ef541-106">Parameters</span></span>

 <span data-ttu-id="ef541-107">_lpsrcinterface_</span><span class="sxs-lookup"><span data-stu-id="ef541-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="ef541-108">順番コピーまたは移動するメッセージを含むフォルダーへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ef541-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the folder that contains the messages to be copied or moved.</span></span>
    
 <span data-ttu-id="ef541-109">_lpsrcfolder_</span><span class="sxs-lookup"><span data-stu-id="ef541-109">_lpSrcFolder_</span></span>
  
> <span data-ttu-id="ef541-110">順番コピーまたは移動するメッセージを含むフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ef541-110">[in] A pointer to the folder that contains the messages to be copied or moved.</span></span>
    
 <span data-ttu-id="ef541-111">_lpmsglist_</span><span class="sxs-lookup"><span data-stu-id="ef541-111">_lpMsgList_</span></span>
  
> <span data-ttu-id="ef541-112">順番コピーまたは移動するメッセージを識別するエントリ識別子の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ef541-112">[in] A pointer to an array of entry identifiers that identify the messages to be copied or moved.</span></span> 
    
 <span data-ttu-id="ef541-113">_lpdestinterface_</span><span class="sxs-lookup"><span data-stu-id="ef541-113">_lpDestInterface_</span></span>
  
> <span data-ttu-id="ef541-114">順番コピーまたは移動されたメッセージの宛先フォルダーへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ef541-114">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the destination folder for the copied or moved messages.</span></span>
    
 <span data-ttu-id="ef541-115">_lpdestfolder_</span><span class="sxs-lookup"><span data-stu-id="ef541-115">_lpDestFolder_</span></span>
  
> <span data-ttu-id="ef541-116">順番コピーまたは移動されたメッセージの宛先フォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ef541-116">[in] A pointer to the destination folder for the copied or moved messages.</span></span> <span data-ttu-id="ef541-117">このフォルダーは開いている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef541-117">This folder must be open.</span></span>
    
 <span data-ttu-id="ef541-118">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="ef541-118">_ulUIParam_</span></span>
  
> <span data-ttu-id="ef541-119">順番進行状況インジケーターを表示する progress オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ef541-119">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="ef541-120">_lpprogress_で NULL が渡された場合、メッセージストアプロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="ef541-120">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="ef541-121">MESSAGE_DIALOG フラグが_ulflags_で設定されていない場合、 _lpprogress_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="ef541-121">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="ef541-122">_lpprogress_</span><span class="sxs-lookup"><span data-stu-id="ef541-122">_lpProgress_</span></span>
  
> <span data-ttu-id="ef541-123">順番進行状況インジケーターを表示する progress オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ef541-123">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="ef541-124">_lpprogress_で NULL が渡された場合、メッセージストアプロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="ef541-124">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="ef541-125">MESSAGE_DIALOG フラグが_ulflags_で設定されていない場合、 _lpprogress_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="ef541-125">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="ef541-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ef541-126">_ulFlags_</span></span>
  
> <span data-ttu-id="ef541-127">順番コピー操作または移動操作の実行方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="ef541-127">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="ef541-128">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="ef541-128">The following flags can be set:</span></span>
    
<span data-ttu-id="ef541-129">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="ef541-129">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="ef541-130">進行状況インジケーターの表示を要求します。</span><span class="sxs-lookup"><span data-stu-id="ef541-130">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="ef541-131">MESSAGE_MOVE</span><span class="sxs-lookup"><span data-stu-id="ef541-131">MESSAGE_MOVE</span></span> 
  
> <span data-ttu-id="ef541-132">メッセージはコピーではなく移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef541-132">The messages should be moved, instead of copied.</span></span> <span data-ttu-id="ef541-133">MESSAGE_MOVE が設定されていない場合は、メッセージがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="ef541-133">If MESSAGE_MOVE is not set, the messages are copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ef541-134">戻り値</span><span class="sxs-lookup"><span data-stu-id="ef541-134">Return value</span></span>

<span data-ttu-id="ef541-135">S_OK</span><span class="sxs-lookup"><span data-stu-id="ef541-135">S_OK</span></span> 
  
> <span data-ttu-id="ef541-136">コピーまたは移動操作が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="ef541-136">The copy or move operation was successful.</span></span>
    
<span data-ttu-id="ef541-137">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="ef541-137">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="ef541-138">ユーザーが操作をキャンセルしました。通常は、ダイアログボックスの **[キャンセル**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef541-138">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ef541-139">解説</span><span class="sxs-lookup"><span data-stu-id="ef541-139">Remarks</span></span>

<span data-ttu-id="ef541-140">**imapisupport:: copymessages**メソッドは、メッセージストアプロバイダーサポートオブジェクトに実装されています。</span><span class="sxs-lookup"><span data-stu-id="ef541-140">The **IMAPISupport::CopyMessages** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="ef541-141">メッセージストアプロバイダーは、imapisupport [:: copymessages](imapifolder-copymessages.md)を使用して、1つまたは複数のメッセージを別のフォルダーにコピーまたは移動する**imapisupport:: copymessages**を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="ef541-141">Message store providers can call **IMAPISupport::CopyMessages** in their implementation of [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) to copy or move one or more messages from one folder to another.</span></span> <span data-ttu-id="ef541-142">**imapisupport:: copymessages**呼び出しの一部として、メッセージストアプロバイダーは MAPI が進行状況インジケーターを表示するように指定できます。</span><span class="sxs-lookup"><span data-stu-id="ef541-142">As part of the **IMAPISupport::CopyMessages** call, the message store provider can specify that MAPI should display a progress indicator.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ef541-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="ef541-143">See also</span></span>



[<span data-ttu-id="ef541-144">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="ef541-144">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="ef541-145">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ef541-145">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

