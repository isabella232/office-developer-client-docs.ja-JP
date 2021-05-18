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
# <a name="imapiviewadvisesinkonprint"></a><span data-ttu-id="475b1-103">IMAPIViewAdviseSink::OnPrint</span><span class="sxs-lookup"><span data-stu-id="475b1-103">IMAPIViewAdviseSink::OnPrint</span></span>

  
  
<span data-ttu-id="475b1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="475b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="475b1-105">フォームの印刷状態をフォーム ビューアーに通知します。</span><span class="sxs-lookup"><span data-stu-id="475b1-105">Notifies the form viewer of the printing status of a form.</span></span>
  
```cpp
HRESULT OnPrint(
ULONG dwPageNumber,
HRESULT hrStatus
);
```

## <a name="parameters"></a><span data-ttu-id="475b1-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="475b1-106">Parameters</span></span>

 <span data-ttu-id="475b1-107">_dwPageNumber_</span><span class="sxs-lookup"><span data-stu-id="475b1-107">_dwPageNumber_</span></span>
  
> <span data-ttu-id="475b1-108">[in]印刷された最後のページの番号。</span><span class="sxs-lookup"><span data-stu-id="475b1-108">[in] Number of the last page printed.</span></span>
    
 <span data-ttu-id="475b1-109">_hrStatus_</span><span class="sxs-lookup"><span data-stu-id="475b1-109">_hrStatus_</span></span>
  
> <span data-ttu-id="475b1-110">[in]印刷ジョブの状態を示す HRESULT 値。</span><span class="sxs-lookup"><span data-stu-id="475b1-110">[in] An HRESULT value indicating the status of the print job.</span></span> <span data-ttu-id="475b1-111">使用可能な値は次のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="475b1-111">Possible values are:</span></span>
    
<span data-ttu-id="475b1-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="475b1-112">S_FALSE</span></span> 
  
> <span data-ttu-id="475b1-113">印刷ジョブが正常に終了しました。</span><span class="sxs-lookup"><span data-stu-id="475b1-113">The printing job has finished successfully.</span></span>
    
<span data-ttu-id="475b1-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="475b1-114">S_OK</span></span> 
  
> <span data-ttu-id="475b1-115">印刷ジョブが進行中です。</span><span class="sxs-lookup"><span data-stu-id="475b1-115">The printing job is in progress.</span></span>
    
<span data-ttu-id="475b1-116">FAILED</span><span class="sxs-lookup"><span data-stu-id="475b1-116">FAILED</span></span> 
  
> <span data-ttu-id="475b1-117">エラーが原因で印刷ジョブが終了しました。</span><span class="sxs-lookup"><span data-stu-id="475b1-117">The printing job was terminated due to a failure.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="475b1-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="475b1-118">Return value</span></span>

<span data-ttu-id="475b1-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="475b1-119">S_OK</span></span> 
  
> <span data-ttu-id="475b1-120">通知が成功しました。</span><span class="sxs-lookup"><span data-stu-id="475b1-120">The notification succeeded.</span></span>
    
<span data-ttu-id="475b1-121">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="475b1-121">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="475b1-122">通常、ユーザーはダイアログ ボックスの [キャンセル] ボタンをクリックして操作をキャンセルしました。</span><span class="sxs-lookup"><span data-stu-id="475b1-122">The user canceled the operation, typically by clicking the Cancel button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="475b1-123">注釈</span><span class="sxs-lookup"><span data-stu-id="475b1-123">Remarks</span></span>

<span data-ttu-id="475b1-124">フォーム オブジェクトは **、印刷中に IMAPIViewAdviseSink::OnPrint** メソッドを呼び出して、印刷の進行状況をビューアーに通知します。</span><span class="sxs-lookup"><span data-stu-id="475b1-124">Form objects call the **IMAPIViewAdviseSink::OnPrint** method while printing to inform the viewer of printing progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="475b1-125">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="475b1-125">Notes to callers</span></span>

<span data-ttu-id="475b1-126">印刷ジョブに複数のページが含まれる場合は、各ページの印刷後に **OnPrint** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="475b1-126">If the printing job involves multiple pages, you can call **OnPrint** after each page is printed.</span></span> <span data-ttu-id="475b1-127">_dwPageNumber を_ 現在印刷中のページに設定し _、hrStatus_ を [S_OK.</span><span class="sxs-lookup"><span data-stu-id="475b1-127">Set  _dwPageNumber_ to the page currently being printed and  _hrStatus_ to S_OK.</span></span> <span data-ttu-id="475b1-128">印刷ジョブが完了したら、印刷された最後のページに _dwPageNumber_ が設定された **OnPrint** を呼び出し _、hrStatus_ を [印刷] にS_FALSE。</span><span class="sxs-lookup"><span data-stu-id="475b1-128">When the printing job is complete, call **OnPrint** with  _dwPageNumber_ set to the last page printed and  _hrStatus_ set to S_FALSE.</span></span> 
  
<span data-ttu-id="475b1-129">フォーム通知の詳細については、「フォーム通知の送受信 [」を参照してください](sending-and-receiving-form-notifications.md)。</span><span class="sxs-lookup"><span data-stu-id="475b1-129">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="475b1-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="475b1-130">See also</span></span>



[<span data-ttu-id="475b1-131">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="475b1-131">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

