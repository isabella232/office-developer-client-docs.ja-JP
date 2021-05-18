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
# <a name="mapi-interfaces"></a><span data-ttu-id="0353a-103">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="0353a-103">MAPI Interfaces</span></span>

  
  
<span data-ttu-id="0353a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0353a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0353a-105">各インターフェイスのドキュメントは、インターフェイスの目的の簡単な説明と、次の情報を含むテーブルを含む概要セクションで構成されます。</span><span class="sxs-lookup"><span data-stu-id="0353a-105">The documentation for each interface consists of an introductory section that includes a brief description of the interface's purpose followed by a table that contains the following information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0353a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0353a-106">Header file:</span></span>  <br/> |<span data-ttu-id="0353a-107">インターフェイスが定義され、ソース コードをコンパイルするときに含める必要があるヘッダー ファイル。</span><span class="sxs-lookup"><span data-stu-id="0353a-107">The header file where the interface is defined and that must be included when you compile your source code.</span></span>  <br/> |
|<span data-ttu-id="0353a-108">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="0353a-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="0353a-109">インターフェイスを公開するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="0353a-109">The object that exposes the interface.</span></span>  <br/> |
|<span data-ttu-id="0353a-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="0353a-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="0353a-111">インターフェイスの実装を提供するコンポーネントの一覧。</span><span class="sxs-lookup"><span data-stu-id="0353a-111">A list of the components that provide an implementation of the interface.</span></span>  <br/> |
|<span data-ttu-id="0353a-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="0353a-112">Called by:</span></span>  <br/> |<span data-ttu-id="0353a-113">通常、インターフェイスのメソッドを呼び出すコンポーネントの一覧。</span><span class="sxs-lookup"><span data-stu-id="0353a-113">A list of the components that typically call the methods of the interface.</span></span>  <br/> |
|<span data-ttu-id="0353a-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="0353a-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="0353a-115">インターフェイス識別子 GUID。</span><span class="sxs-lookup"><span data-stu-id="0353a-115">The interface identifier GUID.</span></span>  <br/> |
|<span data-ttu-id="0353a-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="0353a-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="0353a-117">インターフェイスを公開するオブジェクトのポインターの種類。</span><span class="sxs-lookup"><span data-stu-id="0353a-117">The pointer type for the object that exposes the interface.</span></span>  <br/> |
|<span data-ttu-id="0353a-118">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="0353a-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="0353a-119">IMAPIProp から派生した [インターフェイスの場合](imapipropiunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="0353a-119">For interfaces derived from [IMAPIProp](imapipropiunknown.md).</span></span> <span data-ttu-id="0353a-120">変換されていない場合、変更は直ちに有効になります。トランザクションを実行した場合 [、IMAPIProp::SaveChanges](imapiprop-savechanges.md) が呼び出されるまで、変更は有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="0353a-120">If nontransacted, changes take effect immediately; if transacted, changes do not take effect until [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span>  <br/> |
   
<span data-ttu-id="0353a-121">最初の表の後に、このインターフェイスのすべてのメソッドを vtable の順序で一覧表示する別の表を示します。</span><span class="sxs-lookup"><span data-stu-id="0353a-121">Following the first table is another table that lists all the methods of this interface in vtable order.</span></span> <span data-ttu-id="0353a-122">vtable は、MAPI オブジェクトのメソッドごとに 1 つの関数ポインターを含むコンパイラによって作成された関数ポインターの配列です。</span><span class="sxs-lookup"><span data-stu-id="0353a-122">A vtable is an array of function pointers created by the compiler containing one function pointer for each method of a MAPI object.</span></span> <span data-ttu-id="0353a-123">メソッドは、宣言された順序と同じ順序で一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="0353a-123">The methods are listed in the same order that they are declared.</span></span> <span data-ttu-id="0353a-124">他のインターフェイスから継承されたメソッドは、Vtable Order テーブルには表示されませんが、それらを定義するインターフェイスに記載されているのと同じ方法で使用できます。</span><span class="sxs-lookup"><span data-stu-id="0353a-124">Methods inherited from other interfaces are not shown in the Vtable Order table but can be used in the same way as documented in the interface that defines them.</span></span>
  
<span data-ttu-id="0353a-125">各インターフェイス トピックの後、インターフェイスのメソッドはアルファベット順に文書化されます。</span><span class="sxs-lookup"><span data-stu-id="0353a-125">After each interface topic, the interface's methods are then documented in alphabetical order.</span></span> <span data-ttu-id="0353a-126">各メソッドについて、ドキュメントには簡単な目的のステートメント、構文ブロック、および次の情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0353a-126">For each method, the documentation includes a brief purpose statement, a syntax block, and the following information.</span></span>
  
|<span data-ttu-id="0353a-127">**見出し**</span><span class="sxs-lookup"><span data-stu-id="0353a-127">**Heading**</span></span>|<span data-ttu-id="0353a-128">**Content**</span><span class="sxs-lookup"><span data-stu-id="0353a-128">**Content**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0353a-129">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0353a-129">Parameters</span></span>  <br/> |<span data-ttu-id="0353a-130">メソッド内の各パラメーターの説明。</span><span class="sxs-lookup"><span data-stu-id="0353a-130">A description of each parameter in the method.</span></span>  <br/> |
|<span data-ttu-id="0353a-131">戻り値</span><span class="sxs-lookup"><span data-stu-id="0353a-131">Return Value</span></span>  <br/> |<span data-ttu-id="0353a-132">メソッドが返す一意の値の説明。</span><span class="sxs-lookup"><span data-stu-id="0353a-132">A description of the unique values that the method can return.</span></span> <span data-ttu-id="0353a-133">これらは、呼び出し元がコードでチェックする必要がある値です。</span><span class="sxs-lookup"><span data-stu-id="0353a-133">These are the values that callers should check for in their code.</span></span>  <br/> |
|<span data-ttu-id="0353a-134">注釈</span><span class="sxs-lookup"><span data-stu-id="0353a-134">Remarks</span></span>  <br/> |<span data-ttu-id="0353a-135">メソッドの使用理由と使い方の説明。</span><span class="sxs-lookup"><span data-stu-id="0353a-135">A description of why and how the method is used.</span></span>  <br/> |
|<span data-ttu-id="0353a-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="0353a-136">See Also</span></span>  <br/> |<span data-ttu-id="0353a-137">このリファレンスの他のトピックへの相互参照。</span><span class="sxs-lookup"><span data-stu-id="0353a-137">Cross-references to other topics in this Reference.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0353a-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="0353a-138">See also</span></span>



[<span data-ttu-id="0353a-139">MAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="0353a-139">MAPI Reference</span></span>](mapi-reference.md)

