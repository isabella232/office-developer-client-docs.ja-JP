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
ms.openlocfilehash: 694ee8b12b9918502e60c0c6ea92992cc1062945
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800606"
---
# <a name="imapimessagesitesubmitmessage"></a><span data-ttu-id="ac6b0-103">IMAPIMessageSite::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="ac6b0-103">IMAPIMessageSite::SubmitMessage</span></span>

  
  
<span data-ttu-id="ac6b0-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ac6b0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ac6b0-105">現在のメッセージが配信のキューに置かれることを要求します。</span><span class="sxs-lookup"><span data-stu-id="ac6b0-105">Requests that the current message be queued for delivery.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="ac6b0-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="ac6b0-106">Parameters</span></span>

 <span data-ttu-id="ac6b0-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ac6b0-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ac6b0-108">[in]メッセージの送信方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="ac6b0-108">[in] A bitmask of flags that controls how a message is submitted.</span></span> <span data-ttu-id="ac6b0-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="ac6b0-109">The following flag can be set:</span></span>
    
<span data-ttu-id="ac6b0-110">FORCE_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="ac6b0-110">FORCE_SUBMIT</span></span> 
  
> <span data-ttu-id="ac6b0-111">MAPI は、場合でも、すぐに送信されない可能性があります、そのメッセージを送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ac6b0-111">MAPI should submit the message even if it might not be sent immediately.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ac6b0-112">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ac6b0-112">Return value</span></span>

<span data-ttu-id="ac6b0-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac6b0-113">S_OK</span></span> 
  
> <span data-ttu-id="ac6b0-114">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="ac6b0-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ac6b0-115">����</span><span class="sxs-lookup"><span data-stu-id="ac6b0-115">Remarks</span></span>

<span data-ttu-id="ac6b0-116">フォーム オブジェクトは、メッセージが配信のキューに置かれることを要求する**IMAPIMessageSite::SubmitMessage**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ac6b0-116">Form objects call the **IMAPIMessageSite::SubmitMessage** method to request that a message be queued for delivery.</span></span> <span data-ttu-id="ac6b0-117">メッセージのサイトでは、メッセージを送信する前に、 [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ac6b0-117">The message site should call the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method before submitting the message.</span></span> <span data-ttu-id="ac6b0-118">メッセージは、メッセージが変更されている場合に保存するメッセージが発生する必要があります**SubmitMessage の**ために既に保存されている必要はありません。</span><span class="sxs-lookup"><span data-stu-id="ac6b0-118">The message does not need to have been previously saved, because **SubmitMessage** should cause the message to be saved if the message has been modified.</span></span> <span data-ttu-id="ac6b0-119">**SubmitMessage**の戻り値は後、フォームは現在のメッセージを確認し、存在しない場合はそれ自体を終了してください。</span><span class="sxs-lookup"><span data-stu-id="ac6b0-119">After the return of **SubmitMessage**, the form must check for a current message and then dismiss itself if none exists.</span></span> 
  
<span data-ttu-id="ac6b0-120">フォームのサーバーに関連するインターフェイスの一覧は、 [MAPI フォームのインタ フェース](mapi-form-interfaces.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ac6b0-120">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ac6b0-121">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="ac6b0-121">MFCMAPI reference</span></span>

<span data-ttu-id="ac6b0-122">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="ac6b0-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ac6b0-123">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="ac6b0-123">**File**</span></span>|<span data-ttu-id="ac6b0-124">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="ac6b0-124">**Function**</span></span>|<span data-ttu-id="ac6b0-125">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="ac6b0-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ac6b0-126">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="ac6b0-126">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="ac6b0-127">CMyMAPIFormViewer::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="ac6b0-127">CMyMAPIFormViewer::SubmitMessage</span></span>  <br/> |<span data-ttu-id="ac6b0-128">MFCMAPI では、 **IMAPIMessageSite::SubmitMessage**メソッドを使用してメッセージを保存します。</span><span class="sxs-lookup"><span data-stu-id="ac6b0-128">MFCMAPI uses the **IMAPIMessageSite::SubmitMessage** method to save the message.</span></span> <span data-ttu-id="ac6b0-129">最初に、 **IPersistMessage::HandsOffMessage**メソッドを呼び出すことと、 **SubmitMessage**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ac6b0-129">First, it calls the **IPersistMessage::HandsOffMessage** method, and then it calls **SubmitMessage**.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ac6b0-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="ac6b0-130">See also</span></span>



[<span data-ttu-id="ac6b0-131">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="ac6b0-131">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="ac6b0-132">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ac6b0-132">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


<span data-ttu-id="ac6b0-133">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="ac6b0-133">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="ac6b0-134">MAPI フォーム インターフェイス</span><span class="sxs-lookup"><span data-stu-id="ac6b0-134">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

