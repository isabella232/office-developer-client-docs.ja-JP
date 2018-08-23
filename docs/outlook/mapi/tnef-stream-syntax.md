---
title: TNEF ストリームの構文
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1353d494-c266-4715-afe7-14543a1bbe1b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: cbaf37415608dd1d79a06be65b34632f2b4afc89
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804133"
---
# <a name="tnef-stream-syntax"></a><span data-ttu-id="d4d82-103">TNEF ストリームの構文</span><span class="sxs-lookup"><span data-stu-id="d4d82-103">TNEF Stream Syntax</span></span>

  
  
<span data-ttu-id="d4d82-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d4d82-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d4d82-105">TNEF ストリームの構文の説明のような Bakus ・ Nauer をここに示します。</span><span class="sxs-lookup"><span data-stu-id="d4d82-105">This topic presents a Bakus-Nauer like description of the TNEF stream syntax.</span></span> <span data-ttu-id="d4d82-106">この説明では、斜体文字で終端要素をさらに定義を持ちます。</span><span class="sxs-lookup"><span data-stu-id="d4d82-106">In this description, nonterminal elements that have a further definition are in italics.</span></span> <span data-ttu-id="d4d82-107">定数とリテラルの項目は、太字で。</span><span class="sxs-lookup"><span data-stu-id="d4d82-107">Constants and literal items are in bold.</span></span> <span data-ttu-id="d4d82-108">要素のシーケンスは、1 つの行に順に並んでいます。</span><span class="sxs-lookup"><span data-stu-id="d4d82-108">Sequences of elements are listed in order on a single line.</span></span> <span data-ttu-id="d4d82-109">たとえば、_ストリーム_の項目は、定数**TNEF_SIGNATURE**、_キー_、_オブジェクト_の後に続くので構成されます。</span><span class="sxs-lookup"><span data-stu-id="d4d82-109">For example, the  _Stream_ item consists of the constant **TNEF_SIGNATURE**, followed by a  _Key_, followed by an  _Object_.</span></span> <span data-ttu-id="d4d82-110">アイテムに複数の可能な実装がある場合は、連続する行の代替案のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d4d82-110">When an item has more than one possible implementation, the alternatives are listed on consecutive lines.</span></span> <span data-ttu-id="d4d82-111">たとえば、_オブジェクト_は、 _Message_Seq_、 _Message_Seq_ _Attach_Seq_、または単に_Attach_Seq_に続くので構成できます。</span><span class="sxs-lookup"><span data-stu-id="d4d82-111">For example, an  _Object_ can consist of a  _Message_Seq_, a  _Message_Seq_ followed by an  _Attach_Seq_, or just an  _Attach_Seq_.</span></span>
  
 <span data-ttu-id="d4d82-112">_TNEF_Stream。_</span><span class="sxs-lookup"><span data-stu-id="d4d82-112">_TNEF_Stream:_</span></span>
  
> <span data-ttu-id="d4d82-113">**TNEF_SIGNATURE**_キー__オブジェクト_</span><span class="sxs-lookup"><span data-stu-id="d4d82-113">**TNEF_SIGNATURE** _Key_ _Object_</span></span>
    
 <span data-ttu-id="d4d82-114">_キー:_</span><span class="sxs-lookup"><span data-stu-id="d4d82-114">_Key:_</span></span>
  
> <span data-ttu-id="d4d82-115">0 以外の値を 16 ビット符号なし整数</span><span class="sxs-lookup"><span data-stu-id="d4d82-115">a nonzero 16-bit unsigned integer</span></span>
    
<span data-ttu-id="d4d82-116">TNEF を有効になっているトランスポートは、TNEF の実装を使用して、TNEF ストリームを生成する前にこの値を生成します。</span><span class="sxs-lookup"><span data-stu-id="d4d82-116">TNEF enabled transports generate this value before using the TNEF implementation to generate a TNEF stream.</span></span>
  
 <span data-ttu-id="d4d82-117">_オブジェクト:_</span><span class="sxs-lookup"><span data-stu-id="d4d82-117">_Object:_</span></span>
  
>  <span data-ttu-id="d4d82-118">_Message_Seq Message_Seq Attach_Seq Attach_Seq_</span><span class="sxs-lookup"><span data-stu-id="d4d82-118">_Message_Seq Message_Seq Attach_Seq Attach_Seq_</span></span>
    
 <span data-ttu-id="d4d82-119">_Message_Seq。_</span><span class="sxs-lookup"><span data-stu-id="d4d82-119">_Message_Seq:_</span></span>
  
>  <span data-ttu-id="d4d82-120">_attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="d4d82-120">_attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_</span></span>
    
 <span data-ttu-id="d4d82-121">_attTnefVersion。_</span><span class="sxs-lookup"><span data-stu-id="d4d82-121">_attTnefVersion:_</span></span>
  
> <span data-ttu-id="d4d82-122">**LVL_MESSAGE attTnefVersion sizeof(ULONG)****0x00010000**チェックサム</span><span class="sxs-lookup"><span data-stu-id="d4d82-122">**LVL_MESSAGE attTnefVersion sizeof(ULONG)** **0x00010000** checksum</span></span> 
    
 <span data-ttu-id="d4d82-123">_attMessageClass。_</span><span class="sxs-lookup"><span data-stu-id="d4d82-123">_attMessageClass:_</span></span>
  
> <span data-ttu-id="d4d82-124">**LVL_MESSAGE attMessageClass**_msg_class_length msg_class_チェックサム</span><span class="sxs-lookup"><span data-stu-id="d4d82-124">**LVL_MESSAGE attMessageClass** _msg_class_length msg_class_ checksum</span></span> 
    
 <span data-ttu-id="d4d82-125">_Msg_Attribute_Seq。_</span><span class="sxs-lookup"><span data-stu-id="d4d82-125">_Msg_Attribute_Seq:_</span></span>
  
>  <span data-ttu-id="d4d82-126">_Msg_Attribute Msg_Attribute Msg_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="d4d82-126">_Msg_Attribute Msg_Attribute Msg_Attribute_Seq_</span></span>
    
 <span data-ttu-id="d4d82-127">_Msg_Attribute。_</span><span class="sxs-lookup"><span data-stu-id="d4d82-127">_Msg_Attribute:_</span></span>
  
> <span data-ttu-id="d4d82-128">**LVL_MESSAGE**属性 ID の属性の長さの属性データのチェックサム</span><span class="sxs-lookup"><span data-stu-id="d4d82-128">**LVL_MESSAGE** attribute-ID attribute-length attribute-data checksum</span></span> 
    
<span data-ttu-id="d4d82-129">属性 ID は、TNEF 属性識別子の**attSubject**などの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="d4d82-129">Attribute-ID is one of the TNEF attribute identifiers, such as **attSubject**.</span></span> <span data-ttu-id="d4d82-130">属性の長さは、属性データの長さ (バイト単位) です。</span><span class="sxs-lookup"><span data-stu-id="d4d82-130">Attribute-length is the length in bytes of the attribute data.</span></span> <span data-ttu-id="d4d82-131">属性データは、属性に関連付けられているデータです。</span><span class="sxs-lookup"><span data-stu-id="d4d82-131">Attribute-data is the data associated with the attribute.</span></span>
  
 <span data-ttu-id="d4d82-132">_Attach_Seq。_</span><span class="sxs-lookup"><span data-stu-id="d4d82-132">_Attach_Seq:_</span></span>
  
>  <span data-ttu-id="d4d82-133">_attRenddata attRenddata Att_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="d4d82-133">_attRenddata attRenddata Att_Attribute_Seq_</span></span>
    
 <span data-ttu-id="d4d82-134">_attRenddata。_</span><span class="sxs-lookup"><span data-stu-id="d4d82-134">_attRenddata:_</span></span>
  
> <span data-ttu-id="d4d82-135">**LVL_ATTACHMENT attRenddata****sizeof(RENDDATA)** renddata のチェックサム</span><span class="sxs-lookup"><span data-stu-id="d4d82-135">**LVL_ATTACHMENT attRenddata** **sizeof(RENDDATA)** renddata checksum</span></span> 
    
<span data-ttu-id="d4d82-136">Renddata は、対応する添付ファイルのレンダリング情報を格納する**RENDDATA**構造体に関連付けられているデータです。</span><span class="sxs-lookup"><span data-stu-id="d4d82-136">Renddata is the data associated with the **RENDDATA** structure that contains the rendering information for the corresponding attachment.</span></span> <span data-ttu-id="d4d82-137">**RENDDATA**構造体は、TNEF で定義されます。H ヘッダー ファイルです。</span><span class="sxs-lookup"><span data-stu-id="d4d82-137">The **RENDDATA** structure is defined in the TNEF.H header file.</span></span> 
  
 <span data-ttu-id="d4d82-138">_Att_Attribute_Seq。_</span><span class="sxs-lookup"><span data-stu-id="d4d82-138">_Att_Attribute_Seq:_</span></span>
  
>  <span data-ttu-id="d4d82-139">_Att_Attribute Att_Attribute Att_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="d4d82-139">_Att_Attribute Att_Attribute Att_Attribute_Seq_</span></span>
    
 <span data-ttu-id="d4d82-140">_Att_Attribute。_</span><span class="sxs-lookup"><span data-stu-id="d4d82-140">_Att_Attribute:_</span></span>
  
> <span data-ttu-id="d4d82-141">**LVL_ATTACHMENT**属性 ID の属性の長さの属性データのチェックサム</span><span class="sxs-lookup"><span data-stu-id="d4d82-141">**LVL_ATTACHMENT** attribute-ID attribute-length attribute-data checksum</span></span> 
    
<span data-ttu-id="d4d82-142">属性 ID、属性の長さ、および属性データは、Msg_Attribute の項目の場合と同じの意味を持ちます。</span><span class="sxs-lookup"><span data-stu-id="d4d82-142">Attribute-ID, attribute-length, and attribute-data have the same meanings as for the Msg_Attribute item.</span></span>
  

