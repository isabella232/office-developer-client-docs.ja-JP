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
ms.openlocfilehash: 5e56fd8c053ff32bdeb7b243701c0330b378cdc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800800"
---
# <a name="imapisupportreadreceipt"></a><span data-ttu-id="a0e2c-103">IMAPISupport::ReadReceipt</span><span class="sxs-lookup"><span data-stu-id="a0e2c-103">IMAPISupport::ReadReceipt</span></span>

  
  
<span data-ttu-id="a0e2c-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a0e2c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a0e2c-105">読み取りまたはメッセージの nonread のレポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="a0e2c-105">Generates a read or nonread report for a message.</span></span>
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a><span data-ttu-id="a0e2c-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="a0e2c-106">Parameters</span></span>

 <span data-ttu-id="a0e2c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a0e2c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a0e2c-108">[in]読み取りまたは nonread のレポートの生成方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="a0e2c-108">[in] A bitmask of flags that controls how the read or nonread report is generated.</span></span> <span data-ttu-id="a0e2c-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="a0e2c-109">The following flag can be set:</span></span>
    
<span data-ttu-id="a0e2c-110">MAPI_NON_READ</span><span class="sxs-lookup"><span data-stu-id="a0e2c-110">MAPI_NON_READ</span></span> 
  
> <span data-ttu-id="a0e2c-111">Nonread のレポートが生成されます。</span><span class="sxs-lookup"><span data-stu-id="a0e2c-111">A nonread report is generated.</span></span> <span data-ttu-id="a0e2c-112">MAPI_NON_READ が設定されていない場合は、リードのレポートが生成されます。</span><span class="sxs-lookup"><span data-stu-id="a0e2c-112">If MAPI_NON_READ is not set, a read report is generated.</span></span>
    
 <span data-ttu-id="a0e2c-113">_lpReadMessage_</span><span class="sxs-lookup"><span data-stu-id="a0e2c-113">_lpReadMessage_</span></span>
  
> <span data-ttu-id="a0e2c-114">[in]レポートを生成するかについては、メッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a0e2c-114">[in] A pointer to the message about which the report should be generated.</span></span>
    
 <span data-ttu-id="a0e2c-115">_lppEmptyMessage_</span><span class="sxs-lookup"><span data-stu-id="a0e2c-115">_lppEmptyMessage_</span></span>
  
> <span data-ttu-id="a0e2c-116">[で [チェック アウト]入力では、 _lppEmptyMessage_は、空のメッセージへのポインターを指しています。</span><span class="sxs-lookup"><span data-stu-id="a0e2c-116">[in, out] On input,  _lppEmptyMessage_ points to a pointer to an empty message.</span></span> <span data-ttu-id="a0e2c-117">出力では、 _lppEmptyMessage_は、レポート メッセージへのポインターをポイントします。</span><span class="sxs-lookup"><span data-stu-id="a0e2c-117">On output,  _lppEmptyMessage_ points to a pointer to the report message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a0e2c-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="a0e2c-118">Return value</span></span>

<span data-ttu-id="a0e2c-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="a0e2c-119">S_OK</span></span> 
  
> <span data-ttu-id="a0e2c-120">レポートが正常に生成されました。</span><span class="sxs-lookup"><span data-stu-id="a0e2c-120">The report was successfully generated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a0e2c-121">備考</span><span class="sxs-lookup"><span data-stu-id="a0e2c-121">Remarks</span></span>

<span data-ttu-id="a0e2c-122">**IMAPISupport::ReadReceipt**メソッドは、メッセージ ストア プロバイダーのサポートのオブジェクトに対してのみ実装されます。</span><span class="sxs-lookup"><span data-stu-id="a0e2c-122">The **IMAPISupport::ReadReceipt** method is implemented only for message store provider support objects.</span></span> <span data-ttu-id="a0e2c-123">メッセージ ストア プロバイダーは、読み取りまたは_lpReadMessage_パラメーターで指定されたメッセージの nonread のレポートを生成するための MAPI に指示するために**ReadReceipt**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a0e2c-123">Message store providers call **ReadReceipt** to instruct MAPI to generate a read or nonread report for the message pointed to by the  _lpReadMessage_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a0e2c-124">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="a0e2c-124">Notes to callers</span></span>

<span data-ttu-id="a0e2c-125">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) プロパティが設定されて、次の条件のいずれかが true の場合は、 **ReadReceipt**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a0e2c-125">Call **ReadReceipt** when the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set and one of the following conditions is true:</span></span>
  
- <span data-ttu-id="a0e2c-126">メッセージが読み取られています。</span><span class="sxs-lookup"><span data-stu-id="a0e2c-126">The message has been read.</span></span>
    
- <span data-ttu-id="a0e2c-127">メッセージを移動するとします。</span><span class="sxs-lookup"><span data-stu-id="a0e2c-127">The message has been moved.</span></span>
    
- <span data-ttu-id="a0e2c-128">メッセージがコピーされました。</span><span class="sxs-lookup"><span data-stu-id="a0e2c-128">The message has been copied.</span></span>
    
- <span data-ttu-id="a0e2c-129">メッセージの[IMessage::SetReadFlag](imessage-setreadflag.md)メソッドが呼び出されました。</span><span class="sxs-lookup"><span data-stu-id="a0e2c-129">The message's [IMessage::SetReadFlag](imessage-setreadflag.md) method has been called.</span></span> 
    
<span data-ttu-id="a0e2c-130">メッセージが削除されると、 **ReadReceipt**を呼び出さないようにします。</span><span class="sxs-lookup"><span data-stu-id="a0e2c-130">Do not call **ReadReceipt** when a message is deleted.</span></span> 
  
<span data-ttu-id="a0e2c-131">読み取りまたは nonread のレポートは、メッセージの 1 回だけ送信してください。</span><span class="sxs-lookup"><span data-stu-id="a0e2c-131">A read or nonread report should be sent only once for a message.</span></span> <span data-ttu-id="a0e2c-132">メッセージの読み取り状態を追跡し、1 つのメッセージの複数のレポートを送信できません。</span><span class="sxs-lookup"><span data-stu-id="a0e2c-132">Keep track of a message's read status and do not send multiple reports for a single message.</span></span>
  
<span data-ttu-id="a0e2c-133">_LppEmptyMessage_パラメーターは、MAPI は、 **ReadReceipt**から返されるときに、有効なレポートのメッセージをポイントしている場合、メッセージを送信し、その**の IUnknown:s:Release を呼び出すことによって、ポインターを解放する[IMessage::SubmitMessage](imessage-submitmessage.md)メソッドを呼び出す**メソッドです。</span><span class="sxs-lookup"><span data-stu-id="a0e2c-133">If the  _lppEmptyMessage_ parameter points to a valid report message when MAPI returns from **ReadReceipt**, call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send the message and then release the pointer by calling its **IUnknown:s:Release** method.</span></span> 
  
<span data-ttu-id="a0e2c-134">**ReadReceipt**が失敗した場合、送信されることがなくメッセージを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0e2c-134">If **ReadReceipt** fails, the message should be released without being submitted.</span></span> <span data-ttu-id="a0e2c-135">メッセージの読み取り状態を保存する場合は後で、読み取りまたは nonread のレポートを生成しようとすることができます。</span><span class="sxs-lookup"><span data-stu-id="a0e2c-135">If you store the message's read status, you can attempt to generate the read or nonread report at a later time.</span></span> 
  
<span data-ttu-id="a0e2c-136">非表示にするか、フォルダー内のストアによって生成される読み取りおよび nonread のレポートを表示します。</span><span class="sxs-lookup"><span data-stu-id="a0e2c-136">You can either hide or display read and nonread reports generated by stores in your folders.</span></span> <span data-ttu-id="a0e2c-137">隠しフォルダーに読み取りおよび nonread のレポートを格納する、強固なセキュリティを実装できます。</span><span class="sxs-lookup"><span data-stu-id="a0e2c-137">Storing read and nonread reports in hidden folders enables you to implement tighter security.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a0e2c-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="a0e2c-138">See also</span></span>



[<span data-ttu-id="a0e2c-139">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="a0e2c-139">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
  
[<span data-ttu-id="a0e2c-140">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="a0e2c-140">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="a0e2c-141">PidTagReadReceiptRequested の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="a0e2c-141">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)
  
[<span data-ttu-id="a0e2c-142">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a0e2c-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

