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
# <a name="imapiformmgrisinconflict"></a><span data-ttu-id="aca15-103">IMAPIFormMgr::IsInConflict</span><span class="sxs-lookup"><span data-stu-id="aca15-103">IMAPIFormMgr::IsInConflict</span></span>

  
  
<span data-ttu-id="aca15-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aca15-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aca15-105">フォームが独自のメッセージ競合を処理できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="aca15-105">Determines whether a form can handle its own message conflicts.</span></span> <span data-ttu-id="aca15-106">複数のユーザーが同時に編集した場合、メッセージが競合しています。</span><span class="sxs-lookup"><span data-stu-id="aca15-106">A message is in conflict if it has been simultaneously edited by more than one user.</span></span> <span data-ttu-id="aca15-107">これは、パブリック フォルダー内のメッセージに発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="aca15-107">This can happen to messages in public folders.</span></span>
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a><span data-ttu-id="aca15-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="aca15-108">Parameters</span></span>

 <span data-ttu-id="aca15-109">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="aca15-109">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="aca15-110">[in]メッセージの現在の状態を示すメッセージの **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティからコピーされたフラグのビットマスクへのポインター。</span><span class="sxs-lookup"><span data-stu-id="aca15-110">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of a message that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="aca15-111">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="aca15-111">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="aca15-112">[in]メッセージの状態に関する追加情報を提供するメッセージの **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティからコピーされたクライアント定義フラグまたはプロバイダー定義フラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="aca15-112">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of a message that provides additional information about the state of the message.</span></span>
    
 <span data-ttu-id="aca15-113">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="aca15-113">_szMessageClass_</span></span>
  
> <span data-ttu-id="aca15-114">[in]メッセージのメッセージ クラスの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="aca15-114">[in] A string that names the message's message class.</span></span>
    
 <span data-ttu-id="aca15-115">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="aca15-115">_pFolderFocus_</span></span>
  
> <span data-ttu-id="aca15-116">[in]メッセージを含むフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="aca15-116">[in] A pointer to the folder that contains the message.</span></span> <span data-ttu-id="aca15-117">_pFolderFocus_ パラメーターは、そのようなフォルダーが存在しない場合は NULL にできます (たとえば、メッセージが別のメッセージに埋め込まれている場合)。</span><span class="sxs-lookup"><span data-stu-id="aca15-117">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="aca15-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="aca15-118">Return value</span></span>

<span data-ttu-id="aca15-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="aca15-119">S_OK</span></span> 
  
> <span data-ttu-id="aca15-120">フォームは、独自のメッセージ競合を処理しない。</span><span class="sxs-lookup"><span data-stu-id="aca15-120">The form does not handle its own message conflicts.</span></span>
    
<span data-ttu-id="aca15-121">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="aca15-121">S_FALSE</span></span> 
  
> <span data-ttu-id="aca15-122">フォームは、独自のメッセージ競合を処理するか、渡された情報のメッセージが競合していない。</span><span class="sxs-lookup"><span data-stu-id="aca15-122">The form handles its own message conflicts, or the message for which information was passed is not in conflict.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="aca15-123">注釈</span><span class="sxs-lookup"><span data-stu-id="aca15-123">Remarks</span></span>

<span data-ttu-id="aca15-124">フォーム ビューアーは **IMAPIFormMgr::IsInConflict** メソッドを呼び出して、特定のフォームが独自のメッセージ競合を処理していないかどうかを検出します。</span><span class="sxs-lookup"><span data-stu-id="aca15-124">Form viewers call the **IMAPIFormMgr::IsInConflict** method to discover whether a particular form does not handle its own message conflicts.</span></span> <span data-ttu-id="aca15-125">**IsInConflict は**_、ulMessageFlags_ パラメーターと _ulMessageStatus_ パラメーターのビットマスクをチェックして、競合フラグの有無を確認します。</span><span class="sxs-lookup"><span data-stu-id="aca15-125">**IsInConflict** checks the bitmasks in the  _ulMessageFlags_ and  _ulMessageStatus_ parameters for the presence of a conflict flag.</span></span> <span data-ttu-id="aca15-126">競合フラグが設定されている場合 **、IsInConflict** は  _szMessageClass_ パラメーターで渡されたメッセージ クラスを解決し、フォームが独自の競合を処理しない場合は S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="aca15-126">If a conflict flag is set, **IsInConflict** resolves the message class passed in the  _szMessageClass_ parameter and returns S_OK if the form does not handle its own conflicts.</span></span> <span data-ttu-id="aca15-127">**IsInConflict は** 、フォームS_FALSE競合を処理する場合に、この値を返します。</span><span class="sxs-lookup"><span data-stu-id="aca15-127">**IsInConflict** returns S_FALSE if the form handles its own conflicts.</span></span> 
  
<span data-ttu-id="aca15-128">独自の競合を処理しないフォームは [、IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) メソッドを使用して開く必要があります。既存のフォーム オブジェクトを再利用することはできません。</span><span class="sxs-lookup"><span data-stu-id="aca15-128">A form that does not handle its own conflicts must be opened by using the [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) method and cannot reuse an existing form object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="aca15-129">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="aca15-129">Notes to callers</span></span>

<span data-ttu-id="aca15-130">通常、クライアント アプリケーションは、アプリケーションがフォルダー内の 1 つのメッセージから次のメッセージまたは前のメッセージに移動するときに競合に対処する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aca15-130">Client applications typically have to deal with conflicts when the applications move from one message to the next or previous message in a folder.</span></span> <span data-ttu-id="aca15-131">メッセージが競合しているが、そのメッセージのフォーム サーバーが競合を処理できる場合、クライアント アプリケーションは、次または前のメッセージを表示するための通常のコードを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aca15-131">If a message is in conflict, but the form server for that message can handle conflicts, the client application should execute its usual code for displaying the next or previous message.</span></span> <span data-ttu-id="aca15-132">フォーム サーバーが競合を処理できない場合、クライアント アプリケーションは、次または前のメッセージのメッセージ クラスを知らなかった場合と同様に続行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aca15-132">If the form server cannot handle conflicts, the client application should continue as if it was unaware of the message class of the next or previous message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="aca15-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="aca15-133">See also</span></span>



[<span data-ttu-id="aca15-134">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="aca15-134">IMAPIFormAdviseSink::OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md)
  
[<span data-ttu-id="aca15-135">PidTagMessageFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="aca15-135">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="aca15-136">PidTagMessageStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="aca15-136">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="aca15-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="aca15-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

