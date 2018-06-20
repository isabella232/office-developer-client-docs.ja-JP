---
title: MAPI インターフェイス
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 34a66cf0-b4e0-4fd5-b937-cd157888961d
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e485079de800c63b02d71b3c3ccb90d66101c64b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801392"
---
# <a name="mapi-interfaces"></a><span data-ttu-id="2b823-103">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="2b823-103">MAPI Interfaces</span></span>

  
  
<span data-ttu-id="2b823-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2b823-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2b823-105">各インタ フェースのマニュアルは、次の情報を含むテーブルの後にインタ フェースの目的の簡単な説明を含む紹介の章で構成されます。</span><span class="sxs-lookup"><span data-stu-id="2b823-105">The documentation for each interface consists of an introductory section that includes a brief description of the interface's purpose followed by a table that contains the following information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2b823-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2b823-106">Header file:</span></span>  <br/> |<span data-ttu-id="2b823-107">インターフェイスが定義されているし、を含める必要があるソース コードをコンパイルするときのヘッダー ファイルです。</span><span class="sxs-lookup"><span data-stu-id="2b823-107">The header file where the interface is defined and that must be included when you compile your source code.</span></span>  <br/> |
|<span data-ttu-id="2b823-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="2b823-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="2b823-109">インターフェイスを公開するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="2b823-109">The object that exposes the interface.</span></span>  <br/> |
|<span data-ttu-id="2b823-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="2b823-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="2b823-111">インターフェイスの実装を提供するコンポーネントの一覧です。</span><span class="sxs-lookup"><span data-stu-id="2b823-111">A list of the components that provide an implementation of the interface.</span></span>  <br/> |
|<span data-ttu-id="2b823-112">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2b823-112">Called by:</span></span>  <br/> |<span data-ttu-id="2b823-113">通常、インターフェイスのメソッドを呼び出すコンポーネントの一覧です。</span><span class="sxs-lookup"><span data-stu-id="2b823-113">A list of the components that typically call the methods of the interface.</span></span>  <br/> |
|<span data-ttu-id="2b823-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="2b823-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2b823-115">インターフェイス識別子の GUID です。</span><span class="sxs-lookup"><span data-stu-id="2b823-115">The interface identifier GUID.</span></span>  <br/> |
|<span data-ttu-id="2b823-116">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="2b823-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="2b823-117">インターフェイスを公開するオブジェクトのポインターの型です。</span><span class="sxs-lookup"><span data-stu-id="2b823-117">The pointer type for the object that exposes the interface.</span></span>  <br/> |
|<span data-ttu-id="2b823-118">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="2b823-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="2b823-119">[IMAPIProp](imapipropiunknown.md)から派生したインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="2b823-119">For interfaces derived from [IMAPIProp](imapipropiunknown.md).</span></span> <span data-ttu-id="2b823-120">非トランザクション、変更が直ちに有効です。場合は、トランザクションの変更は反映されません[IMAPIProp::SaveChanges](imapiprop-savechanges.md)が呼び出されるまで。</span><span class="sxs-lookup"><span data-stu-id="2b823-120">If nontransacted, changes take effect immediately; if transacted, changes do not take effect until [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span>  <br/> |
   
<span data-ttu-id="2b823-121">次の最初の表は、vtable の順序では、このインターフェイスのすべてのメソッドの一覧が表示される別のテーブルです。</span><span class="sxs-lookup"><span data-stu-id="2b823-121">Following the first table is another table that lists all the methods of this interface in vtable order.</span></span> <span data-ttu-id="2b823-122">Vtable は、MAPI オブジェクトのメソッドごとに 1 つの関数ポインターが含まれているコンパイラで作成された関数ポインターの配列です。</span><span class="sxs-lookup"><span data-stu-id="2b823-122">A vtable is an array of function pointers created by the compiler containing one function pointer for each method of a MAPI object.</span></span> <span data-ttu-id="2b823-123">メソッドは、宣言されていることと同じ順序に表示されます。</span><span class="sxs-lookup"><span data-stu-id="2b823-123">The methods are listed in the same order that they are declared.</span></span> <span data-ttu-id="2b823-124">他のインターフェイスから継承したメソッドは Vtable の順序の表には表示されませんが、それを定義するインターフェイスに記述されていると同じ方法で使用することができます。</span><span class="sxs-lookup"><span data-stu-id="2b823-124">Methods inherited from other interfaces are not shown in the Vtable Order table but can be used in the same way as documented in the interface that defines them.</span></span>
  
<span data-ttu-id="2b823-125">後は、各インターフェイスのトピックでは、インターフェイスのメソッドは、アルファベット順に記載されています。</span><span class="sxs-lookup"><span data-stu-id="2b823-125">After each interface topic, the interface's methods are then documented in alphabetical order.</span></span> <span data-ttu-id="2b823-126">メソッドごとに、ドキュメントには、目的の簡単な文、構文ブロック、および次の情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2b823-126">For each method, the documentation includes a brief purpose statement, a syntax block, and the following information.</span></span>
  
|<span data-ttu-id="2b823-127">**見出し**</span><span class="sxs-lookup"><span data-stu-id="2b823-127">**Heading**</span></span>|<span data-ttu-id="2b823-128">**コンテンツ**</span><span class="sxs-lookup"><span data-stu-id="2b823-128">**Content**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2b823-129">Parameters</span><span class="sxs-lookup"><span data-stu-id="2b823-129">Parameters</span></span>  <br/> |<span data-ttu-id="2b823-130">メソッドの各パラメーターの説明です。</span><span class="sxs-lookup"><span data-stu-id="2b823-130">A description of each parameter in the method.</span></span>  <br/> |
|<span data-ttu-id="2b823-131">戻り値</span><span class="sxs-lookup"><span data-stu-id="2b823-131">Return Value</span></span>  <br/> |<span data-ttu-id="2b823-132">メソッドが返すことができる一意の値の説明です。</span><span class="sxs-lookup"><span data-stu-id="2b823-132">A description of the unique values that the method can return.</span></span> <span data-ttu-id="2b823-133">これらは、値がコード内の呼び出し元を確認することです。</span><span class="sxs-lookup"><span data-stu-id="2b823-133">These are the values that callers should check for in their code.</span></span>  <br/> |
|<span data-ttu-id="2b823-134">備考</span><span class="sxs-lookup"><span data-stu-id="2b823-134">Remarks</span></span>  <br/> |<span data-ttu-id="2b823-135">メソッドを使用する理由と方法の説明です。</span><span class="sxs-lookup"><span data-stu-id="2b823-135">A description of why and how the method is used.</span></span>  <br/> |
|<span data-ttu-id="2b823-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="2b823-136">See Also</span></span>  <br/> |<span data-ttu-id="2b823-137">このリファレンスでは、他のトピックへの相互参照。</span><span class="sxs-lookup"><span data-stu-id="2b823-137">Cross-references to other topics in this Reference.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2b823-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="2b823-138">See also</span></span>



[<span data-ttu-id="2b823-139">MAPI ���t�@�����X</span><span class="sxs-lookup"><span data-stu-id="2b823-139">MAPI Reference</span></span>](mapi-reference.md)

