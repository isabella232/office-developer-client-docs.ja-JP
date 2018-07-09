---
title: GetTnefStreamCodepage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f22ccf2-1004-4731-9d68-f66c01b4588b
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c4859fa4f8f55af7913c884e25c96727c063ba79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800165"
---
# <a name="gettnefstreamcodepage"></a><span data-ttu-id="fac14-103">GetTnefStreamCodepage</span><span class="sxs-lookup"><span data-stu-id="fac14-103">GetTnefStreamCodepage</span></span>

  
  
<span data-ttu-id="fac14-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fac14-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fac14-105">トランスポート ニュートラル カプセル化形式 (TNEF) ストリームのコード ページを決定します。</span><span class="sxs-lookup"><span data-stu-id="fac14-105">Determines the code page for a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fac14-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="fac14-106">Header file:</span></span>  <br/> |<span data-ttu-id="fac14-107">tnef.h</span><span class="sxs-lookup"><span data-stu-id="fac14-107">tnef.h</span></span>  <br/> |
|<span data-ttu-id="fac14-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="fac14-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fac14-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fac14-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fac14-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fac14-110">Called by:</span></span>  <br/> |<span data-ttu-id="fac14-111">クライアント アプリケーションとサービス ・ プロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="fac14-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a><span data-ttu-id="fac14-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="fac14-112">Parameters</span></span>

 <span data-ttu-id="fac14-113">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="fac14-113">_lpStream_</span></span>
  
> <span data-ttu-id="fac14-114">[in]TNEF ストリーム メッセージのソースを提供するストレージ ストリーム オブジェクト OLE の**IStream**インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="fac14-114">[in] Pointer to a storage stream object OLE **IStream** interface providing a source for a TNEF stream message.</span></span> 
    
 <span data-ttu-id="fac14-115">_lpulCodepage_</span><span class="sxs-lookup"><span data-stu-id="fac14-115">_lpulCodepage_</span></span>
  
> <span data-ttu-id="fac14-116">[out]ストリームのコード ページへのポインター。</span><span class="sxs-lookup"><span data-stu-id="fac14-116">[out] Pointer to the code page of the stream.</span></span>
    
 <span data-ttu-id="fac14-117">_lpulSubCodepage_</span><span class="sxs-lookup"><span data-stu-id="fac14-117">_lpulSubCodepage_</span></span>
  
> <span data-ttu-id="fac14-118">[out]ストリームのサブコードのページへのポインター。</span><span class="sxs-lookup"><span data-stu-id="fac14-118">[out] Pointer to the subcode page of the stream.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fac14-119">�߂�l</span><span class="sxs-lookup"><span data-stu-id="fac14-119">Return value</span></span>

 <span data-ttu-id="fac14-120">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="fac14-120">**S_OK**</span></span>
  
> <span data-ttu-id="fac14-121">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="fac14-121">The call succeeded and has returned the expected value or values.</span></span>
    
 <span data-ttu-id="fac14-122">**MAPI_E_NOT_ENOUGH_DISK**</span><span class="sxs-lookup"><span data-stu-id="fac14-122">**MAPI_E_NOT_ENOUGH_DISK**</span></span>
  
> <span data-ttu-id="fac14-123">TNEF ストリーム内の属性を読み取り中にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="fac14-123">There was an error reading an attribute in the TNEF stream.</span></span>
    
 <span data-ttu-id="fac14-124">**MAPI_E_CORRUPT_DATA**</span><span class="sxs-lookup"><span data-stu-id="fac14-124">**MAPI_E_CORRUPT_DATA**</span></span>
  
> <span data-ttu-id="fac14-125">ストリームが TNEF ストリームではないか、attOemCodepage 属性を読み取り中にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="fac14-125">Either the stream was not a TNEF stream or there was an error reading the attOemCodepage attribute.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fac14-126">備考</span><span class="sxs-lookup"><span data-stu-id="fac14-126">Remarks</span></span>

<span data-ttu-id="fac14-127">TNEF ストリームのコード ページとサブコードのページを決定するのにの**attOemCodepage**属性を読み取ることには、 **GetTnefStreamCodepage**関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="fac14-127">Use the **GetTnefStreamCodepage** function to read the **attOemCodepage** attribute of the TNEF stream to determine the code page and subcode page.</span></span> <span data-ttu-id="fac14-128">**AttOemCodepage**が見つからない場合、 **GetTnefStreamCodepage**は、コード ページ 437 と 0 のサブコードのページを返します。</span><span class="sxs-lookup"><span data-stu-id="fac14-128">If **attOemCodepage** is not found, **GetTnefStreamCodepage** returns a code page of 437 and a subcode page of 0.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fac14-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="fac14-129">See also</span></span>



[<span data-ttu-id="fac14-130">attOemCodepage</span><span class="sxs-lookup"><span data-stu-id="fac14-130">attOemCodepage</span></span>](http://msdn.microsoft.com/ja-jp/library/ee158667%28EXCHG.80%29.aspx)

