---
title: imapisupportdo進捗ダイアログ
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
# <a name="imapisupportdoprogressdialog"></a><span data-ttu-id="bdb35-103">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="bdb35-103">IMAPISupport::DoProgressDialog</span></span>

  
  
<span data-ttu-id="bdb35-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bdb35-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bdb35-105">進行状況インジケーターを表示する progress オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="bdb35-105">Retrieves a progress object that displays a progress indicator.</span></span>
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a><span data-ttu-id="bdb35-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bdb35-106">Parameters</span></span>

 <span data-ttu-id="bdb35-107">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="bdb35-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="bdb35-108">順番進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="bdb35-108">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="bdb35-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bdb35-109">_ulFlags_</span></span>
  
> <span data-ttu-id="bdb35-110">順番進捗状況オブジェクトが進捗状況を計算する方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="bdb35-110">[in] A bitmask of flags that controls how the progress object should calculate progress.</span></span> <span data-ttu-id="bdb35-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="bdb35-111">The following flag can be set:</span></span>
    
<span data-ttu-id="bdb35-112">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="bdb35-112">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="bdb35-113">最上位レベルのアイテム (親フォルダーなど) について、進行状況が計算されます。</span><span class="sxs-lookup"><span data-stu-id="bdb35-113">Progress is calculated for a top-level item, such as a parent folder.</span></span> <span data-ttu-id="bdb35-114">progress オブジェクトは、imapiprogress の値を使用する必要があり[ます。:P rogress](imapiprogress-progress.md)メソッドの_ulcount_および_ulcount_パラメーター (それぞれ、現在のアイテムおよび操作の合計アイテムを示す) を使用して、進行状況を増分します。操作のインジケーター。</span><span class="sxs-lookup"><span data-stu-id="bdb35-114">The progress object should use the values in the [IMAPIProgress::Progress](imapiprogress-progress.md) method's  _ulCount_ and  _ulTotal_ parameters — which indicate the current item and the total items in the operation, respectively — to increment the progress indicator for the operation.</span></span> 
    
 <span data-ttu-id="bdb35-115">_lppprogress_</span><span class="sxs-lookup"><span data-stu-id="bdb35-115">_lppProgress_</span></span>
  
> <span data-ttu-id="bdb35-116">読み上げprogress オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="bdb35-116">[out] A pointer to a pointer to the progress object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bdb35-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="bdb35-117">Return value</span></span>

<span data-ttu-id="bdb35-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="bdb35-118">S_OK</span></span> 
  
> <span data-ttu-id="bdb35-119">progress オブジェクトが正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="bdb35-119">The progress object was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bdb35-120">注釈</span><span class="sxs-lookup"><span data-stu-id="bdb35-120">Remarks</span></span>

<span data-ttu-id="bdb35-121">**imapisupport::D o進捗ダイアログ**メソッドは、アドレス帳とメッセージストアプロバイダーのサポートオブジェクトに実装されています。</span><span class="sxs-lookup"><span data-stu-id="bdb35-121">The **IMAPISupport::DoProgressDialog** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="bdb35-122">これらのプロバイダーは**doprogress ダイアログ**を呼び出して、進行状況の情報を計算し、標準ダイアログボックスを表示する[imapiprogress](imapiprogressiunknown.md)インターフェイスの MAPI 実装にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="bdb35-122">These providers call **DoProgressDialog** to access the MAPI implementation of the [IMAPIProgress](imapiprogressiunknown.md) interface, which calculates the progress information and displays a standard dialog box.</span></span> 
  
<span data-ttu-id="bdb35-123">progress オブジェクトと**imapiprogress**インターフェイスを使用する方法については、「[進行状況インジケーターを表示する](how-to-display-a-progress-indicator.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bdb35-123">For information about how to use a progress object and the **IMAPIProgress** interface, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bdb35-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="bdb35-124">See also</span></span>



[<span data-ttu-id="bdb35-125">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bdb35-125">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="bdb35-126">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="bdb35-126">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="bdb35-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="bdb35-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="bdb35-128">進行状況インジケーターを表示する</span><span class="sxs-lookup"><span data-stu-id="bdb35-128">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)

