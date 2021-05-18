---
title: MAPI でのエラー処理
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99e2c485-af84-46f4-84b4-fca2117b5a21
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 98ee0856411cce3a3e9012185be6c30503de7779
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287282"
---
# <a name="error-handling-in-mapi"></a><span data-ttu-id="43745-103">MAPI でのエラー処理</span><span class="sxs-lookup"><span data-stu-id="43745-103">Error handling in MAPI</span></span>

<span data-ttu-id="43745-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43745-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43745-105">成功、警告、およびエラーの値は、結果ハンドルまたは HRESULT と呼ばれる 32 ビットの数値を使用して返されます。</span><span class="sxs-lookup"><span data-stu-id="43745-105">Success, warning, and error values are returned using a 32-bit number known as a result handle, or HRESULT.</span></span> <span data-ttu-id="43745-106">HRESULT は、実際には何も処理しません。単なる 32 ビットの値で、複数のフィールドが値にエンコードされています。</span><span class="sxs-lookup"><span data-stu-id="43745-106">An HRESULT is really not a handle to anything; it is merely a 32-bit value with several fields encoded in the value.</span></span> <span data-ttu-id="43745-107">結果が 0 の場合は成功を示し、0 以外の結果は失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="43745-107">A zero result indicates success and a nonzero result indicates failure.</span></span>
  
<span data-ttu-id="43745-108">32 ビット プラットフォーム上の MAPI は、HRESULT 値でのみ動作します。</span><span class="sxs-lookup"><span data-stu-id="43745-108">MAPI on 32-bit platforms works solely with HRESULT values.</span></span>
  
<span data-ttu-id="43745-109">次の図は、32 ビット プラットフォームの HRESULT 形式を示しています。</span><span class="sxs-lookup"><span data-stu-id="43745-109">The following illustration shows the HRESULT format for 32-bit platforms.</span></span>
  
<span data-ttu-id="43745-110">**HRESULT の書式**</span><span class="sxs-lookup"><span data-stu-id="43745-110">**HRESULT format**</span></span>
  
<span data-ttu-id="43745-111">![HRESULT 形式](media/amapi_49.gif "HRESULT 形式")</span><span class="sxs-lookup"><span data-stu-id="43745-111">![HRESULT format](media/amapi_49.gif "HRESULT format")</span></span>
  
<span data-ttu-id="43745-112">HRESULT の高次ビットは、戻り値が成功または失敗を表すかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="43745-112">The high order bit in the HRESULT indicates whether the return value represents success or failure.</span></span> <span data-ttu-id="43745-113">ゼロに設定すると、値は成功を示します。</span><span class="sxs-lookup"><span data-stu-id="43745-113">If set to zero, the value indicates success.</span></span> <span data-ttu-id="43745-114">1 に設定すると、エラーが示されます。</span><span class="sxs-lookup"><span data-stu-id="43745-114">If set to 1, it indicates failure.</span></span>
  
<span data-ttu-id="43745-115">R、C、N、および r のビットは HRESULT で予約されています。</span><span class="sxs-lookup"><span data-stu-id="43745-115">The R, C, N, and r bits are reserved in the HRESULT.</span></span>
  
<span data-ttu-id="43745-116">両方のバージョンの機能フィールドは、エラーの責任領域を示します。</span><span class="sxs-lookup"><span data-stu-id="43745-116">The facility field in both versions indicates the area of responsibility for the error.</span></span> <span data-ttu-id="43745-117">いくつかの機能がありますが、MAPI エラーの大部分は、インターフェイス エラーを表すFACILITY_ITFを使用します。</span><span class="sxs-lookup"><span data-stu-id="43745-117">There are several facilities, but the vast majority of MAPI errors use FACILITY_ITF to represent interface errors.</span></span> <span data-ttu-id="43745-118">現在使用されている最も一般的な機能は、FACILITY_NULL、FACILITY_ITF、FACILITY_DISPATCH、FACILITY_RPC、FACILITY_STORAGE。</span><span class="sxs-lookup"><span data-stu-id="43745-118">The most common facilities that are currently used are: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC, and FACILITY_STORAGE.</span></span> <span data-ttu-id="43745-119">新しい施設が必要な場合は、一意である必要があるため、Microsoft が割り当てします。</span><span class="sxs-lookup"><span data-stu-id="43745-119">If new facilities are necessary, Microsoft allocates them because they need to be unique.</span></span> <span data-ttu-id="43745-120">次の表では、さまざまな機能フィールドについて説明します。</span><span class="sxs-lookup"><span data-stu-id="43745-120">The following table describes the various facility fields.</span></span>
  
|<span data-ttu-id="43745-121">Facility</span><span class="sxs-lookup"><span data-stu-id="43745-121">Facility</span></span>|<span data-ttu-id="43745-122">説明</span><span class="sxs-lookup"><span data-stu-id="43745-122">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="43745-123">FACILITY_NULL</span><span class="sxs-lookup"><span data-stu-id="43745-123">FACILITY_NULL</span></span>  <br/> |<span data-ttu-id="43745-124">広く適用可能な一般的な状態コード (たとえば、S_OKまたはE_OUTOF_MEMORY。値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="43745-124">For broadly applicable common status codes such as S_OK or E_OUTOF_MEMORY; the value is zero.</span></span>  <br/> |
|<span data-ttu-id="43745-125">FACILITY_ITF</span><span class="sxs-lookup"><span data-stu-id="43745-125">FACILITY_ITF</span></span>  <br/> |<span data-ttu-id="43745-126">インターフェイス メソッドから返されるほとんどの状態コードの場合。値はインターフェイスによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="43745-126">For most status codes returned from interface methods; the value is defined by the interface.</span></span> <span data-ttu-id="43745-127">つまり、2 つの異なるインターフェイスから返される 32 ビット値がまったく同じ 2 つの HRESULT 値は、異なる意味を持つ場合があります。</span><span class="sxs-lookup"><span data-stu-id="43745-127">That is, two HRESULT values with exactly the same 32-bit value returned from two different interfaces might have different meanings.</span></span>  <br/> |
|<span data-ttu-id="43745-128">FACILITY_DISPATCH</span><span class="sxs-lookup"><span data-stu-id="43745-128">FACILITY_DISPATCH</span></span>  <br/> |<span data-ttu-id="43745-129">[IDispatch インターフェイスのエラーの](https://msdn.microsoft.com/library/ms221608.aspx)バインディングが遅い場合。</span><span class="sxs-lookup"><span data-stu-id="43745-129">For late binding [IDispatch](https://msdn.microsoft.com/library/ms221608.aspx) interface errors.</span></span>  <br/> |
|<span data-ttu-id="43745-130">FACILITY_RPC</span><span class="sxs-lookup"><span data-stu-id="43745-130">FACILITY_RPC</span></span>  <br/> |<span data-ttu-id="43745-131">リモート プロシージャ呼び出しから返される状態コードの場合。</span><span class="sxs-lookup"><span data-stu-id="43745-131">For status codes returned from remote procedure calls.</span></span>  <br/> |
|<span data-ttu-id="43745-132">FACILITY_STORAGE</span><span class="sxs-lookup"><span data-stu-id="43745-132">FACILITY_STORAGE</span></span>  <br/> |<span data-ttu-id="43745-133">構造化ストレージに関連する [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) メソッドまたは [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) メソッド呼び出しから返される状態コードの場合。</span><span class="sxs-lookup"><span data-stu-id="43745-133">For status codes returned from [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) or [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) method calls relating to structured storage.</span></span> <span data-ttu-id="43745-134">Windows エラー コードの範囲 (つまり、256 未満) のコード (下位 16 ビット) の値を持つ状態コードは、対応する Windows エラーと同じ意味を持ちます。</span><span class="sxs-lookup"><span data-stu-id="43745-134">Status codes with code (lower 16 bits) values in the range of Windows error codes (that is, less than 256) have the same meaning as the corresponding Windows errors.</span></span>  <br/> |
   
<span data-ttu-id="43745-135">コード フィールドは、エラーまたは警告を表す一意の番号です。</span><span class="sxs-lookup"><span data-stu-id="43745-135">The code field is a unique number that is assigned to represent the error or warning.</span></span>
  

