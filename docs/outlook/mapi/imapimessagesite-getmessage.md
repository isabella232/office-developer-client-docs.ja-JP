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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3612c12a503174484d4a469ffa167922a015ed5b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576611"
---
# <a name="imapimessagesitegetmessage"></a><span data-ttu-id="3b388-103">IMAPIMessageSite::GetMessage</span><span class="sxs-lookup"><span data-stu-id="3b388-103">IMAPIMessageSite::GetMessage</span></span>

  
  
<span data-ttu-id="3b388-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b388-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b388-105">現在のメッセージを返します。</span><span class="sxs-lookup"><span data-stu-id="3b388-105">Returns the current message.</span></span>
  
```cpp
HRESULT GetMessage(
  LPMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a><span data-ttu-id="3b388-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3b388-106">Parameters</span></span>

 <span data-ttu-id="3b388-107">_ppmsg_</span><span class="sxs-lookup"><span data-stu-id="3b388-107">_ppmsg_</span></span>
  
> <span data-ttu-id="3b388-108">[out]メッセージの返されるインターフェイスへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="3b388-108">[out] A pointer to a pointer to the returned interface for the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3b388-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="3b388-109">Return value</span></span>

<span data-ttu-id="3b388-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="3b388-110">S_OK</span></span> 
  
> <span data-ttu-id="3b388-111">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="3b388-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="3b388-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="3b388-112">S_FALSE</span></span> 
  
> <span data-ttu-id="3b388-113">メッセージ現在存在しない呼び出し元のフォームにします。</span><span class="sxs-lookup"><span data-stu-id="3b388-113">No message currently exists for the calling form.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3b388-114">注釈</span><span class="sxs-lookup"><span data-stu-id="3b388-114">Remarks</span></span>

<span data-ttu-id="3b388-115">フォームでは、現在のメッセージのメッセージのインターフェイスを取得する**IMAPIMessageSite::GetMessage**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3b388-115">Forms call the **IMAPIMessageSite::GetMessage** method to obtain a message interface for the current message.</span></span> <span data-ttu-id="3b388-116">現在のメッセージは、 [IPersistMessage::InitNew](ipersistmessage-initnew.md)、 [IPersistMessage::Load](ipersistmessage-load.md)、または[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)メソッドに渡されたものでは以前と同じメッセージ。</span><span class="sxs-lookup"><span data-stu-id="3b388-116">The current message is the same message as was previously passed in the [IPersistMessage::InitNew](ipersistmessage-initnew.md), [IPersistMessage::Load](ipersistmessage-load.md), or [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method.</span></span> 
  
 <span data-ttu-id="3b388-117">メッセージ現在存在しない場合は、**自動インクリメント**は S_FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="3b388-117">**GetMessage** returns S_FALSE if no message currently exists.</span></span> <span data-ttu-id="3b388-118">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)メソッド、または**IPersistMessage::Load**の次の呼び出しの前に、の呼び出しの後に発生することがこの状態や、 **IPersistMessage::SaveCompleted**が行われます。</span><span class="sxs-lookup"><span data-stu-id="3b388-118">This state can occur after calls to the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method or before the next call to **IPersistMessage::Load** or **IPersistMessage::SaveCompleted** is made.</span></span> 
  
<span data-ttu-id="3b388-119">フォームのサーバーに関連するインターフェイスの一覧は、 [MAPI フォームのインタ フェース](mapi-form-interfaces.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3b388-119">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3b388-120">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="3b388-120">MFCMAPI reference</span></span>

<span data-ttu-id="3b388-121">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="3b388-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3b388-122">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="3b388-122">**File**</span></span>|<span data-ttu-id="3b388-123">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="3b388-123">**Function**</span></span>|<span data-ttu-id="3b388-124">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="3b388-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3b388-125">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="3b388-125">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="3b388-126">CMyMAPIFormViewer::GetSession</span><span class="sxs-lookup"><span data-stu-id="3b388-126">CMyMAPIFormViewer::GetSession</span></span>  <br/> |<span data-ttu-id="3b388-127">MFCMAPI メソッドを使用して、 **IMAPIMessageSite::GetMessage** 、現在キャッシュされているメッセージ ポインターを返すことがある場合。</span><span class="sxs-lookup"><span data-stu-id="3b388-127">MFCMAPI uses the **IMAPIMessageSite::GetMessage** method to return the currently cached message pointer, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3b388-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="3b388-128">See also</span></span>



[<span data-ttu-id="3b388-129">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="3b388-129">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="3b388-130">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="3b388-130">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md)
  
[<span data-ttu-id="3b388-131">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3b388-131">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="3b388-132">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="3b388-132">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="3b388-133">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="3b388-133">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="3b388-134">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3b388-134">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


<span data-ttu-id="3b388-135">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="3b388-135">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="3b388-136">MAPI フォーム インターフェイス</span><span class="sxs-lookup"><span data-stu-id="3b388-136">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

