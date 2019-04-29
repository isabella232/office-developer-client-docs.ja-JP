---
title: MAPI のインターフェイス
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 34a66cf0-b4e0-4fd5-b937-cd157888961d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4f5d6a5d2dbb48a86363896bf14b61ed28118330
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422664"
---
# <a name="mapi-interfaces"></a><span data-ttu-id="dbb5d-103">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="dbb5d-103">MAPI Interfaces</span></span>

  
  
<span data-ttu-id="dbb5d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dbb5d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dbb5d-105">各インターフェイスのドキュメントは、インターフェイスの目的についての簡単な説明と、その後に次の情報を含む表を含む概要セクションで構成されています。</span><span class="sxs-lookup"><span data-stu-id="dbb5d-105">The documentation for each interface consists of an introductory section that includes a brief description of the interface's purpose followed by a table that contains the following information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dbb5d-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="dbb5d-106">Header file:</span></span>  <br/> |<span data-ttu-id="dbb5d-107">インターフェイスが定義されており、ソースコードをコンパイルするときに含める必要があるヘッダーファイル。</span><span class="sxs-lookup"><span data-stu-id="dbb5d-107">The header file where the interface is defined and that must be included when you compile your source code.</span></span>  <br/> |
|<span data-ttu-id="dbb5d-108">公開者:</span><span class="sxs-lookup"><span data-stu-id="dbb5d-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="dbb5d-109">インターフェイスを公開するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="dbb5d-109">The object that exposes the interface.</span></span>  <br/> |
|<span data-ttu-id="dbb5d-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="dbb5d-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="dbb5d-111">インターフェイスの実装を提供するコンポーネントのリスト。</span><span class="sxs-lookup"><span data-stu-id="dbb5d-111">A list of the components that provide an implementation of the interface.</span></span>  <br/> |
|<span data-ttu-id="dbb5d-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="dbb5d-112">Called by:</span></span>  <br/> |<span data-ttu-id="dbb5d-113">通常、インターフェイスのメソッドを呼び出すコンポーネントのリスト。</span><span class="sxs-lookup"><span data-stu-id="dbb5d-113">A list of the components that typically call the methods of the interface.</span></span>  <br/> |
|<span data-ttu-id="dbb5d-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="dbb5d-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="dbb5d-115">インターフェイス識別子の GUID。</span><span class="sxs-lookup"><span data-stu-id="dbb5d-115">The interface identifier GUID.</span></span>  <br/> |
|<span data-ttu-id="dbb5d-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="dbb5d-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="dbb5d-117">インターフェイスを公開するオブジェクトのポインターの種類。</span><span class="sxs-lookup"><span data-stu-id="dbb5d-117">The pointer type for the object that exposes the interface.</span></span>  <br/> |
|<span data-ttu-id="dbb5d-118">トランザクションモデル:</span><span class="sxs-lookup"><span data-stu-id="dbb5d-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="dbb5d-119">[imapiprop](imapipropiunknown.md)から派生したインターフェイスの場合。</span><span class="sxs-lookup"><span data-stu-id="dbb5d-119">For interfaces derived from [IMAPIProp](imapipropiunknown.md).</span></span> <span data-ttu-id="dbb5d-120">非トランザクションの場合、変更はすぐに反映されるようになります。トランザクションの場合、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)が呼び出されるまで、変更は有効になりません。</span><span class="sxs-lookup"><span data-stu-id="dbb5d-120">If nontransacted, changes take effect immediately; if transacted, changes do not take effect until [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span>  <br/> |
   
<span data-ttu-id="dbb5d-121">最初の表の次の表は、このインターフェイスのすべてのメソッドを vtable オーダーで列挙した別の表です。</span><span class="sxs-lookup"><span data-stu-id="dbb5d-121">Following the first table is another table that lists all the methods of this interface in vtable order.</span></span> <span data-ttu-id="dbb5d-122">vtable は、コンパイラによって作成された関数ポインターの配列であり、MAPI オブジェクトのメソッドごとに1つの関数ポインターを含みます。</span><span class="sxs-lookup"><span data-stu-id="dbb5d-122">A vtable is an array of function pointers created by the compiler containing one function pointer for each method of a MAPI object.</span></span> <span data-ttu-id="dbb5d-123">メソッドは、宣言されたのと同じ順序で一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="dbb5d-123">The methods are listed in the same order that they are declared.</span></span> <span data-ttu-id="dbb5d-124">他のインターフェイスから継承したメソッドは、Vtable の Order テーブルには表示されませんが、それを定義するインターフェイスで記述されているものと同じ方法で使用できます。</span><span class="sxs-lookup"><span data-stu-id="dbb5d-124">Methods inherited from other interfaces are not shown in the Vtable Order table but can be used in the same way as documented in the interface that defines them.</span></span>
  
<span data-ttu-id="dbb5d-125">各インターフェイストピックの後に、インターフェイスのメソッドがアルファベット順にドキュメント化されます。</span><span class="sxs-lookup"><span data-stu-id="dbb5d-125">After each interface topic, the interface's methods are then documented in alphabetical order.</span></span> <span data-ttu-id="dbb5d-126">各メソッドについて、簡単な目的のステートメント、構文ブロック、および次の情報が記載されています。</span><span class="sxs-lookup"><span data-stu-id="dbb5d-126">For each method, the documentation includes a brief purpose statement, a syntax block, and the following information.</span></span>
  
|<span data-ttu-id="dbb5d-127">**見出し**</span><span class="sxs-lookup"><span data-stu-id="dbb5d-127">**Heading**</span></span>|<span data-ttu-id="dbb5d-128">**コンテンツ**</span><span class="sxs-lookup"><span data-stu-id="dbb5d-128">**Content**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dbb5d-129">パラメーター</span><span class="sxs-lookup"><span data-stu-id="dbb5d-129">Parameters</span></span>  <br/> |<span data-ttu-id="dbb5d-130">メソッド内の各パラメーターの説明。</span><span class="sxs-lookup"><span data-stu-id="dbb5d-130">A description of each parameter in the method.</span></span>  <br/> |
|<span data-ttu-id="dbb5d-131">戻り値</span><span class="sxs-lookup"><span data-stu-id="dbb5d-131">Return Value</span></span>  <br/> |<span data-ttu-id="dbb5d-132">メソッドが返すことのできる一意の値の説明。</span><span class="sxs-lookup"><span data-stu-id="dbb5d-132">A description of the unique values that the method can return.</span></span> <span data-ttu-id="dbb5d-133">これらの値は、発信者がコード内で確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dbb5d-133">These are the values that callers should check for in their code.</span></span>  <br/> |
|<span data-ttu-id="dbb5d-134">注釈</span><span class="sxs-lookup"><span data-stu-id="dbb5d-134">Remarks</span></span>  <br/> |<span data-ttu-id="dbb5d-135">メソッドを使用する理由と方法についての説明。</span><span class="sxs-lookup"><span data-stu-id="dbb5d-135">A description of why and how the method is used.</span></span>  <br/> |
|<span data-ttu-id="dbb5d-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="dbb5d-136">See Also</span></span>  <br/> |<span data-ttu-id="dbb5d-137">このリファレンスの他のトピックへの相互参照。</span><span class="sxs-lookup"><span data-stu-id="dbb5d-137">Cross-references to other topics in this Reference.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dbb5d-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="dbb5d-138">See also</span></span>



[<span data-ttu-id="dbb5d-139">MAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="dbb5d-139">MAPI Reference</span></span>](mapi-reference.md)

