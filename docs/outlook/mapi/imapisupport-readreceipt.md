---
title: IMAPISupportReadReceipt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ReadReceipt
api_type:
- COM
ms.assetid: ef31b61a-93b6-4ae8-bc71-f5ef5caf43f4
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e785d42639d51dab154a0bde239f858a92ddd143
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588623"
---
# <a name="imapisupportreadreceipt"></a><span data-ttu-id="df216-103">IMAPISupport::ReadReceipt</span><span class="sxs-lookup"><span data-stu-id="df216-103">IMAPISupport::ReadReceipt</span></span>

  
  
<span data-ttu-id="df216-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df216-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df216-105">読み取りまたはメッセージの nonread のレポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="df216-105">Generates a read or nonread report for a message.</span></span>
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a><span data-ttu-id="df216-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="df216-106">Parameters</span></span>

 <span data-ttu-id="df216-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="df216-107">_ulFlags_</span></span>
  
> <span data-ttu-id="df216-108">[in]読み取りまたは nonread のレポートの生成方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="df216-108">[in] A bitmask of flags that controls how the read or nonread report is generated.</span></span> <span data-ttu-id="df216-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="df216-109">The following flag can be set:</span></span>
    
<span data-ttu-id="df216-110">MAPI_NON_READ</span><span class="sxs-lookup"><span data-stu-id="df216-110">MAPI_NON_READ</span></span> 
  
> <span data-ttu-id="df216-111">Nonread のレポートが生成されます。</span><span class="sxs-lookup"><span data-stu-id="df216-111">A nonread report is generated.</span></span> <span data-ttu-id="df216-112">MAPI_NON_READ が設定されていない場合は、リードのレポートが生成されます。</span><span class="sxs-lookup"><span data-stu-id="df216-112">If MAPI_NON_READ is not set, a read report is generated.</span></span>
    
 <span data-ttu-id="df216-113">_lpReadMessage_</span><span class="sxs-lookup"><span data-stu-id="df216-113">_lpReadMessage_</span></span>
  
> <span data-ttu-id="df216-114">[in]レポートを生成するかについては、メッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="df216-114">[in] A pointer to the message about which the report should be generated.</span></span>
    
 <span data-ttu-id="df216-115">_lppEmptyMessage_</span><span class="sxs-lookup"><span data-stu-id="df216-115">_lppEmptyMessage_</span></span>
  
> <span data-ttu-id="df216-116">[で [チェック アウト]入力では、 _lppEmptyMessage_は、空のメッセージへのポインターを指しています。</span><span class="sxs-lookup"><span data-stu-id="df216-116">[in, out] On input,  _lppEmptyMessage_ points to a pointer to an empty message.</span></span> <span data-ttu-id="df216-117">出力では、 _lppEmptyMessage_は、レポート メッセージへのポインターをポイントします。</span><span class="sxs-lookup"><span data-stu-id="df216-117">On output,  _lppEmptyMessage_ points to a pointer to the report message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="df216-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="df216-118">Return value</span></span>

<span data-ttu-id="df216-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="df216-119">S_OK</span></span> 
  
> <span data-ttu-id="df216-120">レポートが正常に生成されました。</span><span class="sxs-lookup"><span data-stu-id="df216-120">The report was successfully generated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="df216-121">注釈</span><span class="sxs-lookup"><span data-stu-id="df216-121">Remarks</span></span>

<span data-ttu-id="df216-122">**IMAPISupport::ReadReceipt**メソッドは、メッセージ ストア プロバイダーのサポートのオブジェクトに対してのみ実装されます。</span><span class="sxs-lookup"><span data-stu-id="df216-122">The **IMAPISupport::ReadReceipt** method is implemented only for message store provider support objects.</span></span> <span data-ttu-id="df216-123">メッセージ ストア プロバイダーは、読み取りまたは_lpReadMessage_パラメーターで指定されたメッセージの nonread のレポートを生成するための MAPI に指示するために**ReadReceipt**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="df216-123">Message store providers call **ReadReceipt** to instruct MAPI to generate a read or nonread report for the message pointed to by the  _lpReadMessage_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="df216-124">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="df216-124">Notes to callers</span></span>

<span data-ttu-id="df216-125">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) プロパティが設定されて、次の条件のいずれかが true の場合は、 **ReadReceipt**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="df216-125">Call **ReadReceipt** when the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set and one of the following conditions is true:</span></span>
  
- <span data-ttu-id="df216-126">メッセージが読み取られています。</span><span class="sxs-lookup"><span data-stu-id="df216-126">The message has been read.</span></span>
    
- <span data-ttu-id="df216-127">メッセージを移動するとします。</span><span class="sxs-lookup"><span data-stu-id="df216-127">The message has been moved.</span></span>
    
- <span data-ttu-id="df216-128">メッセージがコピーされました。</span><span class="sxs-lookup"><span data-stu-id="df216-128">The message has been copied.</span></span>
    
- <span data-ttu-id="df216-129">メッセージの[IMessage::SetReadFlag](imessage-setreadflag.md)メソッドが呼び出されました。</span><span class="sxs-lookup"><span data-stu-id="df216-129">The message's [IMessage::SetReadFlag](imessage-setreadflag.md) method has been called.</span></span> 
    
<span data-ttu-id="df216-130">メッセージが削除されると、 **ReadReceipt**を呼び出さないようにします。</span><span class="sxs-lookup"><span data-stu-id="df216-130">Do not call **ReadReceipt** when a message is deleted.</span></span> 
  
<span data-ttu-id="df216-131">読み取りまたは nonread のレポートは、メッセージの 1 回だけ送信してください。</span><span class="sxs-lookup"><span data-stu-id="df216-131">A read or nonread report should be sent only once for a message.</span></span> <span data-ttu-id="df216-132">メッセージの読み取り状態を追跡し、1 つのメッセージの複数のレポートを送信できません。</span><span class="sxs-lookup"><span data-stu-id="df216-132">Keep track of a message's read status and do not send multiple reports for a single message.</span></span>
  
<span data-ttu-id="df216-133">_LppEmptyMessage_パラメーターは、MAPI は、 **ReadReceipt**から返されるときに、有効なレポートのメッセージをポイントしている場合、メッセージを送信し、その**の IUnknown:s:Release を呼び出すことによって、ポインターを解放する[IMessage::SubmitMessage](imessage-submitmessage.md)メソッドを呼び出す**メソッドです。</span><span class="sxs-lookup"><span data-stu-id="df216-133">If the  _lppEmptyMessage_ parameter points to a valid report message when MAPI returns from **ReadReceipt**, call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send the message and then release the pointer by calling its **IUnknown:s:Release** method.</span></span> 
  
<span data-ttu-id="df216-134">**ReadReceipt**が失敗した場合、送信されることがなくメッセージを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="df216-134">If **ReadReceipt** fails, the message should be released without being submitted.</span></span> <span data-ttu-id="df216-135">メッセージの読み取り状態を保存する場合は後で、読み取りまたは nonread のレポートを生成しようとすることができます。</span><span class="sxs-lookup"><span data-stu-id="df216-135">If you store the message's read status, you can attempt to generate the read or nonread report at a later time.</span></span> 
  
<span data-ttu-id="df216-136">非表示にするか、フォルダー内のストアによって生成される読み取りおよび nonread のレポートを表示します。</span><span class="sxs-lookup"><span data-stu-id="df216-136">You can either hide or display read and nonread reports generated by stores in your folders.</span></span> <span data-ttu-id="df216-137">隠しフォルダーに読み取りおよび nonread のレポートを格納する、強固なセキュリティを実装できます。</span><span class="sxs-lookup"><span data-stu-id="df216-137">Storing read and nonread reports in hidden folders enables you to implement tighter security.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="df216-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="df216-138">See also</span></span>



[<span data-ttu-id="df216-139">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="df216-139">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
  
[<span data-ttu-id="df216-140">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="df216-140">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="df216-141">PidTagReadReceiptRequested 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="df216-141">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)
  
[<span data-ttu-id="df216-142">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="df216-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

