---
title: IMAPISupportPrepareSubmit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.PrepareSubmit
api_type:
- COM
ms.assetid: 467242e3-96c9-4280-9cbc-9ecfe3f279cf
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 738eb346ec5388cbd94b32598236ef2ca05740f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425737"
---
# <a name="imapisupportpreparesubmit"></a><span data-ttu-id="a7c97-103">IMAPISupport::PrepareSubmit</span><span class="sxs-lookup"><span data-stu-id="a7c97-103">IMAPISupport::PrepareSubmit</span></span>

  
  
<span data-ttu-id="a7c97-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7c97-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7c97-105">MAPI スプーラーに送信するメッセージを準備します。</span><span class="sxs-lookup"><span data-stu-id="a7c97-105">Prepares a message for submission to the MAPI spooler.</span></span>
  
```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a7c97-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a7c97-106">Parameters</span></span>

 <span data-ttu-id="a7c97-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="a7c97-107">_lpMessage_</span></span>
  
> <span data-ttu-id="a7c97-108">[in]準備するメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a7c97-108">[in] A pointer to the message to prepare.</span></span>
    
 <span data-ttu-id="a7c97-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="a7c97-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="a7c97-110">[in, out]入力では  _、lpulFlags_ パラメーターは予約済みで、ゼロである必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7c97-110">[in, out] On input, the  _lpulFlags_ parameter is reserved and must be zero.</span></span> <span data-ttu-id="a7c97-111">出力では  _、lpulFlags は_ NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7c97-111">On output,  _lpulFlags_ must be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a7c97-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="a7c97-112">Return value</span></span>

<span data-ttu-id="a7c97-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="a7c97-113">S_OK</span></span> 
  
> <span data-ttu-id="a7c97-114">メッセージが正常に準備されました。</span><span class="sxs-lookup"><span data-stu-id="a7c97-114">The message was successfully prepared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a7c97-115">注釈</span><span class="sxs-lookup"><span data-stu-id="a7c97-115">Remarks</span></span>

<span data-ttu-id="a7c97-116">**IMAPISupport::P repareSubmit** メソッドは、メッセージ ストア プロバイダーのサポート オブジェクトに実装されます。</span><span class="sxs-lookup"><span data-stu-id="a7c97-116">The **IMAPISupport::PrepareSubmit** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="a7c97-117">メッセージ ストア プロバイダーは [、IMessage::SubmitMessage](imessage-submitmessage.md)メソッドの実装で **PrepareSubmit** を呼び出して、MAPI スプーラーに送信するメッセージを準備します。</span><span class="sxs-lookup"><span data-stu-id="a7c97-117">Message store providers call **PrepareSubmit** in their implementation of the [IMessage::SubmitMessage](imessage-submitmessage.md) method to prepare a message for submission to the MAPI spooler.</span></span> 
  
 <span data-ttu-id="a7c97-118">**PrepareSubmit を** 使用して、MSGFLAG_RESEND ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティに PR_MESSAGE_FLAGS フラグが設定 **されている** メッセージを処理します。</span><span class="sxs-lookup"><span data-stu-id="a7c97-118">**PrepareSubmit** is used to handle messages that have the MSGFLAG_RESEND flag set in their **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="a7c97-119">MSGFLAG_RESEND送信が失敗した場合に再送信する要求を含むメッセージに対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="a7c97-119">MSGFLAG_RESEND is set for messages that include a request to be resent when an initial transmission fails.</span></span> <span data-ttu-id="a7c97-120">**PrepareSubmit は** 、受信者リスト内の受信者がメッセージを正常に受信し、受信しなかった受信者を決定します。</span><span class="sxs-lookup"><span data-stu-id="a7c97-120">**PrepareSubmit** determines which of the recipients in the recipient list successfully received the message and which did not.</span></span> 
  
<span data-ttu-id="a7c97-121">受信者リストにアクセスするには **、PrepareSubmit は** メッセージの [IMessage::GetRecipientTable メソッドを呼び出](imessage-getrecipienttable.md) します。</span><span class="sxs-lookup"><span data-stu-id="a7c97-121">To access the recipient list, **PrepareSubmit** calls the message's [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method.</span></span> <span data-ttu-id="a7c97-122">受信者データを取得するには **、PrepareSubmit は** 受信者テーブルの [IMAPITable::QueryRows メソッドを呼び出](imapitable-queryrows.md) します。</span><span class="sxs-lookup"><span data-stu-id="a7c97-122">To retrieve the recipient data, **PrepareSubmit** calls the recipient table's [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> <span data-ttu-id="a7c97-123">テーブル内の各行について **、PrepareSubmit** は PR_RECIPIENT_TYPE **(** [PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) プロパティをチェックし、次のいずれかのアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="a7c97-123">For each row in the table, **PrepareSubmit** checks the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property and takes one of the following actions:</span></span>
  
- <span data-ttu-id="a7c97-124">このフラグMAPI_SUBMITTED設定されている場合 **、PrepareSubmit** はフラグをクリアし、PR_RESPONSIBILITY **(** [PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティを FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="a7c97-124">If the MAPI_SUBMITTED flag is set, **PrepareSubmit** clears the flag and sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property to FALSE.</span></span>
    
- <span data-ttu-id="a7c97-125">このフラグMAPI_SUBMITTED設定されていない場合は **、PrepareSubmit** は設定PR_RECIPIENT_TYPEにMAPI_P1し、PR_RESPONSIBILITY **TRUE** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a7c97-125">If the MAPI_SUBMITTED flag is not set, **PrepareSubmit** changes **PR_RECIPIENT_TYPE** to MAPI_P1 and sets **PR_RESPONSIBILITY** to TRUE.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="a7c97-126">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="a7c97-126">Notes to callers</span></span>

<span data-ttu-id="a7c97-127">**PrepareSubmit** を呼び出す前に [、IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)メソッドを呼び出し _、ulFlags_ パラメーターに NOTIFY_READYTOSEND フラグを設定してください。</span><span class="sxs-lookup"><span data-stu-id="a7c97-127">Before you call **PrepareSubmit**, be sure you have called the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method and set the NOTIFY_READYTOSEND flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="a7c97-128">**SpoolerNotify 呼び出し** は **、PrepareSubmit** の呼び出しの前にセッションごとに 1 回行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7c97-128">The **SpoolerNotify** call must be made once per session before the call to **PrepareSubmit**.</span></span> <span data-ttu-id="a7c97-129">**SpoolerNotify** は MAPI スプーラーを同期し、必要なすべてのトランスポート プロバイダーがログオンし、そのアドレスの種類が登録されます。</span><span class="sxs-lookup"><span data-stu-id="a7c97-129">**SpoolerNotify** synchronizes the MAPI spooler and ensures that all needed transport providers are logged on and their address types are registered.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a7c97-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="a7c97-130">See also</span></span>



[<span data-ttu-id="a7c97-131">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="a7c97-131">IMAPIFolder::GetMessageStatus</span></span>](imapifolder-getmessagestatus.md)
  
[<span data-ttu-id="a7c97-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="a7c97-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="a7c97-133">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a7c97-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

