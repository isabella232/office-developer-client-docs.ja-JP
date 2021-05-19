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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 496732e334d2d39672048dd1a02346aaee4b70e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417029"
---
# <a name="imapimessagesitesubmitmessage"></a><span data-ttu-id="0fd44-103">IMAPIMessageSite::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="0fd44-103">IMAPIMessageSite::SubmitMessage</span></span>

  
  
<span data-ttu-id="0fd44-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0fd44-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0fd44-105">現在のメッセージを配信キューに入れろという要求。</span><span class="sxs-lookup"><span data-stu-id="0fd44-105">Requests that the current message be queued for delivery.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="0fd44-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0fd44-106">Parameters</span></span>

 <span data-ttu-id="0fd44-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0fd44-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0fd44-108">[in]メッセージの送信方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="0fd44-108">[in] A bitmask of flags that controls how a message is submitted.</span></span> <span data-ttu-id="0fd44-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="0fd44-109">The following flag can be set:</span></span>
    
<span data-ttu-id="0fd44-110">FORCE_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="0fd44-110">FORCE_SUBMIT</span></span> 
  
> <span data-ttu-id="0fd44-111">MAPI は、すぐに送信されない可能性がある場合でも、メッセージを送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0fd44-111">MAPI should submit the message even if it might not be sent immediately.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0fd44-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="0fd44-112">Return value</span></span>

<span data-ttu-id="0fd44-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="0fd44-113">S_OK</span></span> 
  
> <span data-ttu-id="0fd44-114">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="0fd44-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0fd44-115">注釈</span><span class="sxs-lookup"><span data-stu-id="0fd44-115">Remarks</span></span>

<span data-ttu-id="0fd44-116">フォーム オブジェクトは **IMAPIMessageSite::SubmitMessage** メソッドを呼び出して、メッセージの配信キューに入れられます。</span><span class="sxs-lookup"><span data-stu-id="0fd44-116">Form objects call the **IMAPIMessageSite::SubmitMessage** method to request that a message be queued for delivery.</span></span> <span data-ttu-id="0fd44-117">メッセージ サイトは、メッセージを送信する前に [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="0fd44-117">The message site should call the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method before submitting the message.</span></span> <span data-ttu-id="0fd44-118">メッセージが変更された場合 **、SubmitMessage** によってメッセージが保存される必要があるため、メッセージを以前に保存する必要はなされません。</span><span class="sxs-lookup"><span data-stu-id="0fd44-118">The message does not need to have been previously saved, because **SubmitMessage** should cause the message to be saved if the message has been modified.</span></span> <span data-ttu-id="0fd44-119">SubmitMessage が返 **された後**、フォームは現在のメッセージをチェックし、存在しない場合は自分自身を閉じなければならない。</span><span class="sxs-lookup"><span data-stu-id="0fd44-119">After the return of **SubmitMessage**, the form must check for a current message and then dismiss itself if none exists.</span></span> 
  
<span data-ttu-id="0fd44-120">フォーム サーバーに関連するインターフェイスの一覧については [、「MAPI フォーム インターフェイス」を参照してください](mapi-form-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="0fd44-120">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0fd44-121">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="0fd44-121">MFCMAPI reference</span></span>

<span data-ttu-id="0fd44-122">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0fd44-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0fd44-123">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="0fd44-123">**File**</span></span>|<span data-ttu-id="0fd44-124">**関数**</span><span class="sxs-lookup"><span data-stu-id="0fd44-124">**Function**</span></span>|<span data-ttu-id="0fd44-125">**コメント**</span><span class="sxs-lookup"><span data-stu-id="0fd44-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0fd44-126">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="0fd44-126">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="0fd44-127">CMyMAPIFormViewer::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="0fd44-127">CMyMAPIFormViewer::SubmitMessage</span></span>  <br/> |<span data-ttu-id="0fd44-128">MFCMAPI は **IMAPIMessageSite::SubmitMessage** メソッドを使用してメッセージを保存します。</span><span class="sxs-lookup"><span data-stu-id="0fd44-128">MFCMAPI uses the **IMAPIMessageSite::SubmitMessage** method to save the message.</span></span> <span data-ttu-id="0fd44-129">まず **、IPersistMessage::HandsOffMessage** メソッドを呼び出し、次に **SubmitMessage を呼び出します**。</span><span class="sxs-lookup"><span data-stu-id="0fd44-129">First, it calls the **IPersistMessage::HandsOffMessage** method, and then it calls **SubmitMessage**.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0fd44-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="0fd44-130">See also</span></span>



[<span data-ttu-id="0fd44-131">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="0fd44-131">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="0fd44-132">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0fd44-132">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


<span data-ttu-id="0fd44-133">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="0fd44-133">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="0fd44-134">MAPI フォーム インターフェイス</span><span class="sxs-lookup"><span data-stu-id="0fd44-134">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

