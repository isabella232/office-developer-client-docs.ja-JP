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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e66315042f8b5cd5aff0e4aa076588c9f312376a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406172"
---
# <a name="imapiviewadvisesinkonprint"></a><span data-ttu-id="9c8fa-103">IMAPIViewAdviseSink::OnPrint</span><span class="sxs-lookup"><span data-stu-id="9c8fa-103">IMAPIViewAdviseSink::OnPrint</span></span>

  
  
<span data-ttu-id="9c8fa-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c8fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c8fa-105">フォームの印刷状態をフォームビューアーに通知します。</span><span class="sxs-lookup"><span data-stu-id="9c8fa-105">Notifies the form viewer of the printing status of a form.</span></span>
  
```cpp
HRESULT OnPrint(
ULONG dwPageNumber,
HRESULT hrStatus
);
```

## <a name="parameters"></a><span data-ttu-id="9c8fa-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9c8fa-106">Parameters</span></span>

 <span data-ttu-id="9c8fa-107">_dwpagenumber_</span><span class="sxs-lookup"><span data-stu-id="9c8fa-107">_dwPageNumber_</span></span>
  
> <span data-ttu-id="9c8fa-108">順番印刷された最後のページの番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="9c8fa-108">[in] Number of the last page printed.</span></span>
    
 <span data-ttu-id="9c8fa-109">_hrstatus_</span><span class="sxs-lookup"><span data-stu-id="9c8fa-109">_hrStatus_</span></span>
  
> <span data-ttu-id="9c8fa-110">順番印刷ジョブの状態を示す HRESULT 値。</span><span class="sxs-lookup"><span data-stu-id="9c8fa-110">[in] An HRESULT value indicating the status of the print job.</span></span> <span data-ttu-id="9c8fa-111">使用可能な値は次のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="9c8fa-111">Possible values are:</span></span>
    
<span data-ttu-id="9c8fa-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="9c8fa-112">S_FALSE</span></span> 
  
> <span data-ttu-id="9c8fa-113">印刷ジョブが正常に終了しました。</span><span class="sxs-lookup"><span data-stu-id="9c8fa-113">The printing job has finished successfully.</span></span>
    
<span data-ttu-id="9c8fa-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="9c8fa-114">S_OK</span></span> 
  
> <span data-ttu-id="9c8fa-115">印刷ジョブが進行中です。</span><span class="sxs-lookup"><span data-stu-id="9c8fa-115">The printing job is in progress.</span></span>
    
<span data-ttu-id="9c8fa-116">フェール</span><span class="sxs-lookup"><span data-stu-id="9c8fa-116">FAILED</span></span> 
  
> <span data-ttu-id="9c8fa-117">印刷ジョブは失敗したため、終了しました。</span><span class="sxs-lookup"><span data-stu-id="9c8fa-117">The printing job was terminated due to a failure.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9c8fa-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="9c8fa-118">Return value</span></span>

<span data-ttu-id="9c8fa-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="9c8fa-119">S_OK</span></span> 
  
> <span data-ttu-id="9c8fa-120">通知に成功しました。</span><span class="sxs-lookup"><span data-stu-id="9c8fa-120">The notification succeeded.</span></span>
    
<span data-ttu-id="9c8fa-121">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="9c8fa-121">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="9c8fa-122">ユーザーが操作をキャンセルしました。通常は、ダイアログボックスの [キャンセル] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9c8fa-122">The user canceled the operation, typically by clicking the Cancel button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9c8fa-123">注釈</span><span class="sxs-lookup"><span data-stu-id="9c8fa-123">Remarks</span></span>

<span data-ttu-id="9c8fa-124">フォームオブジェクトは印刷中に**IMAPIViewAdviseSink:: OnPrint**メソッドを呼び出して、印刷の進行状況を表示します。</span><span class="sxs-lookup"><span data-stu-id="9c8fa-124">Form objects call the **IMAPIViewAdviseSink::OnPrint** method while printing to inform the viewer of printing progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9c8fa-125">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="9c8fa-125">Notes to callers</span></span>

<span data-ttu-id="9c8fa-126">印刷ジョブに複数のページが含まれている場合は、各ページが印刷された後に、 **OnPrint**を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="9c8fa-126">If the printing job involves multiple pages, you can call **OnPrint** after each page is printed.</span></span> <span data-ttu-id="9c8fa-127">現在__ 印刷中のページと_hrstatus_を S_OK に設定します。</span><span class="sxs-lookup"><span data-stu-id="9c8fa-127">Set  _dwPageNumber_ to the page currently being printed and  _hrStatus_ to S_OK.</span></span> <span data-ttu-id="9c8fa-128">印刷ジョブが完了すると、 _dwpagenumber_を使用して**OnPrint**を呼び出し、最後のページが印刷され、 _hrstatus_が S_FALSE に設定されます。</span><span class="sxs-lookup"><span data-stu-id="9c8fa-128">When the printing job is complete, call **OnPrint** with  _dwPageNumber_ set to the last page printed and  _hrStatus_ set to S_FALSE.</span></span> 
  
<span data-ttu-id="9c8fa-129">フォーム通知の詳細については、「[フォーム通知の送信と受信](sending-and-receiving-form-notifications.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9c8fa-129">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9c8fa-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="9c8fa-130">See also</span></span>



[<span data-ttu-id="9c8fa-131">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9c8fa-131">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

