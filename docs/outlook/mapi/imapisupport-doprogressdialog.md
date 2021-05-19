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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3de29e9af5caa82d2e57c8fcbbdab7d5ddb19dd9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432584"
---
# <a name="imapisupportdoprogressdialog"></a><span data-ttu-id="17d38-103">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="17d38-103">IMAPISupport::DoProgressDialog</span></span>

  
  
<span data-ttu-id="17d38-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17d38-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17d38-105">進行状況インジケーターを表示する進行状況オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="17d38-105">Retrieves a progress object that displays a progress indicator.</span></span>
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a><span data-ttu-id="17d38-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="17d38-106">Parameters</span></span>

 <span data-ttu-id="17d38-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="17d38-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="17d38-108">[in]進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="17d38-108">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="17d38-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="17d38-109">_ulFlags_</span></span>
  
> <span data-ttu-id="17d38-110">[in]進行状況オブジェクトが進行状況を計算する方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="17d38-110">[in] A bitmask of flags that controls how the progress object should calculate progress.</span></span> <span data-ttu-id="17d38-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="17d38-111">The following flag can be set:</span></span>
    
<span data-ttu-id="17d38-112">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="17d38-112">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="17d38-113">進行状況は、親フォルダーなどの上位レベルのアイテムに対して計算されます。</span><span class="sxs-lookup"><span data-stu-id="17d38-113">Progress is calculated for a top-level item, such as a parent folder.</span></span> <span data-ttu-id="17d38-114">progress オブジェクトは、操作の進行状況インジケーターをインクリメントするために [、IMAPIProgress::P rogress](imapiprogress-progress.md) メソッドの  _ulCount_ パラメーターと  _ulTotal_ パラメーターの値を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17d38-114">The progress object should use the values in the [IMAPIProgress::Progress](imapiprogress-progress.md) method's  _ulCount_ and  _ulTotal_ parameters — which indicate the current item and the total items in the operation, respectively — to increment the progress indicator for the operation.</span></span> 
    
 <span data-ttu-id="17d38-115">_lppProgress_</span><span class="sxs-lookup"><span data-stu-id="17d38-115">_lppProgress_</span></span>
  
> <span data-ttu-id="17d38-116">[out]progress オブジェクトへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="17d38-116">[out] A pointer to a pointer to the progress object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="17d38-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="17d38-117">Return value</span></span>

<span data-ttu-id="17d38-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="17d38-118">S_OK</span></span> 
  
> <span data-ttu-id="17d38-119">progress オブジェクトが正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="17d38-119">The progress object was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="17d38-120">注釈</span><span class="sxs-lookup"><span data-stu-id="17d38-120">Remarks</span></span>

<span data-ttu-id="17d38-121">**IMAPISupport::D oProgressDialog** メソッドは、アドレス帳およびメッセージ ストア プロバイダーのサポート オブジェクトに実装されます。</span><span class="sxs-lookup"><span data-stu-id="17d38-121">The **IMAPISupport::DoProgressDialog** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="17d38-122">これらのプロバイダーは **DoProgressDialog** を呼び出して [IMAPIProgress](imapiprogressiunknown.md) インターフェイスの MAPI 実装にアクセスし、進行状況情報を計算し、標準のダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="17d38-122">These providers call **DoProgressDialog** to access the MAPI implementation of the [IMAPIProgress](imapiprogressiunknown.md) interface, which calculates the progress information and displays a standard dialog box.</span></span> 
  
<span data-ttu-id="17d38-123">進行状況オブジェクトと **IMAPIProgress** インターフェイスを使用する方法については、「進捗インジケーターを表示 [する」を参照してください](how-to-display-a-progress-indicator.md)。</span><span class="sxs-lookup"><span data-stu-id="17d38-123">For information about how to use a progress object and the **IMAPIProgress** interface, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="17d38-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="17d38-124">See also</span></span>



[<span data-ttu-id="17d38-125">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="17d38-125">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="17d38-126">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="17d38-126">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="17d38-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="17d38-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="17d38-128">進行状況インジケーターを表示する</span><span class="sxs-lookup"><span data-stu-id="17d38-128">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)

