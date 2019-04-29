---
title: imapisupportreadreceipt
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1915004847fdfd27c97656223866aaab9d3e59c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425324"
---
# <a name="imapisupportreadreceipt"></a><span data-ttu-id="af465-103">IMAPISupport::ReadReceipt</span><span class="sxs-lookup"><span data-stu-id="af465-103">IMAPISupport::ReadReceipt</span></span>

  
  
<span data-ttu-id="af465-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af465-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af465-105">メッセージの読み取りまたは非開封レポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="af465-105">Generates a read or nonread report for a message.</span></span>
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a><span data-ttu-id="af465-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="af465-106">Parameters</span></span>

 <span data-ttu-id="af465-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="af465-107">_ulFlags_</span></span>
  
> <span data-ttu-id="af465-108">順番読み取りまたは非開封レポートの生成方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="af465-108">[in] A bitmask of flags that controls how the read or nonread report is generated.</span></span> <span data-ttu-id="af465-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="af465-109">The following flag can be set:</span></span>
    
<span data-ttu-id="af465-110">MAPI_NON_READ</span><span class="sxs-lookup"><span data-stu-id="af465-110">MAPI_NON_READ</span></span> 
  
> <span data-ttu-id="af465-111">非開封レポートが生成されます。</span><span class="sxs-lookup"><span data-stu-id="af465-111">A nonread report is generated.</span></span> <span data-ttu-id="af465-112">MAPI_NON_READ が設定されていない場合は、読み取りレポートが生成されます。</span><span class="sxs-lookup"><span data-stu-id="af465-112">If MAPI_NON_READ is not set, a read report is generated.</span></span>
    
 <span data-ttu-id="af465-113">_lpReadMessage_</span><span class="sxs-lookup"><span data-stu-id="af465-113">_lpReadMessage_</span></span>
  
> <span data-ttu-id="af465-114">順番レポートを生成するメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="af465-114">[in] A pointer to the message about which the report should be generated.</span></span>
    
 <span data-ttu-id="af465-115">_lppemptymessage_</span><span class="sxs-lookup"><span data-stu-id="af465-115">_lppEmptyMessage_</span></span>
  
> <span data-ttu-id="af465-116">[入力]入力時に、 _lppemptymessage_は空のメッセージへのポインターを指します。</span><span class="sxs-lookup"><span data-stu-id="af465-116">[in, out] On input,  _lppEmptyMessage_ points to a pointer to an empty message.</span></span> <span data-ttu-id="af465-117">出力では、 _lppemptymessage_はレポートメッセージへのポインターを指します。</span><span class="sxs-lookup"><span data-stu-id="af465-117">On output,  _lppEmptyMessage_ points to a pointer to the report message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="af465-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="af465-118">Return value</span></span>

<span data-ttu-id="af465-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="af465-119">S_OK</span></span> 
  
> <span data-ttu-id="af465-120">レポートが正常に生成されました。</span><span class="sxs-lookup"><span data-stu-id="af465-120">The report was successfully generated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="af465-121">注釈</span><span class="sxs-lookup"><span data-stu-id="af465-121">Remarks</span></span>

<span data-ttu-id="af465-122">**imapisupport:: readreceipt**メソッドは、メッセージストアプロバイダーサポートオブジェクトに対してのみ実装されます。</span><span class="sxs-lookup"><span data-stu-id="af465-122">The **IMAPISupport::ReadReceipt** method is implemented only for message store provider support objects.</span></span> <span data-ttu-id="af465-123">メッセージストアプロバイダーは、 **readreceipt**を呼び出して、MAPI に、 _lpReadMessage_パラメーターによって示されるメッセージの読み取りレポートまたは非開封レポートを生成するように指示します。</span><span class="sxs-lookup"><span data-stu-id="af465-123">Message store providers call **ReadReceipt** to instruct MAPI to generate a read or nonread report for the message pointed to by the  _lpReadMessage_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="af465-124">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="af465-124">Notes to callers</span></span>

<span data-ttu-id="af465-125">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) プロパティが設定されていて、次のいずれかの条件に該当する場合は、 **readreceipt**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="af465-125">Call **ReadReceipt** when the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set and one of the following conditions is true:</span></span>
  
- <span data-ttu-id="af465-126">メッセージが開封されました。</span><span class="sxs-lookup"><span data-stu-id="af465-126">The message has been read.</span></span>
    
- <span data-ttu-id="af465-127">メッセージが移動されました。</span><span class="sxs-lookup"><span data-stu-id="af465-127">The message has been moved.</span></span>
    
- <span data-ttu-id="af465-128">メッセージがコピーされました。</span><span class="sxs-lookup"><span data-stu-id="af465-128">The message has been copied.</span></span>
    
- <span data-ttu-id="af465-129">メッセージの[IMessage:: setreadflag](imessage-setreadflag.md)メソッドが呼び出されました。</span><span class="sxs-lookup"><span data-stu-id="af465-129">The message's [IMessage::SetReadFlag](imessage-setreadflag.md) method has been called.</span></span> 
    
<span data-ttu-id="af465-130">メッセージが削除されたときに、 **readreceipt**を呼び出しません。</span><span class="sxs-lookup"><span data-stu-id="af465-130">Do not call **ReadReceipt** when a message is deleted.</span></span> 
  
<span data-ttu-id="af465-131">読み取りまたは非開封レポートは、メッセージに対して1回だけ送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="af465-131">A read or nonread report should be sent only once for a message.</span></span> <span data-ttu-id="af465-132">メッセージの開封状態を追跡し、1つのメッセージに対して複数のレポートを送信しません。</span><span class="sxs-lookup"><span data-stu-id="af465-132">Keep track of a message's read status and do not send multiple reports for a single message.</span></span>
  
<span data-ttu-id="af465-133">MAPI が**readreceipt**から返されたときに、 _lppemptymessage_パラメーターが有効なレポートメッセージを指している場合は、 [IMessage:: submitmessage](imessage-submitmessage.md)メソッドを呼び出してメッセージを送信し、 **IUnknown: s: release を呼び出してポインターを解放します。** メソッド。</span><span class="sxs-lookup"><span data-stu-id="af465-133">If the  _lppEmptyMessage_ parameter points to a valid report message when MAPI returns from **ReadReceipt**, call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send the message and then release the pointer by calling its **IUnknown:s:Release** method.</span></span> 
  
<span data-ttu-id="af465-134">**readreceipt**が失敗した場合、メッセージは送信されずに解放される必要があります。</span><span class="sxs-lookup"><span data-stu-id="af465-134">If **ReadReceipt** fails, the message should be released without being submitted.</span></span> <span data-ttu-id="af465-135">メッセージの開封状態を格納する場合は、後で読み取りまたは非開封レポートを生成することができます。</span><span class="sxs-lookup"><span data-stu-id="af465-135">If you store the message's read status, you can attempt to generate the read or nonread report at a later time.</span></span> 
  
<span data-ttu-id="af465-136">フォルダー内のストアによって生成される読み取りおよび非開封レポートを表示または非表示にすることができます。</span><span class="sxs-lookup"><span data-stu-id="af465-136">You can either hide or display read and nonread reports generated by stores in your folders.</span></span> <span data-ttu-id="af465-137">読み取りおよび非開封レポートを隠しフォルダーに格納することで、より厳密なセキュリティを実装できます。</span><span class="sxs-lookup"><span data-stu-id="af465-137">Storing read and nonread reports in hidden folders enables you to implement tighter security.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="af465-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="af465-138">See also</span></span>



[<span data-ttu-id="af465-139">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="af465-139">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
  
[<span data-ttu-id="af465-140">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="af465-140">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="af465-141">PidTagReadReceiptRequested 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="af465-141">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)
  
[<span data-ttu-id="af465-142">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="af465-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

