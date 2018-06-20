---
title: IMAPISupportDoProgressDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoProgressDialog
api_type:
- COM
ms.assetid: 74c52b96-e903-444b-8bda-73a08f278c22
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 527a7bb3201a4a6b1bc0807136bc88b80c189de2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800752"
---
# <a name="imapisupportdoprogressdialog"></a><span data-ttu-id="09648-103">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="09648-103">IMAPISupport::DoProgressDialog</span></span>

  
  
<span data-ttu-id="09648-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="09648-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="09648-105">進行状況インジケーターを表示する進行中のオブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="09648-105">Retrieves a progress object that displays a progress indicator.</span></span>
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a><span data-ttu-id="09648-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="09648-106">Parameters</span></span>

 <span data-ttu-id="09648-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="09648-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="09648-108">[in]進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="09648-108">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="09648-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="09648-109">_ulFlags_</span></span>
  
> <span data-ttu-id="09648-110">[in]オブジェクトの進行状況が進行状況を計算する方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="09648-110">[in] A bitmask of flags that controls how the progress object should calculate progress.</span></span> <span data-ttu-id="09648-111">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="09648-111">The following flag can be set:</span></span>
    
<span data-ttu-id="09648-112">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="09648-112">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="09648-113">親フォルダーなどのトップレベルの項目の進行状況が計算されます。</span><span class="sxs-lookup"><span data-stu-id="09648-113">Progress is calculated for a top-level item, such as a parent folder.</span></span> <span data-ttu-id="09648-114">進行中のオブジェクトは、 [IMAPIProgress::Progress](imapiprogress-progress.md)メソッドの_ulCount_および_ulTotal_パラメーターの値を使用する必要があります-現在の項目と、操作でアイテムの合計をそれぞれ指定する: 進行状況をインクリメントするのには操作のインジケーターです。</span><span class="sxs-lookup"><span data-stu-id="09648-114">The progress object should use the values in the [IMAPIProgress::Progress](imapiprogress-progress.md) method's  _ulCount_ and  _ulTotal_ parameters — which indicate the current item and the total items in the operation, respectively — to increment the progress indicator for the operation.</span></span> 
    
 <span data-ttu-id="09648-115">_lppProgress_</span><span class="sxs-lookup"><span data-stu-id="09648-115">_lppProgress_</span></span>
  
> <span data-ttu-id="09648-116">[out]進行中のオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="09648-116">[out] A pointer to a pointer to the progress object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="09648-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="09648-117">Return value</span></span>

<span data-ttu-id="09648-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="09648-118">S_OK</span></span> 
  
> <span data-ttu-id="09648-119">進行中のオブジェクトが正常に取得しました。</span><span class="sxs-lookup"><span data-stu-id="09648-119">The progress object was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="09648-120">備考</span><span class="sxs-lookup"><span data-stu-id="09648-120">Remarks</span></span>

<span data-ttu-id="09648-121">アドレス帳、メッセージ ストア プロバイダーのサポート オブジェクトの**IMAPISupport::DoProgressDialog**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="09648-121">The **IMAPISupport::DoProgressDialog** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="09648-122">これらのプロバイダーは、MAPI インターフェイスの実装、 [IMAPIProgress](imapiprogressiunknown.md) 、進捗状況の情報を計算し、標準のダイアログ ボックスを表示するにアクセスするために**DoProgressDialog**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="09648-122">These providers call **DoProgressDialog** to access the MAPI implementation of the [IMAPIProgress](imapiprogressiunknown.md) interface, which calculates the progress information and displays a standard dialog box.</span></span> 
  
<span data-ttu-id="09648-123">進行中のオブジェクトと、 **IMAPIProgress**インターフェイスを使用する方法の詳細については、[進行状況のインジケーターの表示](how-to-display-a-progress-indicator.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="09648-123">For information about how to use a progress object and the **IMAPIProgress** interface, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="09648-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="09648-124">See also</span></span>



[<span data-ttu-id="09648-125">IMAPIProgress: IUnknown</span><span class="sxs-lookup"><span data-stu-id="09648-125">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="09648-126">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="09648-126">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="09648-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="09648-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="09648-128">進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="09648-128">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)

