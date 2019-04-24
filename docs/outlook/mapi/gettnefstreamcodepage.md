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
ms.openlocfilehash: 1e3d384f35726ff28bb47f3d537c8a7a1dda6dce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299434"
---
# <a name="gettnefstreamcodepage"></a><span data-ttu-id="4e30a-103">GetTnefStreamCodepage</span><span class="sxs-lookup"><span data-stu-id="4e30a-103">GetTnefStreamCodepage</span></span>

  
  
<span data-ttu-id="4e30a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e30a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e30a-105">トランスポートに中立的なカプセル化形式 (TNEF) ストリームのコードページを指定します。</span><span class="sxs-lookup"><span data-stu-id="4e30a-105">Determines the code page for a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4e30a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="4e30a-106">Header file:</span></span>  <br/> |<span data-ttu-id="4e30a-107">tnef</span><span class="sxs-lookup"><span data-stu-id="4e30a-107">tnef.h</span></span>  <br/> |
|<span data-ttu-id="4e30a-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="4e30a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4e30a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4e30a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4e30a-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="4e30a-110">Called by:</span></span>  <br/> |<span data-ttu-id="4e30a-111">クライアントアプリケーションとサービスプロバイダー。</span><span class="sxs-lookup"><span data-stu-id="4e30a-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a><span data-ttu-id="4e30a-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4e30a-112">Parameters</span></span>

 <span data-ttu-id="4e30a-113">_lpstream_</span><span class="sxs-lookup"><span data-stu-id="4e30a-113">_lpStream_</span></span>
  
> <span data-ttu-id="4e30a-114">順番TNEF ストリームメッセージのソースを提供する、ストレージストリームオブジェクトの OLE **IStream**インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="4e30a-114">[in] Pointer to a storage stream object OLE **IStream** interface providing a source for a TNEF stream message.</span></span> 
    
 <span data-ttu-id="4e30a-115">_lアウトコードページ_</span><span class="sxs-lookup"><span data-stu-id="4e30a-115">_lpulCodepage_</span></span>
  
> <span data-ttu-id="4e30a-116">読み上げストリームのコードページへのポインター。</span><span class="sxs-lookup"><span data-stu-id="4e30a-116">[out] Pointer to the code page of the stream.</span></span>
    
 <span data-ttu-id="4e30a-117">_lアウト subcodepage_</span><span class="sxs-lookup"><span data-stu-id="4e30a-117">_lpulSubCodepage_</span></span>
  
> <span data-ttu-id="4e30a-118">読み上げストリームのサブコードページへのポインター。</span><span class="sxs-lookup"><span data-stu-id="4e30a-118">[out] Pointer to the subcode page of the stream.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4e30a-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="4e30a-119">Return value</span></span>

 <span data-ttu-id="4e30a-120">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="4e30a-120">**S_OK**</span></span>
  
> <span data-ttu-id="4e30a-121">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="4e30a-121">The call succeeded and has returned the expected value or values.</span></span>
    
 <span data-ttu-id="4e30a-122">**MAPI_E_NOT_ENOUGH_DISK**</span><span class="sxs-lookup"><span data-stu-id="4e30a-122">**MAPI_E_NOT_ENOUGH_DISK**</span></span>
  
> <span data-ttu-id="4e30a-123">TNEF ストリームの属性の読み取り中にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="4e30a-123">There was an error reading an attribute in the TNEF stream.</span></span>
    
 <span data-ttu-id="4e30a-124">**MAPI_E_CORRUPT_DATA**</span><span class="sxs-lookup"><span data-stu-id="4e30a-124">**MAPI_E_CORRUPT_DATA**</span></span>
  
> <span data-ttu-id="4e30a-125">ストリームが TNEF ストリームではなかったか、attoemcodepage 属性の読み取り中にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="4e30a-125">Either the stream was not a TNEF stream or there was an error reading the attOemCodepage attribute.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4e30a-126">解説</span><span class="sxs-lookup"><span data-stu-id="4e30a-126">Remarks</span></span>

<span data-ttu-id="4e30a-127">**GetTnefStreamCodepage**関数を使用して、TNEF ストリームの**attoemcodepage**属性を読み取り、コードページとサブコードページを特定します。</span><span class="sxs-lookup"><span data-stu-id="4e30a-127">Use the **GetTnefStreamCodepage** function to read the **attOemCodepage** attribute of the TNEF stream to determine the code page and subcode page.</span></span> <span data-ttu-id="4e30a-128">**attoemcodepage**が見つからない場合、 **GetTnefStreamCodepage**は437のコードページとサブコードページを0に返します。</span><span class="sxs-lookup"><span data-stu-id="4e30a-128">If **attOemCodepage** is not found, **GetTnefStreamCodepage** returns a code page of 437 and a subcode page of 0.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4e30a-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="4e30a-129">See also</span></span>



[<span data-ttu-id="4e30a-130">attoemcodepage</span><span class="sxs-lookup"><span data-stu-id="4e30a-130">attOemCodepage</span></span>](https://msdn.microsoft.com/library/ee158667%28EXCHG.80%29.aspx)

