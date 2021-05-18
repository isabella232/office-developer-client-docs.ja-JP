---
title: IMAPIMessageSiteGetMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetMessage
api_type:
- COM
ms.assetid: 49d12c49-84f8-44ac-bc4a-2ee44a46f8c1
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 03dd0553d0203585850ac5c4f8c91c86ef60236a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409028"
---
# <a name="imapimessagesitegetmessage"></a><span data-ttu-id="7d877-103">IMAPIMessageSite::GetMessage</span><span class="sxs-lookup"><span data-stu-id="7d877-103">IMAPIMessageSite::GetMessage</span></span>

  
  
<span data-ttu-id="7d877-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d877-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d877-105">現在のメッセージを返します。</span><span class="sxs-lookup"><span data-stu-id="7d877-105">Returns the current message.</span></span>
  
```cpp
HRESULT GetMessage(
  LPMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a><span data-ttu-id="7d877-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7d877-106">Parameters</span></span>

 <span data-ttu-id="7d877-107">_ppmsg_</span><span class="sxs-lookup"><span data-stu-id="7d877-107">_ppmsg_</span></span>
  
> <span data-ttu-id="7d877-108">[out]メッセージの返されるインターフェイスへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="7d877-108">[out] A pointer to a pointer to the returned interface for the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7d877-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="7d877-109">Return value</span></span>

<span data-ttu-id="7d877-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="7d877-110">S_OK</span></span> 
  
> <span data-ttu-id="7d877-111">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="7d877-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="7d877-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="7d877-112">S_FALSE</span></span> 
  
> <span data-ttu-id="7d877-113">呼び出し元のフォームにメッセージが現在存在しません。</span><span class="sxs-lookup"><span data-stu-id="7d877-113">No message currently exists for the calling form.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7d877-114">注釈</span><span class="sxs-lookup"><span data-stu-id="7d877-114">Remarks</span></span>

<span data-ttu-id="7d877-115">フォームは **IMAPIMessageSite::GetMessage** メソッドを呼び出して、現在のメッセージのメッセージ インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="7d877-115">Forms call the **IMAPIMessageSite::GetMessage** method to obtain a message interface for the current message.</span></span> <span data-ttu-id="7d877-116">現在のメッセージは [、IPersistMessage::InitNew](ipersistmessage-initnew.md) [、IPersistMessage::Load、](ipersistmessage-load.md)または [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) メソッドで以前に渡されたメッセージと同じです。</span><span class="sxs-lookup"><span data-stu-id="7d877-116">The current message is the same message as was previously passed in the [IPersistMessage::InitNew](ipersistmessage-initnew.md), [IPersistMessage::Load](ipersistmessage-load.md), or [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method.</span></span> 
  
 <span data-ttu-id="7d877-117">**GetMessage は** 、現在S_FALSEメッセージが存在しない場合、そのメッセージを返します。</span><span class="sxs-lookup"><span data-stu-id="7d877-117">**GetMessage** returns S_FALSE if no message currently exists.</span></span> <span data-ttu-id="7d877-118">この状態は [、IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)メソッドを呼び出した後、または **IPersistMessage::Load または IPersistMessage::SaveCompleted** の次の呼び出しが行われる前に発生する可能性があります。 </span><span class="sxs-lookup"><span data-stu-id="7d877-118">This state can occur after calls to the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method or before the next call to **IPersistMessage::Load** or **IPersistMessage::SaveCompleted** is made.</span></span> 
  
<span data-ttu-id="7d877-119">フォーム サーバーに関連するインターフェイスの一覧については [、「MAPI フォーム インターフェイス」を参照してください](mapi-form-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="7d877-119">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7d877-120">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="7d877-120">MFCMAPI reference</span></span>

<span data-ttu-id="7d877-121">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7d877-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7d877-122">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="7d877-122">**File**</span></span>|<span data-ttu-id="7d877-123">**関数**</span><span class="sxs-lookup"><span data-stu-id="7d877-123">**Function**</span></span>|<span data-ttu-id="7d877-124">**コメント**</span><span class="sxs-lookup"><span data-stu-id="7d877-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7d877-125">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="7d877-125">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="7d877-126">CMyMAPIFormViewer::GetSession</span><span class="sxs-lookup"><span data-stu-id="7d877-126">CMyMAPIFormViewer::GetSession</span></span>  <br/> |<span data-ttu-id="7d877-127">MFCMAPI は **IMAPIMessageSite::GetMessage** メソッドを使用して、現在キャッシュされているメッセージ ポインター (使用可能な場合) を返します。</span><span class="sxs-lookup"><span data-stu-id="7d877-127">MFCMAPI uses the **IMAPIMessageSite::GetMessage** method to return the currently cached message pointer, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7d877-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="7d877-128">See also</span></span>



[<span data-ttu-id="7d877-129">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="7d877-129">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="7d877-130">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="7d877-130">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md)
  
[<span data-ttu-id="7d877-131">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7d877-131">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="7d877-132">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="7d877-132">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="7d877-133">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="7d877-133">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="7d877-134">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7d877-134">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


<span data-ttu-id="7d877-135">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="7d877-135">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="7d877-136">MAPI フォーム インターフェイス</span><span class="sxs-lookup"><span data-stu-id="7d877-136">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

