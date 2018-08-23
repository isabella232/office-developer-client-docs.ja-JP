---
title: IMAPIViewContextSetAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.SetAdviseSink
api_type:
- COM
ms.assetid: 4799084a-b5d1-48c3-a889-b2f0e9d68c30
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 555bb4820dc36934fb28197b7e222633a5248125
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583184"
---
# <a name="imapiviewcontextsetadvisesink"></a><span data-ttu-id="1e760-103">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="1e760-103">IMAPIViewContext::SetAdviseSink</span></span>

  
  
<span data-ttu-id="1e760-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e760-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e760-105">ビューアーの変更についての通知を受信するフォームの登録を管理します。</span><span class="sxs-lookup"><span data-stu-id="1e760-105">Manages a form's registration to receive notifications about changes in the viewer.</span></span> 
  
```cpp
HRESULT SetAdviseSink(
LPMAPIFORMADVISESINK pmvns
);
```

## <a name="parameters"></a><span data-ttu-id="1e760-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1e760-106">Parameters</span></span>

 <span data-ttu-id="1e760-107">_pmvns_</span><span class="sxs-lookup"><span data-stu-id="1e760-107">_pmvns_</span></span>
  
> <span data-ttu-id="1e760-108">[in]フォームへのポインターでは、シンク オブジェクトまたは NULL を案内します。</span><span class="sxs-lookup"><span data-stu-id="1e760-108">[in] Pointer to a form advise sink object or NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1e760-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="1e760-109">Return value</span></span>

<span data-ttu-id="1e760-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="1e760-110">S_OK</span></span> 
  
> <span data-ttu-id="1e760-111">登録またはフォームの通知の取り消しに成功しました。</span><span class="sxs-lookup"><span data-stu-id="1e760-111">The registration or cancellation for form notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1e760-112">注釈</span><span class="sxs-lookup"><span data-stu-id="1e760-112">Remarks</span></span>

<span data-ttu-id="1e760-113">フォーム オブジェクトは、いずれかの登録フォーム ビューアーでの変更点について説明する前の登録をキャンセルする**IMAPIViewContext::SetAdviseSink**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1e760-113">Form objects call the **IMAPIViewContext::SetAdviseSink** method to either register to learn about changes in the form viewer or cancel a prior registration.</span></span> <span data-ttu-id="1e760-114">_Pmvns_を NULL に設定すると、フォームは、登録をキャンセルしようとします。</span><span class="sxs-lookup"><span data-stu-id="1e760-114">When  _pmvns_ is set to NULL, the form wants to cancel a registration.</span></span> <span data-ttu-id="1e760-115">有効なフォームに_pmvns_ポイントは、シンクをアドバイス、フォームの今後の通知を登録しようとします。</span><span class="sxs-lookup"><span data-stu-id="1e760-115">When  _pmvns_ points to a valid form advise sink, the form wants to register for future notifications.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1e760-116">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="1e760-116">Notes to implementers</span></span>

<span data-ttu-id="1e760-117">**SetAdviseSink**にフォームが含まれていますとシンク ポインターの通知、通知をキャンセルするのには別の**SetAdviseSink**呼び出しが行われるまでは、オブジェクトへの参照を保持します。</span><span class="sxs-lookup"><span data-stu-id="1e760-117">When **SetAdviseSink** includes a form advise sink pointer, keep a reference to it until another **SetAdviseSink** call is made to cancel notification.</span></span> <span data-ttu-id="1e760-118">ビューアーで、新しいメッセージをロードするときに変更が発生したときに通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="1e760-118">Send a notification when a change occurs in your viewer and when you are loading a new message.</span></span> 
  
<span data-ttu-id="1e760-119">詳細については、[送信およびフォームの通知の受信](sending-and-receiving-form-notifications.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1e760-119">For more information, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1e760-120">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="1e760-120">MFCMAPI reference</span></span>

<span data-ttu-id="1e760-121">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="1e760-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1e760-122">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="1e760-122">**File**</span></span>|<span data-ttu-id="1e760-123">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="1e760-123">**Function**</span></span>|<span data-ttu-id="1e760-124">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="1e760-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1e760-125">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="1e760-125">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="1e760-126">CMyMAPIFormViewer::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="1e760-126">CMyMAPIFormViewer::SetAdviseSink</span></span>  <br/> |<span data-ttu-id="1e760-127">MFCMAPI では、この関数では、 **IMAPIViewContext::SetAdviseSink**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="1e760-127">MFCMAPI implements the **IMAPIViewContext::SetAdviseSink** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1e760-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="1e760-128">See also</span></span>



<span data-ttu-id="1e760-129">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="1e760-129">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

