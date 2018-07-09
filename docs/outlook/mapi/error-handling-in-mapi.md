---
title: MAPI でのエラー処理
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99e2c485-af84-46f4-84b4-fca2117b5a21
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 6f0ebd2112b65140a106a1376896f6de9c00da1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800013"
---
# <a name="error-handling-in-mapi"></a><span data-ttu-id="c0d0e-103">MAPI でのエラー処理</span><span class="sxs-lookup"><span data-stu-id="c0d0e-103">Error handling in MAPI</span></span>

<span data-ttu-id="c0d0e-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c0d0e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c0d0e-105">ハンドル、または HRESULT を結果として呼ばれる 32 ビットの数値を使用して成功、警告、エラー値が返されます。</span><span class="sxs-lookup"><span data-stu-id="c0d0e-105">Success, warning, and error values are returned using a 32-bit number known as a result handle, or HRESULT.</span></span> <span data-ttu-id="c0d0e-106">HRESULT は本当に何もへのハンドル値のエンコードされたいくつかのフィールドを持つ 32 ビット値だけですることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c0d0e-106">An HRESULT is really not a handle to anything; it is merely a 32-bit value with several fields encoded in the value.</span></span> <span data-ttu-id="c0d0e-107">ゼロという結果は成功を示し、0 以外の結果は失敗を示します。</span><span class="sxs-lookup"><span data-stu-id="c0d0e-107">A zero result indicates success and a nonzero result indicates failure.</span></span>
  
<span data-ttu-id="c0d0e-108">MAPI 32 ビットのプラットフォームでは、HRESULT の値でのみ動作します。</span><span class="sxs-lookup"><span data-stu-id="c0d0e-108">MAPI on 32-bit platforms works solely with HRESULT values.</span></span>
  
<span data-ttu-id="c0d0e-109">次の図では、32 ビット プラットフォーム用の HRESULT の形式を示します。</span><span class="sxs-lookup"><span data-stu-id="c0d0e-109">The following illustration shows the HRESULT format for 32-bit platforms.</span></span>
  
<span data-ttu-id="c0d0e-110">**HRESULT の形式**</span><span class="sxs-lookup"><span data-stu-id="c0d0e-110">**HRESULT format**</span></span>
  
<span data-ttu-id="c0d0e-111">![HRESULT の形式](media/amapi_49.gif "HRESULT の形式")</span><span class="sxs-lookup"><span data-stu-id="c0d0e-111">![HRESULT format](media/amapi_49.gif "HRESULT format")</span></span>
  
<span data-ttu-id="c0d0e-112">HRESULT の最上位ビットは、戻り値が成功または失敗を表すかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="c0d0e-112">The high order bit in the HRESULT indicates whether the return value represents success or failure.</span></span> <span data-ttu-id="c0d0e-113">かどうかは 0 に設定すると、値成功を示します。</span><span class="sxs-lookup"><span data-stu-id="c0d0e-113">If set to zero, the value indicates success.</span></span> <span data-ttu-id="c0d0e-114">1 に設定すると、その障害を示しています。</span><span class="sxs-lookup"><span data-stu-id="c0d0e-114">If set to 1, it indicates failure.</span></span>
  
<span data-ttu-id="c0d0e-115">HRESULT には、R、C、N、r ビットが予約されています。</span><span class="sxs-lookup"><span data-stu-id="c0d0e-115">The R, C, N, and r bits are reserved in the HRESULT.</span></span>
  
<span data-ttu-id="c0d0e-116">両方のバージョンの機能のフィールドでは、エラーの責任の範囲を示します。</span><span class="sxs-lookup"><span data-stu-id="c0d0e-116">The facility field in both versions indicates the area of responsibility for the error.</span></span> <span data-ttu-id="c0d0e-117">いくつかの機能がありますが、MAPI エラーの大部分では、FACILITY_ITF を使用して、インターフェイスのエラーを表します。</span><span class="sxs-lookup"><span data-stu-id="c0d0e-117">There are several facilities, but the vast majority of MAPI errors use FACILITY_ITF to represent interface errors.</span></span> <span data-ttu-id="c0d0e-118">現在使用されている最も一般的な機能: FACILITY_NULL、FACILITY_ITF、FACILITY_DISPATCH、FACILITY_RPC、および FACILITY_STORAGE。</span><span class="sxs-lookup"><span data-stu-id="c0d0e-118">The most common facilities that are currently used are: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC, and FACILITY_STORAGE.</span></span> <span data-ttu-id="c0d0e-119">新しい設備が必要な場合は、Microsoft ライセンスを割り当てますは一意である必要があるためです。</span><span class="sxs-lookup"><span data-stu-id="c0d0e-119">If new facilities are necessary, Microsoft allocates them because they need to be unique.</span></span> <span data-ttu-id="c0d0e-120">次の表では、さまざまな機能のフィールドについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c0d0e-120">The following table describes the various facility fields.</span></span>
  
|<span data-ttu-id="c0d0e-121">施設</span><span class="sxs-lookup"><span data-stu-id="c0d0e-121">Facility</span></span>|<span data-ttu-id="c0d0e-122">説明</span><span class="sxs-lookup"><span data-stu-id="c0d0e-122">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="c0d0e-123">FACILITY_NULL</span><span class="sxs-lookup"><span data-stu-id="c0d0e-123">FACILITY_NULL</span></span>  <br/> |<span data-ttu-id="c0d0e-124">広範に適用される一般的なステータス コード S_OK、または E_OUTOF_MEMORY です。値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="c0d0e-124">For broadly applicable common status codes such as S_OK or E_OUTOF_MEMORY; the value is zero.</span></span>  <br/> |
|<span data-ttu-id="c0d0e-125">FACILITY_ITF</span><span class="sxs-lookup"><span data-stu-id="c0d0e-125">FACILITY_ITF</span></span>  <br/> |<span data-ttu-id="c0d0e-126">インターフェイス メソッドから返されたステータス コードのほとんどの値は、インターフェイスによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="c0d0e-126">For most status codes returned from interface methods; the value is defined by the interface.</span></span> <span data-ttu-id="c0d0e-127">正確に 32 ビット値が同じ 2 つの異なるインターフェイスから返される 2 つの HRESULT 値は、異なる意味を持つ可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c0d0e-127">That is, two HRESULT values with exactly the same 32-bit value returned from two different interfaces might have different meanings.</span></span>  <br/> |
|<span data-ttu-id="c0d0e-128">FACILITY_DISPATCH</span><span class="sxs-lookup"><span data-stu-id="c0d0e-128">FACILITY_DISPATCH</span></span>  <br/> |<span data-ttu-id="c0d0e-129">[IDispatch](http://msdn.microsoft.com/ja-jp/library/ms221608.aspx)を遅延バインディングのインターフェイスのエラーを実行します。</span><span class="sxs-lookup"><span data-stu-id="c0d0e-129">For late binding [IDispatch](http://msdn.microsoft.com/ja-jp/library/ms221608.aspx) interface errors.</span></span>  <br/> |
|<span data-ttu-id="c0d0e-130">FACILITY_RPC</span><span class="sxs-lookup"><span data-stu-id="c0d0e-130">FACILITY_RPC</span></span>  <br/> |<span data-ttu-id="c0d0e-131">リモート ・ プロシージャ ・ コールから返されるステータス ・ コードです。</span><span class="sxs-lookup"><span data-stu-id="c0d0e-131">For status codes returned from remote procedure calls.</span></span>  <br/> |
|<span data-ttu-id="c0d0e-132">FACILITY_STORAGE</span><span class="sxs-lookup"><span data-stu-id="c0d0e-132">FACILITY_STORAGE</span></span>  <br/> |<span data-ttu-id="c0d0e-133">構造化ストレージに関連する[IStorage](http://msdn.microsoft.com/ja-jp/library/aa380015%28VS.85%29.aspx)または[IStream](http://msdn.microsoft.com/ja-jp/library/aa380034%28VS.85%29.aspx)のメソッド呼び出しから返されるステータス ・ コードです。</span><span class="sxs-lookup"><span data-stu-id="c0d0e-133">For status codes returned from [IStorage](http://msdn.microsoft.com/ja-jp/library/aa380015%28VS.85%29.aspx) or [IStream](http://msdn.microsoft.com/ja-jp/library/aa380034%28VS.85%29.aspx) method calls relating to structured storage.</span></span> <span data-ttu-id="c0d0e-134">コード (下位 16 ビット) 値が範囲の Windows のエラー コードでステータス コード (つまり、256 文字未満) 対応する Windows のエラーと同じ意味を持ちます。</span><span class="sxs-lookup"><span data-stu-id="c0d0e-134">Status codes with code (lower 16 bits) values in the range of Windows error codes (that is, less than 256) have the same meaning as the corresponding Windows errors.</span></span>  <br/> |
   
<span data-ttu-id="c0d0e-135">[コード] フィールドは、エラーまたは警告を表すために割り当てられている一意の番号です。</span><span class="sxs-lookup"><span data-stu-id="c0d0e-135">The code field is a unique number that is assigned to represent the error or warning.</span></span>
  

