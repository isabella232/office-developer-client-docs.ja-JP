---
title: MAPI でのエラー処理
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99e2c485-af84-46f4-84b4-fca2117b5a21
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 98ee0856411cce3a3e9012185be6c30503de7779
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287282"
---
# <a name="error-handling-in-mapi"></a><span data-ttu-id="a1543-103">MAPI でのエラー処理</span><span class="sxs-lookup"><span data-stu-id="a1543-103">Error handling in MAPI</span></span>

<span data-ttu-id="a1543-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1543-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1543-105">成功、警告、およびエラー値は、result handle と呼ばれる32ビットの数値、または HRESULT を使用して返されます。</span><span class="sxs-lookup"><span data-stu-id="a1543-105">Success, warning, and error values are returned using a 32-bit number known as a result handle, or HRESULT.</span></span> <span data-ttu-id="a1543-106">HRESULT は、実際には何もハンドルではありません。値でエンコードされた複数のフィールドを持つ32ビットの値にすぎません。</span><span class="sxs-lookup"><span data-stu-id="a1543-106">An HRESULT is really not a handle to anything; it is merely a 32-bit value with several fields encoded in the value.</span></span> <span data-ttu-id="a1543-107">結果が0の場合は成功を示し、0以外の結果は失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="a1543-107">A zero result indicates success and a nonzero result indicates failure.</span></span>
  
<span data-ttu-id="a1543-108">32ビットプラットフォームでの MAPI は、HRESULT 値に対してのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="a1543-108">MAPI on 32-bit platforms works solely with HRESULT values.</span></span>
  
<span data-ttu-id="a1543-109">次の図は、32ビットプラットフォームの HRESULT 形式を示しています。</span><span class="sxs-lookup"><span data-stu-id="a1543-109">The following illustration shows the HRESULT format for 32-bit platforms.</span></span>
  
<span data-ttu-id="a1543-110">**HRESULT の書式**</span><span class="sxs-lookup"><span data-stu-id="a1543-110">**HRESULT format**</span></span>
  
<span data-ttu-id="a1543-111">![HRESULT 形式](media/amapi_49.gif "HRESULT 形式")</span><span class="sxs-lookup"><span data-stu-id="a1543-111">![HRESULT format](media/amapi_49.gif "HRESULT format")</span></span>
  
<span data-ttu-id="a1543-112">HRESULT の上位ビットは、戻り値が成功または失敗を表しているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="a1543-112">The high order bit in the HRESULT indicates whether the return value represents success or failure.</span></span> <span data-ttu-id="a1543-113">0に設定すると、値は success を示します。</span><span class="sxs-lookup"><span data-stu-id="a1543-113">If set to zero, the value indicates success.</span></span> <span data-ttu-id="a1543-114">1に設定されている場合は、エラーを示します。</span><span class="sxs-lookup"><span data-stu-id="a1543-114">If set to 1, it indicates failure.</span></span>
  
<span data-ttu-id="a1543-115">r、C、N、および r のビットは、HRESULT で予約されています。</span><span class="sxs-lookup"><span data-stu-id="a1543-115">The R, C, N, and r bits are reserved in the HRESULT.</span></span>
  
<span data-ttu-id="a1543-116">両方のバージョンのファシリティフィールドは、エラーが発生する責任の領域を示します。</span><span class="sxs-lookup"><span data-stu-id="a1543-116">The facility field in both versions indicates the area of responsibility for the error.</span></span> <span data-ttu-id="a1543-117">いくつかの機能がありますが、大部分の MAPI エラーは FACILITY_ITF を使用してインターフェイスエラーを表します。</span><span class="sxs-lookup"><span data-stu-id="a1543-117">There are several facilities, but the vast majority of MAPI errors use FACILITY_ITF to represent interface errors.</span></span> <span data-ttu-id="a1543-118">現在使用されている最も一般的なファシリティは、FACILITY_NULL、FACILITY_ITF、FACILITY_DISPATCH、FACILITY_RPC、および FACILITY_STORAGE です。</span><span class="sxs-lookup"><span data-stu-id="a1543-118">The most common facilities that are currently used are: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC, and FACILITY_STORAGE.</span></span> <span data-ttu-id="a1543-119">新しい機能が必要な場合は、一意である必要があるため、Microsoft はそれらを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="a1543-119">If new facilities are necessary, Microsoft allocates them because they need to be unique.</span></span> <span data-ttu-id="a1543-120">次の表では、さまざまな機能フィールドについて説明します。</span><span class="sxs-lookup"><span data-stu-id="a1543-120">The following table describes the various facility fields.</span></span>
  
|<span data-ttu-id="a1543-121">Facility</span><span class="sxs-lookup"><span data-stu-id="a1543-121">Facility</span></span>|<span data-ttu-id="a1543-122">説明</span><span class="sxs-lookup"><span data-stu-id="a1543-122">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="a1543-123">FACILITY_NULL</span><span class="sxs-lookup"><span data-stu-id="a1543-123">FACILITY_NULL</span></span>  <br/> |<span data-ttu-id="a1543-124">S_OK や E_OUTOF_MEMORY などの広範に適用される一般的な状態コードの場合は、値は0です。</span><span class="sxs-lookup"><span data-stu-id="a1543-124">For broadly applicable common status codes such as S_OK or E_OUTOF_MEMORY; the value is zero.</span></span>  <br/> |
|<span data-ttu-id="a1543-125">FACILITY_ITF</span><span class="sxs-lookup"><span data-stu-id="a1543-125">FACILITY_ITF</span></span>  <br/> |<span data-ttu-id="a1543-126">インターフェイスメソッドから返されるほとんどの状態コードについては、値はインターフェイスによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="a1543-126">For most status codes returned from interface methods; the value is defined by the interface.</span></span> <span data-ttu-id="a1543-127">つまり、2つの異なるインターフェイスから返される32ビット値がまったく同じで2つの HRESULT 値は、意味が異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="a1543-127">That is, two HRESULT values with exactly the same 32-bit value returned from two different interfaces might have different meanings.</span></span>  <br/> |
|<span data-ttu-id="a1543-128">FACILITY_DISPATCH</span><span class="sxs-lookup"><span data-stu-id="a1543-128">FACILITY_DISPATCH</span></span>  <br/> |<span data-ttu-id="a1543-129">遅延バインディングの[IDispatch](https://msdn.microsoft.com/library/ms221608.aspx)インターフェイスエラーの場合。</span><span class="sxs-lookup"><span data-stu-id="a1543-129">For late binding [IDispatch](https://msdn.microsoft.com/library/ms221608.aspx) interface errors.</span></span>  <br/> |
|<span data-ttu-id="a1543-130">FACILITY_RPC</span><span class="sxs-lookup"><span data-stu-id="a1543-130">FACILITY_RPC</span></span>  <br/> |<span data-ttu-id="a1543-131">リモートプロシージャコールから返された状態コードの場合。</span><span class="sxs-lookup"><span data-stu-id="a1543-131">For status codes returned from remote procedure calls.</span></span>  <br/> |
|<span data-ttu-id="a1543-132">FACILITY_STORAGE</span><span class="sxs-lookup"><span data-stu-id="a1543-132">FACILITY_STORAGE</span></span>  <br/> |<span data-ttu-id="a1543-133">構造化ストレージに関連する[IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx)または[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)メソッドの呼び出しから返された状態コードの場合。</span><span class="sxs-lookup"><span data-stu-id="a1543-133">For status codes returned from [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) or [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) method calls relating to structured storage.</span></span> <span data-ttu-id="a1543-134">windows エラーコードの範囲内のコードを含む状態コード (下位16ビット) の値 (つまり、256未満) は、対応する windows エラーと同じ意味を持ちます。</span><span class="sxs-lookup"><span data-stu-id="a1543-134">Status codes with code (lower 16 bits) values in the range of Windows error codes (that is, less than 256) have the same meaning as the corresponding Windows errors.</span></span>  <br/> |
   
<span data-ttu-id="a1543-135">[コード] フィールドは、エラーまたは警告を表すために割り当てられた一意の番号です。</span><span class="sxs-lookup"><span data-stu-id="a1543-135">The code field is a unique number that is assigned to represent the error or warning.</span></span>
  

