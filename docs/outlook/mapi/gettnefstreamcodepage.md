---
title: GetTnefStreamCodepage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f22ccf2-1004-4731-9d68-f66c01b4588b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1e3d384f35726ff28bb47f3d537c8a7a1dda6dce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299434"
---
# <a name="gettnefstreamcodepage"></a><span data-ttu-id="dfd69-103">GetTnefStreamCodepage</span><span class="sxs-lookup"><span data-stu-id="dfd69-103">GetTnefStreamCodepage</span></span>

  
  
<span data-ttu-id="dfd69-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dfd69-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dfd69-105">カプセル化形式 (TNEF) ストリームTransport-Neutralコード ページを決定します。</span><span class="sxs-lookup"><span data-stu-id="dfd69-105">Determines the code page for a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dfd69-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="dfd69-106">Header file:</span></span>  <br/> |<span data-ttu-id="dfd69-107">tnef.h</span><span class="sxs-lookup"><span data-stu-id="dfd69-107">tnef.h</span></span>  <br/> |
|<span data-ttu-id="dfd69-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="dfd69-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dfd69-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dfd69-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dfd69-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="dfd69-110">Called by:</span></span>  <br/> |<span data-ttu-id="dfd69-111">クライアント アプリケーションとサービス プロバイダー。</span><span class="sxs-lookup"><span data-stu-id="dfd69-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a><span data-ttu-id="dfd69-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="dfd69-112">Parameters</span></span>

 <span data-ttu-id="dfd69-113">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="dfd69-113">_lpStream_</span></span>
  
> <span data-ttu-id="dfd69-114">[in]TNEF ストリーム メッセージのソースを提供するストレージ ストリーム オブジェクト OLE **IStream** インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="dfd69-114">[in] Pointer to a storage stream object OLE **IStream** interface providing a source for a TNEF stream message.</span></span> 
    
 <span data-ttu-id="dfd69-115">_lpulCodepage_</span><span class="sxs-lookup"><span data-stu-id="dfd69-115">_lpulCodepage_</span></span>
  
> <span data-ttu-id="dfd69-116">[out]ストリームのコード ページへのポインター。</span><span class="sxs-lookup"><span data-stu-id="dfd69-116">[out] Pointer to the code page of the stream.</span></span>
    
 <span data-ttu-id="dfd69-117">_lpulSubCodepage_</span><span class="sxs-lookup"><span data-stu-id="dfd69-117">_lpulSubCodepage_</span></span>
  
> <span data-ttu-id="dfd69-118">[out]ストリームのサブコード ページへのポインター。</span><span class="sxs-lookup"><span data-stu-id="dfd69-118">[out] Pointer to the subcode page of the stream.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dfd69-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="dfd69-119">Return value</span></span>

 <span data-ttu-id="dfd69-120">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="dfd69-120">**S_OK**</span></span>
  
> <span data-ttu-id="dfd69-121">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="dfd69-121">The call succeeded and has returned the expected value or values.</span></span>
    
 <span data-ttu-id="dfd69-122">**MAPI_E_NOT_ENOUGH_DISK**</span><span class="sxs-lookup"><span data-stu-id="dfd69-122">**MAPI_E_NOT_ENOUGH_DISK**</span></span>
  
> <span data-ttu-id="dfd69-123">TNEF ストリームで属性を読み取るエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="dfd69-123">There was an error reading an attribute in the TNEF stream.</span></span>
    
 <span data-ttu-id="dfd69-124">**MAPI_E_CORRUPT_DATA**</span><span class="sxs-lookup"><span data-stu-id="dfd69-124">**MAPI_E_CORRUPT_DATA**</span></span>
  
> <span data-ttu-id="dfd69-125">ストリームが TNEF ストリームでなかったか、attOemCodepage 属性の読み取りエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="dfd69-125">Either the stream was not a TNEF stream or there was an error reading the attOemCodepage attribute.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dfd69-126">注釈</span><span class="sxs-lookup"><span data-stu-id="dfd69-126">Remarks</span></span>

<span data-ttu-id="dfd69-127">**GetTnefStreamCodepage** 関数を使用して、TNEF ストリームの **attOemCodepage** 属性を読み取り、コード ページとサブコード ページを決定します。</span><span class="sxs-lookup"><span data-stu-id="dfd69-127">Use the **GetTnefStreamCodepage** function to read the **attOemCodepage** attribute of the TNEF stream to determine the code page and subcode page.</span></span> <span data-ttu-id="dfd69-128">**attOemCodepage** が見つからない場合 **、GetTnefStreamCodepage** は 437 のコード ページと 0 のサブコード ページを返します。</span><span class="sxs-lookup"><span data-stu-id="dfd69-128">If **attOemCodepage** is not found, **GetTnefStreamCodepage** returns a code page of 437 and a subcode page of 0.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dfd69-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="dfd69-129">See also</span></span>



[<span data-ttu-id="dfd69-130">attOemCodepage</span><span class="sxs-lookup"><span data-stu-id="dfd69-130">attOemCodepage</span></span>](https://msdn.microsoft.com/library/ee158667%28EXCHG.80%29.aspx)

