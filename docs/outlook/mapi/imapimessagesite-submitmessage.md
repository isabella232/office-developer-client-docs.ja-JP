---
title: IMAPIMessageSiteSubmitMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.SubmitMessage
api_type:
- COM
ms.assetid: 6b14c383-8bc6-4e86-bd92-0500272af40d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 496732e334d2d39672048dd1a02346aaee4b70e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321407"
---
# <a name="imapimessagesitesubmitmessage"></a><span data-ttu-id="8881f-103">IMAPIMessageSite::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="8881f-103">IMAPIMessageSite::SubmitMessage</span></span>

  
  
<span data-ttu-id="8881f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8881f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8881f-105">現在のメッセージが配信のためにキューに入れられるように要求します。</span><span class="sxs-lookup"><span data-stu-id="8881f-105">Requests that the current message be queued for delivery.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="8881f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8881f-106">Parameters</span></span>

 <span data-ttu-id="8881f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8881f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8881f-108">順番メッセージの送信方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="8881f-108">[in] A bitmask of flags that controls how a message is submitted.</span></span> <span data-ttu-id="8881f-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="8881f-109">The following flag can be set:</span></span>
    
<span data-ttu-id="8881f-110">FORCE_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="8881f-110">FORCE_SUBMIT</span></span> 
  
> <span data-ttu-id="8881f-111">MAPI は、メッセージがすぐに送信されない可能性がある場合でも、メッセージを送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8881f-111">MAPI should submit the message even if it might not be sent immediately.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8881f-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="8881f-112">Return value</span></span>

<span data-ttu-id="8881f-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="8881f-113">S_OK</span></span> 
  
> <span data-ttu-id="8881f-114">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="8881f-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8881f-115">解説</span><span class="sxs-lookup"><span data-stu-id="8881f-115">Remarks</span></span>

<span data-ttu-id="8881f-116">Form オブジェクトは**IMAPIMessageSite:: submitmessage**メソッドを呼び出して、メッセージが配信のためにキューに入れられるよう要求します。</span><span class="sxs-lookup"><span data-stu-id="8881f-116">Form objects call the **IMAPIMessageSite::SubmitMessage** method to request that a message be queued for delivery.</span></span> <span data-ttu-id="8881f-117">メッセージサイトは、メッセージを送信する前に、 [IPersistMessage::](ipersistmessage-handsoffmessage.md)配布用のメッセージメソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="8881f-117">The message site should call the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method before submitting the message.</span></span> <span data-ttu-id="8881f-118">メッセージが変更された場合、 **submitmessage**によってメッセージが保存されるため、メッセージを以前に保存しておく必要はありません。</span><span class="sxs-lookup"><span data-stu-id="8881f-118">The message does not need to have been previously saved, because **SubmitMessage** should cause the message to be saved if the message has been modified.</span></span> <span data-ttu-id="8881f-119">**submitmessage**を戻すと、フォームは現在のメッセージを確認し、存在しない場合は自分自身を破棄する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8881f-119">After the return of **SubmitMessage**, the form must check for a current message and then dismiss itself if none exists.</span></span> 
  
<span data-ttu-id="8881f-120">フォームサーバーに関連するインターフェイスの一覧については、「 [MAPI フォームインターフェイス](mapi-form-interfaces.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8881f-120">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8881f-121">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="8881f-121">MFCMAPI reference</span></span>

<span data-ttu-id="8881f-122">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8881f-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8881f-123">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="8881f-123">**File**</span></span>|<span data-ttu-id="8881f-124">**関数**</span><span class="sxs-lookup"><span data-stu-id="8881f-124">**Function**</span></span>|<span data-ttu-id="8881f-125">**コメント**</span><span class="sxs-lookup"><span data-stu-id="8881f-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8881f-126">MyMAPIFormViewer</span><span class="sxs-lookup"><span data-stu-id="8881f-126">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="8881f-127">cmymapiformviewer:: submitmessage</span><span class="sxs-lookup"><span data-stu-id="8881f-127">CMyMAPIFormViewer::SubmitMessage</span></span>  <br/> |<span data-ttu-id="8881f-128">mfcmapi は、 **IMAPIMessageSite:: submitmessage**メソッドを使用して、メッセージを保存します。</span><span class="sxs-lookup"><span data-stu-id="8881f-128">MFCMAPI uses the **IMAPIMessageSite::SubmitMessage** method to save the message.</span></span> <span data-ttu-id="8881f-129">最初に、 **IPersistMessage:: handsoffmessage**メソッドを呼び出して、 **submitmessage**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8881f-129">First, it calls the **IPersistMessage::HandsOffMessage** method, and then it calls **SubmitMessage**.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8881f-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="8881f-130">See also</span></span>



[<span data-ttu-id="8881f-131">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="8881f-131">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="8881f-132">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8881f-132">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


<span data-ttu-id="8881f-133">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="8881f-133">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="8881f-134">MAPI フォームインターフェイス</span><span class="sxs-lookup"><span data-stu-id="8881f-134">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

