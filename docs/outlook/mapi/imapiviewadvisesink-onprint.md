---
title: IMAPIViewAdviseSinkOnPrint
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnPrint
api_type:
- COM
ms.assetid: d16219a0-268c-428d-9f02-4f06eb5b6d7d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: bf3eee43a70fbc4abf32b60379fc7b191bd9d513
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800858"
---
# <a name="imapiviewadvisesinkonprint"></a><span data-ttu-id="e814d-103">IMAPIViewAdviseSink::OnPrint</span><span class="sxs-lookup"><span data-stu-id="e814d-103">IMAPIViewAdviseSink::OnPrint</span></span>

  
  
<span data-ttu-id="e814d-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e814d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e814d-105">フォーム ビューアーのフォームの印刷の状態を通知します。</span><span class="sxs-lookup"><span data-stu-id="e814d-105">Notifies the form viewer of the printing status of a form.</span></span>
  
```cpp
HRESULT OnPrint(
ULONG dwPageNumber,
HRESULT hrStatus
);
```

## <a name="parameters"></a><span data-ttu-id="e814d-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e814d-106">Parameters</span></span>

 <span data-ttu-id="e814d-107">_dwPageNumber_</span><span class="sxs-lookup"><span data-stu-id="e814d-107">_dwPageNumber_</span></span>
  
> <span data-ttu-id="e814d-108">[in]最後のページ数が印刷されます。</span><span class="sxs-lookup"><span data-stu-id="e814d-108">[in] Number of the last page printed.</span></span>
    
 <span data-ttu-id="e814d-109">_hrStatus_</span><span class="sxs-lookup"><span data-stu-id="e814d-109">_hrStatus_</span></span>
  
> <span data-ttu-id="e814d-110">[in]印刷ジョブのステータスを示す HRESULT 値です。</span><span class="sxs-lookup"><span data-stu-id="e814d-110">[in] An HRESULT value indicating the status of the print job.</span></span> <span data-ttu-id="e814d-111">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e814d-111">Possible values are:</span></span>
    
<span data-ttu-id="e814d-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="e814d-112">S_FALSE</span></span> 
  
> <span data-ttu-id="e814d-113">印刷ジョブが正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="e814d-113">The printing job has finished successfully.</span></span>
    
<span data-ttu-id="e814d-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="e814d-114">S_OK</span></span> 
  
> <span data-ttu-id="e814d-115">印刷ジョブは処理中です。</span><span class="sxs-lookup"><span data-stu-id="e814d-115">The printing job is in progress.</span></span>
    
<span data-ttu-id="e814d-116">失敗しました。</span><span class="sxs-lookup"><span data-stu-id="e814d-116">FAILED</span></span> 
  
> <span data-ttu-id="e814d-117">印刷ジョブが失敗したため終了しました。</span><span class="sxs-lookup"><span data-stu-id="e814d-117">The printing job was terminated due to a failure.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e814d-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="e814d-118">Return value</span></span>

<span data-ttu-id="e814d-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="e814d-119">S_OK</span></span> 
  
> <span data-ttu-id="e814d-120">通知が成功しました。</span><span class="sxs-lookup"><span data-stu-id="e814d-120">The notification succeeded.</span></span>
    
<span data-ttu-id="e814d-121">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="e814d-121">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="e814d-122">ユーザー操作がキャンセルされました、通常ダイアログ ボックスで [キャンセル] ボタンをクリックするとします。</span><span class="sxs-lookup"><span data-stu-id="e814d-122">The user canceled the operation, typically by clicking the Cancel button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e814d-123">注釈</span><span class="sxs-lookup"><span data-stu-id="e814d-123">Remarks</span></span>

<span data-ttu-id="e814d-124">フォーム オブジェクトは、ビューアーの印刷の進行状況を通知するために印刷中に**IMAPIViewAdviseSink::OnPrint**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e814d-124">Form objects call the **IMAPIViewAdviseSink::OnPrint** method while printing to inform the viewer of printing progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e814d-125">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="e814d-125">Notes to callers</span></span>

<span data-ttu-id="e814d-126">印刷ジョブには、複数のページが含まれている場合は、各ページを印刷した後に**OnPrint**を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="e814d-126">If the printing job involves multiple pages, you can call **OnPrint** after each page is printed.</span></span> <span data-ttu-id="e814d-127">S_OK を現在印刷中のページに_dwPageNumber_と_hrStatus_を設定します。</span><span class="sxs-lookup"><span data-stu-id="e814d-127">Set  _dwPageNumber_ to the page currently being printed and  _hrStatus_ to S_OK.</span></span> <span data-ttu-id="e814d-128">印刷ジョブが完了すると、最後の印刷のページを設定する_dwPageNumber_では、**印刷時**の呼び出しおよび_hrStatus_は S_FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="e814d-128">When the printing job is complete, call **OnPrint** with  _dwPageNumber_ set to the last page printed and  _hrStatus_ set to S_FALSE.</span></span> 
  
<span data-ttu-id="e814d-129">フォームの通知の詳細については、[送信およびフォームの通知の受信](sending-and-receiving-form-notifications.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e814d-129">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e814d-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="e814d-130">See also</span></span>



[<span data-ttu-id="e814d-131">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e814d-131">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

