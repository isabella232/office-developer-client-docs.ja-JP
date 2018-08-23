---
title: GetTnefStreamCodepage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f22ccf2-1004-4731-9d68-f66c01b4588b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c4859fa4f8f55af7913c884e25c96727c063ba79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800165"
---
# <a name="gettnefstreamcodepage"></a><span data-ttu-id="a1b55-103">GetTnefStreamCodepage</span><span class="sxs-lookup"><span data-stu-id="a1b55-103">GetTnefStreamCodepage</span></span>

  
  
<span data-ttu-id="a1b55-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a1b55-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a1b55-105">トランスポート ニュートラル カプセル化形式 (TNEF) ストリームのコード ページを決定します。</span><span class="sxs-lookup"><span data-stu-id="a1b55-105">Determines the code page for a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a1b55-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a1b55-106">Header file:</span></span>  <br/> |<span data-ttu-id="a1b55-107">tnef.h</span><span class="sxs-lookup"><span data-stu-id="a1b55-107">tnef.h</span></span>  <br/> |
|<span data-ttu-id="a1b55-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="a1b55-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a1b55-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a1b55-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a1b55-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a1b55-110">Called by:</span></span>  <br/> |<span data-ttu-id="a1b55-111">クライアント アプリケーションとサービス ・ プロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="a1b55-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a><span data-ttu-id="a1b55-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a1b55-112">Parameters</span></span>

 <span data-ttu-id="a1b55-113">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="a1b55-113">_lpStream_</span></span>
  
> <span data-ttu-id="a1b55-114">[in]TNEF ストリーム メッセージのソースを提供するストレージ ストリーム オブジェクト OLE の**IStream**インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a1b55-114">[in] Pointer to a storage stream object OLE **IStream** interface providing a source for a TNEF stream message.</span></span> 
    
 <span data-ttu-id="a1b55-115">_lpulCodepage_</span><span class="sxs-lookup"><span data-stu-id="a1b55-115">_lpulCodepage_</span></span>
  
> <span data-ttu-id="a1b55-116">[out]ストリームのコード ページへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a1b55-116">[out] Pointer to the code page of the stream.</span></span>
    
 <span data-ttu-id="a1b55-117">_lpulSubCodepage_</span><span class="sxs-lookup"><span data-stu-id="a1b55-117">_lpulSubCodepage_</span></span>
  
> <span data-ttu-id="a1b55-118">[out]ストリームのサブコードのページへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a1b55-118">[out] Pointer to the subcode page of the stream.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a1b55-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="a1b55-119">Return value</span></span>

 <span data-ttu-id="a1b55-120">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="a1b55-120">**S_OK**</span></span>
  
> <span data-ttu-id="a1b55-121">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="a1b55-121">The call succeeded and has returned the expected value or values.</span></span>
    
 <span data-ttu-id="a1b55-122">**MAPI_E_NOT_ENOUGH_DISK**</span><span class="sxs-lookup"><span data-stu-id="a1b55-122">**MAPI_E_NOT_ENOUGH_DISK**</span></span>
  
> <span data-ttu-id="a1b55-123">TNEF ストリーム内の属性を読み取り中にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a1b55-123">There was an error reading an attribute in the TNEF stream.</span></span>
    
 <span data-ttu-id="a1b55-124">**MAPI_E_CORRUPT_DATA**</span><span class="sxs-lookup"><span data-stu-id="a1b55-124">**MAPI_E_CORRUPT_DATA**</span></span>
  
> <span data-ttu-id="a1b55-125">ストリームが TNEF ストリームではないか、attOemCodepage 属性を読み取り中にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a1b55-125">Either the stream was not a TNEF stream or there was an error reading the attOemCodepage attribute.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a1b55-126">注釈</span><span class="sxs-lookup"><span data-stu-id="a1b55-126">Remarks</span></span>

<span data-ttu-id="a1b55-127">TNEF ストリームのコード ページとサブコードのページを決定するのにの**attOemCodepage**属性を読み取ることには、 **GetTnefStreamCodepage**関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="a1b55-127">Use the **GetTnefStreamCodepage** function to read the **attOemCodepage** attribute of the TNEF stream to determine the code page and subcode page.</span></span> <span data-ttu-id="a1b55-128">**AttOemCodepage**が見つからない場合、 **GetTnefStreamCodepage**は、コード ページ 437 と 0 のサブコードのページを返します。</span><span class="sxs-lookup"><span data-stu-id="a1b55-128">If **attOemCodepage** is not found, **GetTnefStreamCodepage** returns a code page of 437 and a subcode page of 0.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a1b55-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="a1b55-129">See also</span></span>



[<span data-ttu-id="a1b55-130">attOemCodepage</span><span class="sxs-lookup"><span data-stu-id="a1b55-130">attOemCodepage</span></span>](http://msdn.microsoft.com/en-us/library/ee158667%28EXCHG.80%29.aspx)

