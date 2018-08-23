---
title: TNEF ストリームの構造
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8eda1251-3858-4832-ac43-d817b4a7ea59
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0fcd1c79d1c0debfb18d270dc0e40de42842c6d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804123"
---
# <a name="tnef-stream-structure"></a><span data-ttu-id="0affc-103">TNEF ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="0affc-103">TNEF Stream Structure</span></span>

  
  
<span data-ttu-id="0affc-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0affc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0affc-105">TNEF ストリームは、TNEF ストリームとストリームを識別する 32 ビットの署名で開始します。</span><span class="sxs-lookup"><span data-stu-id="0affc-105">A TNEF stream begins with a 32-bit signature that identifies the stream as a TNEF stream.</span></span> <span data-ttu-id="0affc-106">次の署名は、タグ付けされたメッセージのテキスト内の位置に添付ファイルを相互参照するキーとして使用される 16 ビットの符号なし整数です。</span><span class="sxs-lookup"><span data-stu-id="0affc-106">Following the signature is a 16-bit unsigned integer that is used as a key to cross-reference attachments to their location in the tagged message text.</span></span> <span data-ttu-id="0affc-107">ストリームの残りの部分は、TNEF の属性のシーケンスです。</span><span class="sxs-lookup"><span data-stu-id="0affc-107">The remainder of the stream is a sequence of TNEF attributes.</span></span> <span data-ttu-id="0affc-108">TNEF ストリームで指定されたメッセージの属性が先頭に表示され、添付ファイルの属性に従います。</span><span class="sxs-lookup"><span data-stu-id="0affc-108">Message attributes appear first in the TNEF stream, and attachment attributes follow.</span></span> <span data-ttu-id="0affc-109">特定の添付ファイルに属している属性グループ化、 **attAttachRenddata**属性を使用して開始します。</span><span class="sxs-lookup"><span data-stu-id="0affc-109">Attributes that belong to a particular attachment are grouped together, beginning with the **attAttachRenddata** attribute.</span></span> 
  
<span data-ttu-id="0affc-110">TNEF ストリームで使用されている定数の値のほとんどは、TNEF で定義されます。H ヘッダー ファイルです。</span><span class="sxs-lookup"><span data-stu-id="0affc-110">Most of the constant values used in TNEF streams are defined in the TNEF.H header file.</span></span> <span data-ttu-id="0affc-111">特に、 **TNEF_SIGNATURE**、 **LVL_MESSAGE**、 **LVL_ATTACHMENT**、およびすべての TNEF 属性識別子は、このファイルで定義されます。</span><span class="sxs-lookup"><span data-stu-id="0affc-111">Notably, **TNEF_SIGNATURE**, **LVL_MESSAGE**, **LVL_ATTACHMENT**, and all the TNEF attribute identifiers are defined in this file.</span></span> <span data-ttu-id="0affc-112">C 言語コンパイラの解釈によって示される値は、他の定数であります。</span><span class="sxs-lookup"><span data-stu-id="0affc-112">Other constants have the values indicated by their interpretation to a C language compiler.</span></span> <span data-ttu-id="0affc-113">通常、このような定数を使用して次の項目のサイズを指定します。</span><span class="sxs-lookup"><span data-stu-id="0affc-113">Typically, such constants are used to give the sizes of the following item.</span></span> <span data-ttu-id="0affc-114">たとえば、項目の定義では、 **sizeof(ULONG)** では、TNEF ストリーム内の場所に次の符号なし長整数型のサイズを表す整数値が発生することを示します。</span><span class="sxs-lookup"><span data-stu-id="0affc-114">For example, **sizeof(ULONG)** in an item's definition indicates that an integer representing the size of the following unsigned long integer should occur in that place in the TNEF stream.</span></span> 
  
<span data-ttu-id="0affc-115">TNEF ストリーム内のすべての整数はリトル エンディアンの 2 進形式で格納されますが、このセクション全体で 16 進数で表示されます。</span><span class="sxs-lookup"><span data-stu-id="0affc-115">All integers in a TNEF stream are stored in little-endian binary form, but are shown in hexadecimal throughout this section.</span></span> <span data-ttu-id="0affc-116">チェックサムの値は、合計、65536、チェックサムが適用されるデータのバイト数の剰余は、単に 16 ビットの符号なし整数です。</span><span class="sxs-lookup"><span data-stu-id="0affc-116">Checksum values are simply 16-bit unsigned integers that are the sum, modulo 65536, of the bytes of data that the checksum applies to.</span></span> <span data-ttu-id="0affc-117">すべての属性の長さは、終端の null 文字を含む、符号なし長整数です。</span><span class="sxs-lookup"><span data-stu-id="0affc-117">All attribute lengths are unsigned long integers, including any terminating null characters.</span></span>
  
<span data-ttu-id="0affc-118">キーは、添付ファイルの参照キーの初期値を示す 0 以外の値の 16 ビット符号なし整数です。</span><span class="sxs-lookup"><span data-stu-id="0affc-118">The key is a nonzero, 16-bit unsigned integer that signifies the initial value of the attachment reference keys.</span></span> <span data-ttu-id="0affc-119">TNEF を使用しているサービス プロバイダーによって、 [OpenTnefStream](opentnefstream.md)関数に渡される最初の値から順番に各添付ファイルには、添付ファイルの参照キーが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="0affc-119">The attachment reference keys are assigned to each attachment sequentially beginning with the initial value that is passed to the [OpenTnefStream](opentnefstream.md) function by the service provider that is using TNEF.</span></span> <span data-ttu-id="0affc-120">サービス プロバイダーは、2 つのメッセージが同じキーを使用する可能性を最小限に抑えるためのキーの場合は、ランダムな初期値を生成します。</span><span class="sxs-lookup"><span data-stu-id="0affc-120">The service provider should generate a random initial value for the key to minimize the chance that two messages use the same key.</span></span> 
  
<span data-ttu-id="0affc-121">TNEF の実装では、対応する MAPI プロパティに属性をマップするのに属性の識別子を使用します。</span><span class="sxs-lookup"><span data-stu-id="0affc-121">The TNEF implementation uses attribute identifiers to map attributes to their corresponding MAPI properties.</span></span> <span data-ttu-id="0affc-122">属性識別子は、2 つの word 値の 32 ビットの符号なし整数です。</span><span class="sxs-lookup"><span data-stu-id="0affc-122">An attribute identifier is a 32-bit unsigned integer made up of two word values.</span></span> <span data-ttu-id="0affc-123">上位ワードのデータ型を示す文字列やバイナリなどと、下位ワードは、特定の属性を識別します。</span><span class="sxs-lookup"><span data-stu-id="0affc-123">The high-order word indicates the data type, such as string or binary, and the low-order word identifies the particular attribute.</span></span> <span data-ttu-id="0affc-124">上位 word 内のデータ型は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="0affc-124">The data types in the high order word are:</span></span>
  
|<span data-ttu-id="0affc-125">**型**</span><span class="sxs-lookup"><span data-stu-id="0affc-125">**Type**</span></span>|<span data-ttu-id="0affc-126">**値**</span><span class="sxs-lookup"><span data-stu-id="0affc-126">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0affc-127">atpTriples</span><span class="sxs-lookup"><span data-stu-id="0affc-127">atpTriples</span></span>  <br/> |<span data-ttu-id="0affc-128">0x0000</span><span class="sxs-lookup"><span data-stu-id="0affc-128">0x0000</span></span>  <br/> |
|<span data-ttu-id="0affc-129">atpString</span><span class="sxs-lookup"><span data-stu-id="0affc-129">atpString</span></span>  <br/> |<span data-ttu-id="0affc-130">0x0001</span><span class="sxs-lookup"><span data-stu-id="0affc-130">0x0001</span></span>  <br/> |
|<span data-ttu-id="0affc-131">atpText</span><span class="sxs-lookup"><span data-stu-id="0affc-131">atpText</span></span>  <br/> |<span data-ttu-id="0affc-132">0x0002</span><span class="sxs-lookup"><span data-stu-id="0affc-132">0x0002</span></span>  <br/> |
|<span data-ttu-id="0affc-133">atpDate</span><span class="sxs-lookup"><span data-stu-id="0affc-133">atpDate</span></span>  <br/> |<span data-ttu-id="0affc-134">0x0003</span><span class="sxs-lookup"><span data-stu-id="0affc-134">0x0003</span></span>  <br/> |
|<span data-ttu-id="0affc-135">atpShort</span><span class="sxs-lookup"><span data-stu-id="0affc-135">atpShort</span></span>  <br/> |<span data-ttu-id="0affc-136">0x0004</span><span class="sxs-lookup"><span data-stu-id="0affc-136">0x0004</span></span>  <br/> |
|<span data-ttu-id="0affc-137">atpLong</span><span class="sxs-lookup"><span data-stu-id="0affc-137">atpLong</span></span>  <br/> |<span data-ttu-id="0affc-138">0x0005</span><span class="sxs-lookup"><span data-stu-id="0affc-138">0x0005</span></span>  <br/> |
|<span data-ttu-id="0affc-139">atpByte</span><span class="sxs-lookup"><span data-stu-id="0affc-139">atpByte</span></span>  <br/> |<span data-ttu-id="0affc-140">0x0006</span><span class="sxs-lookup"><span data-stu-id="0affc-140">0x0006</span></span>  <br/> |
|<span data-ttu-id="0affc-141">atpWord</span><span class="sxs-lookup"><span data-stu-id="0affc-141">atpWord</span></span>  <br/> |<span data-ttu-id="0affc-142">0x0007</span><span class="sxs-lookup"><span data-stu-id="0affc-142">0x0007</span></span>  <br/> |
|<span data-ttu-id="0affc-143">atpDword</span><span class="sxs-lookup"><span data-stu-id="0affc-143">atpDword</span></span>  <br/> |<span data-ttu-id="0affc-144">0x0008</span><span class="sxs-lookup"><span data-stu-id="0affc-144">0x0008</span></span>  <br/> |
|<span data-ttu-id="0affc-145">atpMax</span><span class="sxs-lookup"><span data-stu-id="0affc-145">atpMax</span></span>  <br/> |<span data-ttu-id="0affc-146">0x0009</span><span class="sxs-lookup"><span data-stu-id="0affc-146">0x0009</span></span>  <br/> |
   
<span data-ttu-id="0affc-147">TNEF では、各属性の下位ワードの値が定義されています。H ヘッダー ファイルです。</span><span class="sxs-lookup"><span data-stu-id="0affc-147">The low-order word values for each attribute are defined in the TNEF.H header file.</span></span>
  

