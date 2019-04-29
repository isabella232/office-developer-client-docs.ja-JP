---
title: IMAPIFormMgrIsInConflict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgrIsInConflict
api_type:
- COM
ms.assetid: 5ca86ee8-1bf6-4ec8-95b3-575c22fbb170
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 87432d8982c5dc1f64396187739e97314edb385c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412885"
---
# <a name="imapiformmgrisinconflict"></a><span data-ttu-id="4305f-103">IMAPIFormMgr::IsInConflict</span><span class="sxs-lookup"><span data-stu-id="4305f-103">IMAPIFormMgr::IsInConflict</span></span>

  
  
<span data-ttu-id="4305f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4305f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4305f-105">フォームが独自のメッセージ競合を処理できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4305f-105">Determines whether a form can handle its own message conflicts.</span></span> <span data-ttu-id="4305f-106">メッセージが複数のユーザーによって同時に編集されている場合、メッセージは競合しています。</span><span class="sxs-lookup"><span data-stu-id="4305f-106">A message is in conflict if it has been simultaneously edited by more than one user.</span></span> <span data-ttu-id="4305f-107">これは、パブリックフォルダー内のメッセージに発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4305f-107">This can happen to messages in public folders.</span></span>
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a><span data-ttu-id="4305f-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4305f-108">Parameters</span></span>

 <span data-ttu-id="4305f-109">_ulmessageflags_</span><span class="sxs-lookup"><span data-stu-id="4305f-109">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="4305f-110">順番メッセージの現在の状態を示す、メッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティからコピーされたフラグのビットマスクへのポインター。</span><span class="sxs-lookup"><span data-stu-id="4305f-110">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of a message that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="4305f-111">_ulmessagestatus_</span><span class="sxs-lookup"><span data-stu-id="4305f-111">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="4305f-112">順番メッセージの状態に関する追加情報を提供する、メッセージの**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティからコピーされた、クライアント定義またはプロバイダー定義のフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="4305f-112">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of a message that provides additional information about the state of the message.</span></span>
    
 <span data-ttu-id="4305f-113">_szmessageclass_</span><span class="sxs-lookup"><span data-stu-id="4305f-113">_szMessageClass_</span></span>
  
> <span data-ttu-id="4305f-114">順番メッセージのメッセージクラスの名前を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="4305f-114">[in] A string that names the message's message class.</span></span>
    
 <span data-ttu-id="4305f-115">_pfolderfocus_</span><span class="sxs-lookup"><span data-stu-id="4305f-115">_pFolderFocus_</span></span>
  
> <span data-ttu-id="4305f-116">順番メッセージを含むフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="4305f-116">[in] A pointer to the folder that contains the message.</span></span> <span data-ttu-id="4305f-117">このようなフォルダーが存在しない場合 (たとえば、メッセージが別のメッセージに埋め込まれている場合) は、 _pfolderfocus_パラメーターを NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="4305f-117">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4305f-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="4305f-118">Return value</span></span>

<span data-ttu-id="4305f-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="4305f-119">S_OK</span></span> 
  
> <span data-ttu-id="4305f-120">フォームでは、独自のメッセージの競合は処理されません。</span><span class="sxs-lookup"><span data-stu-id="4305f-120">The form does not handle its own message conflicts.</span></span>
    
<span data-ttu-id="4305f-121">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="4305f-121">S_FALSE</span></span> 
  
> <span data-ttu-id="4305f-122">フォームが独自のメッセージ競合を処理するか、渡された情報が競合していないことを示すメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="4305f-122">The form handles its own message conflicts, or the message for which information was passed is not in conflict.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4305f-123">注釈</span><span class="sxs-lookup"><span data-stu-id="4305f-123">Remarks</span></span>

<span data-ttu-id="4305f-124">フォームビューアーは、 **imapiformmgr:: IsInConflict**メソッドを呼び出して、特定のフォームが独自のメッセージ競合を処理していないかどうかを検出します。</span><span class="sxs-lookup"><span data-stu-id="4305f-124">Form viewers call the **IMAPIFormMgr::IsInConflict** method to discover whether a particular form does not handle its own message conflicts.</span></span> <span data-ttu-id="4305f-125">**IsInConflict**は、競合フラグが存在するかどうかについて、 _ulmessageflags_および_ulmessageflags_パラメーターのビットマスクをチェックします。</span><span class="sxs-lookup"><span data-stu-id="4305f-125">**IsInConflict** checks the bitmasks in the  _ulMessageFlags_ and  _ulMessageStatus_ parameters for the presence of a conflict flag.</span></span> <span data-ttu-id="4305f-126">競合フラグが設定されている場合、 **IsInConflict**は、 _szmessageclass_パラメーターで渡されたメッセージクラスを解決し、フォームが自身の競合を処理していない場合は S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="4305f-126">If a conflict flag is set, **IsInConflict** resolves the message class passed in the  _szMessageClass_ parameter and returns S_OK if the form does not handle its own conflicts.</span></span> <span data-ttu-id="4305f-127">フォームが自身の競合を処理する場合、 **IsInConflict**は S_FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="4305f-127">**IsInConflict** returns S_FALSE if the form handles its own conflicts.</span></span> 
  
<span data-ttu-id="4305f-128">独自の競合を処理しないフォームは、 [imapiformmgr:: loadform](imapiformmgr-loadform.md)メソッドを使用して開く必要があります。また、既存の form オブジェクトを再利用することはできません。</span><span class="sxs-lookup"><span data-stu-id="4305f-128">A form that does not handle its own conflicts must be opened by using the [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) method and cannot reuse an existing form object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4305f-129">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="4305f-129">Notes to callers</span></span>

<span data-ttu-id="4305f-130">通常、クライアントアプリケーションは、あるメッセージからフォルダー内の次または前のメッセージにアプリケーションが移動したときに、競合を処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4305f-130">Client applications typically have to deal with conflicts when the applications move from one message to the next or previous message in a folder.</span></span> <span data-ttu-id="4305f-131">メッセージが競合していても、そのメッセージのフォームサーバーが競合を処理できる場合、クライアントアプリケーションは、次のメッセージまたは前のメッセージを表示するために、通常のコードを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4305f-131">If a message is in conflict, but the form server for that message can handle conflicts, the client application should execute its usual code for displaying the next or previous message.</span></span> <span data-ttu-id="4305f-132">フォームサーバーが競合を処理できない場合は、次または前のメッセージのメッセージクラスを認識していない場合と同様に、クライアントアプリケーションを続行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4305f-132">If the form server cannot handle conflicts, the client application should continue as if it was unaware of the message class of the next or previous message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4305f-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="4305f-133">See also</span></span>



[<span data-ttu-id="4305f-134">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="4305f-134">IMAPIFormAdviseSink::OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md)
  
[<span data-ttu-id="4305f-135">PidTagMessageFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4305f-135">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="4305f-136">PidTagMessageStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4305f-136">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="4305f-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4305f-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

