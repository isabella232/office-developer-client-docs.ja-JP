---
title: TNEF ストリームの構造
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8eda1251-3858-4832-ac43-d817b4a7ea59
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7e77c043e4f152740af9bdb2b8fb5b7bedece1c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430204"
---
# <a name="tnef-stream-structure"></a><span data-ttu-id="c835e-103">TNEF ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="c835e-103">TNEF Stream Structure</span></span>

  
  
<span data-ttu-id="c835e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c835e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c835e-105">tnef ストリームは、tnef ストリームとしてストリームを識別する32ビットの署名で始まります。</span><span class="sxs-lookup"><span data-stu-id="c835e-105">A TNEF stream begins with a 32-bit signature that identifies the stream as a TNEF stream.</span></span> <span data-ttu-id="c835e-106">このシグネチャは16ビットの符号なし整数で、タグ付きメッセージテキスト内の場所への添付ファイルを相互参照するためのキーとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="c835e-106">Following the signature is a 16-bit unsigned integer that is used as a key to cross-reference attachments to their location in the tagged message text.</span></span> <span data-ttu-id="c835e-107">ストリームの残りの部分は、TNEF 属性のシーケンスです。</span><span class="sxs-lookup"><span data-stu-id="c835e-107">The remainder of the stream is a sequence of TNEF attributes.</span></span> <span data-ttu-id="c835e-108">メッセージ属性は TNEF ストリームの最初に表示され、添付ファイル属性は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="c835e-108">Message attributes appear first in the TNEF stream, and attachment attributes follow.</span></span> <span data-ttu-id="c835e-109">特定の添付ファイルに属する属性は、 **attAttachRenddata**属性で始まるグループにまとめられています。</span><span class="sxs-lookup"><span data-stu-id="c835e-109">Attributes that belong to a particular attachment are grouped together, beginning with the **attAttachRenddata** attribute.</span></span> 
  
<span data-ttu-id="c835e-110">tnef ストリームで使用される定数値のほとんどは、tnef で定義されています。H ヘッダーファイル。</span><span class="sxs-lookup"><span data-stu-id="c835e-110">Most of the constant values used in TNEF streams are defined in the TNEF.H header file.</span></span> <span data-ttu-id="c835e-111">特に、このファイルでは、 **TNEF_SIGNATURE**、 **LVL_MESSAGE**、 **LVL_ATTACHMENT**、およびすべての TNEF 属性識別子が定義されています。</span><span class="sxs-lookup"><span data-stu-id="c835e-111">Notably, **TNEF_SIGNATURE**, **LVL_MESSAGE**, **LVL_ATTACHMENT**, and all the TNEF attribute identifiers are defined in this file.</span></span> <span data-ttu-id="c835e-112">他の定数には、C 言語コンパイラに対する解釈によって示される値があります。</span><span class="sxs-lookup"><span data-stu-id="c835e-112">Other constants have the values indicated by their interpretation to a C language compiler.</span></span> <span data-ttu-id="c835e-113">通常、このような定数は、次の項目のサイズを指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="c835e-113">Typically, such constants are used to give the sizes of the following item.</span></span> <span data-ttu-id="c835e-114">たとえば、アイテムの定義内の**sizeof (ULONG)** は、TNEF ストリーム内のその場所で、次の符号なし長整数のサイズを表す整数が発生することを示しています。</span><span class="sxs-lookup"><span data-stu-id="c835e-114">For example, **sizeof(ULONG)** in an item's definition indicates that an integer representing the size of the following unsigned long integer should occur in that place in the TNEF stream.</span></span> 
  
<span data-ttu-id="c835e-115">TNEF ストリーム内のすべての整数は、リトルエンディアンバイナリ形式で格納されますが、このセクション全体で16進数で表示されます。</span><span class="sxs-lookup"><span data-stu-id="c835e-115">All integers in a TNEF stream are stored in little-endian binary form, but are shown in hexadecimal throughout this section.</span></span> <span data-ttu-id="c835e-116">チェックサムの値は、チェックサムが適用されるデータのバイト数の合計 (モジュロ 65536) である16ビットの符号なし整数です。</span><span class="sxs-lookup"><span data-stu-id="c835e-116">Checksum values are simply 16-bit unsigned integers that are the sum, modulo 65536, of the bytes of data that the checksum applies to.</span></span> <span data-ttu-id="c835e-117">すべての属性の長さは、終端の null 文字を含む、符号なしの long 整数です。</span><span class="sxs-lookup"><span data-stu-id="c835e-117">All attribute lengths are unsigned long integers, including any terminating null characters.</span></span>
  
<span data-ttu-id="c835e-118">キーは、添付ファイル参照キーの初期値を示す、0以外の16ビット符号なし整数です。</span><span class="sxs-lookup"><span data-stu-id="c835e-118">The key is a nonzero, 16-bit unsigned integer that signifies the initial value of the attachment reference keys.</span></span> <span data-ttu-id="c835e-119">添付ファイルの参照キーは、TNEF を使用しているサービスプロバイダーによって[OpenTnefStream](opentnefstream.md)関数に渡される初期値から順に、各添付ファイルに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="c835e-119">The attachment reference keys are assigned to each attachment sequentially beginning with the initial value that is passed to the [OpenTnefStream](opentnefstream.md) function by the service provider that is using TNEF.</span></span> <span data-ttu-id="c835e-120">サービスプロバイダーは、2つのメッセージが同じキーを使用する可能性を最小限にするために、キーのランダムな初期値を生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c835e-120">The service provider should generate a random initial value for the key to minimize the chance that two messages use the same key.</span></span> 
  
<span data-ttu-id="c835e-121">TNEF 実装は、属性識別子を使用して、対応する MAPI プロパティに属性をマップします。</span><span class="sxs-lookup"><span data-stu-id="c835e-121">The TNEF implementation uses attribute identifiers to map attributes to their corresponding MAPI properties.</span></span> <span data-ttu-id="c835e-122">属性識別子は、2つの単語値で構成される32ビットの符号なし整数です。</span><span class="sxs-lookup"><span data-stu-id="c835e-122">An attribute identifier is a 32-bit unsigned integer made up of two word values.</span></span> <span data-ttu-id="c835e-123">上位の単語は、文字列やバイナリなどのデータ型を示し、下位の単語は特定の属性を識別します。</span><span class="sxs-lookup"><span data-stu-id="c835e-123">The high-order word indicates the data type, such as string or binary, and the low-order word identifies the particular attribute.</span></span> <span data-ttu-id="c835e-124">上位の単語のデータ型は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="c835e-124">The data types in the high order word are:</span></span>
  
|<span data-ttu-id="c835e-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="c835e-125">**Type**</span></span>|<span data-ttu-id="c835e-126">**値**</span><span class="sxs-lookup"><span data-stu-id="c835e-126">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c835e-127">atpTriples</span><span class="sxs-lookup"><span data-stu-id="c835e-127">atpTriples</span></span>  <br/> |<span data-ttu-id="c835e-128">0x0000</span><span class="sxs-lookup"><span data-stu-id="c835e-128">0x0000</span></span>  <br/> |
|<span data-ttu-id="c835e-129">atpstring</span><span class="sxs-lookup"><span data-stu-id="c835e-129">atpString</span></span>  <br/> |<span data-ttu-id="c835e-130">0x0001</span><span class="sxs-lookup"><span data-stu-id="c835e-130">0x0001</span></span>  <br/> |
|<span data-ttu-id="c835e-131">atptext</span><span class="sxs-lookup"><span data-stu-id="c835e-131">atpText</span></span>  <br/> |<span data-ttu-id="c835e-132">0x0002</span><span class="sxs-lookup"><span data-stu-id="c835e-132">0x0002</span></span>  <br/> |
|<span data-ttu-id="c835e-133">atpDate</span><span class="sxs-lookup"><span data-stu-id="c835e-133">atpDate</span></span>  <br/> |<span data-ttu-id="c835e-134">0x0003</span><span class="sxs-lookup"><span data-stu-id="c835e-134">0x0003</span></span>  <br/> |
|<span data-ttu-id="c835e-135">atpshort</span><span class="sxs-lookup"><span data-stu-id="c835e-135">atpShort</span></span>  <br/> |<span data-ttu-id="c835e-136">0x0004</span><span class="sxs-lookup"><span data-stu-id="c835e-136">0x0004</span></span>  <br/> |
|<span data-ttu-id="c835e-137">atpltar</span><span class="sxs-lookup"><span data-stu-id="c835e-137">atpLong</span></span>  <br/> |<span data-ttu-id="c835e-138">0x0005</span><span class="sxs-lookup"><span data-stu-id="c835e-138">0x0005</span></span>  <br/> |
|<span data-ttu-id="c835e-139">atpbyte</span><span class="sxs-lookup"><span data-stu-id="c835e-139">atpByte</span></span>  <br/> |<span data-ttu-id="c835e-140">0x0006</span><span class="sxs-lookup"><span data-stu-id="c835e-140">0x0006</span></span>  <br/> |
|<span data-ttu-id="c835e-141">atpword</span><span class="sxs-lookup"><span data-stu-id="c835e-141">atpWord</span></span>  <br/> |<span data-ttu-id="c835e-142">0x0007</span><span class="sxs-lookup"><span data-stu-id="c835e-142">0x0007</span></span>  <br/> |
|<span data-ttu-id="c835e-143">atpdword</span><span class="sxs-lookup"><span data-stu-id="c835e-143">atpDword</span></span>  <br/> |<span data-ttu-id="c835e-144">0x0008</span><span class="sxs-lookup"><span data-stu-id="c835e-144">0x0008</span></span>  <br/> |
|<span data-ttu-id="c835e-145">atpmax</span><span class="sxs-lookup"><span data-stu-id="c835e-145">atpMax</span></span>  <br/> |<span data-ttu-id="c835e-146">0x0009</span><span class="sxs-lookup"><span data-stu-id="c835e-146">0x0009</span></span>  <br/> |
   
<span data-ttu-id="c835e-147">各属性の下位ワード値は、TNEF で定義されています。H ヘッダーファイル。</span><span class="sxs-lookup"><span data-stu-id="c835e-147">The low-order word values for each attribute are defined in the TNEF.H header file.</span></span>
  

