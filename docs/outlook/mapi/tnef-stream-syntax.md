---
title: TNEF ストリームの構文
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1353d494-c266-4715-afe7-14543a1bbe1b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 12d2a92ff80897456707c7ab8af8f704605c85d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339635"
---
# <a name="tnef-stream-syntax"></a><span data-ttu-id="a144e-103">TNEF ストリームの構文</span><span class="sxs-lookup"><span data-stu-id="a144e-103">TNEF Stream Syntax</span></span>

  
  
<span data-ttu-id="a144e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a144e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a144e-105">このトピックでは、TNEF ストリームの構文についての、Bakus という名前の説明を示します。</span><span class="sxs-lookup"><span data-stu-id="a144e-105">This topic presents a Bakus-Nauer like description of the TNEF stream syntax.</span></span> <span data-ttu-id="a144e-106">この説明では、さらに詳細が定義されている nonterminal 要素は斜体になっています。</span><span class="sxs-lookup"><span data-stu-id="a144e-106">In this description, nonterminal elements that have a further definition are in italics.</span></span> <span data-ttu-id="a144e-107">定数とリテラルアイテムは太字で示しています。</span><span class="sxs-lookup"><span data-stu-id="a144e-107">Constants and literal items are in bold.</span></span> <span data-ttu-id="a144e-108">要素のシーケンスは、1行に順に表示されます。</span><span class="sxs-lookup"><span data-stu-id="a144e-108">Sequences of elements are listed in order on a single line.</span></span> <span data-ttu-id="a144e-109">たとえば、_ストリーム_アイテムは定数**TNEF_SIGNATURE**で構成され、その後に_キー_が続き、その後に_オブジェクト_が続きます。</span><span class="sxs-lookup"><span data-stu-id="a144e-109">For example, the  _Stream_ item consists of the constant **TNEF_SIGNATURE**, followed by a  _Key_, followed by an  _Object_.</span></span> <span data-ttu-id="a144e-110">アイテムに複数の実装がある場合、選択肢は連続した行に表示されます。</span><span class="sxs-lookup"><span data-stu-id="a144e-110">When an item has more than one possible implementation, the alternatives are listed on consecutive lines.</span></span> <span data-ttu-id="a144e-111">たとえば、_オブジェクト_は、 _Message_Seq_、 _Message_Seq_の後に_Attach_Seq_、または_Attach_Seq_だけで構成できます。</span><span class="sxs-lookup"><span data-stu-id="a144e-111">For example, an  _Object_ can consist of a  _Message_Seq_, a  _Message_Seq_ followed by an  _Attach_Seq_, or just an  _Attach_Seq_.</span></span>
  
 <span data-ttu-id="a144e-112">_TNEF_Stream:_</span><span class="sxs-lookup"><span data-stu-id="a144e-112">_TNEF_Stream:_</span></span>
  
> <span data-ttu-id="a144e-113">**TNEF_SIGNATURE**_キー__オブジェクト_</span><span class="sxs-lookup"><span data-stu-id="a144e-113">**TNEF_SIGNATURE** _Key_ _Object_</span></span>
    
 <span data-ttu-id="a144e-114">_要点_</span><span class="sxs-lookup"><span data-stu-id="a144e-114">_Key:_</span></span>
  
> <span data-ttu-id="a144e-115">0以外の16ビットの符号なし整数</span><span class="sxs-lookup"><span data-stu-id="a144e-115">a nonzero 16-bit unsigned integer</span></span>
    
<span data-ttu-id="a144e-116">tnef が有効なトランスポート tnef の実装を使用して tnef ストリームを生成する前に、この値を生成します。</span><span class="sxs-lookup"><span data-stu-id="a144e-116">TNEF enabled transports generate this value before using the TNEF implementation to generate a TNEF stream.</span></span>
  
 <span data-ttu-id="a144e-117">_対象_</span><span class="sxs-lookup"><span data-stu-id="a144e-117">_Object:_</span></span>
  
>  <span data-ttu-id="a144e-118">_Message_Seq Message_Seq Attach_Seq Attach_Seq_</span><span class="sxs-lookup"><span data-stu-id="a144e-118">_Message_Seq Message_Seq Attach_Seq Attach_Seq_</span></span>
    
 <span data-ttu-id="a144e-119">_Message_Seq:_</span><span class="sxs-lookup"><span data-stu-id="a144e-119">_Message_Seq:_</span></span>
  
>  <span data-ttu-id="a144e-120">_attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion/attTnefVersion/Msg_Attribute_Seq の添付 messageclass Msg_Attribute_Seq Msg_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="a144e-120">_attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_</span></span>
    
 <span data-ttu-id="a144e-121">_attTnefVersion:_</span><span class="sxs-lookup"><span data-stu-id="a144e-121">_attTnefVersion:_</span></span>
  
> <span data-ttu-id="a144e-122">**LVL_MESSAGE attTnefVersion sizeof (ULONG)\*\*\*\*0x00010000**チェックサム</span><span class="sxs-lookup"><span data-stu-id="a144e-122">**LVL_MESSAGE attTnefVersion sizeof(ULONG)** **0x00010000** checksum</span></span> 
    
 <span data-ttu-id="a144e-123">_/添付:_</span><span class="sxs-lookup"><span data-stu-id="a144e-123">_attMessageClass:_</span></span>
  
> <span data-ttu-id="a144e-124">**LVL_MESSAGE の添付の messageclass**_msg_class_length msg_class_チェックサム</span><span class="sxs-lookup"><span data-stu-id="a144e-124">**LVL_MESSAGE attMessageClass** _msg_class_length msg_class_ checksum</span></span> 
    
 <span data-ttu-id="a144e-125">_Msg_Attribute_Seq:_</span><span class="sxs-lookup"><span data-stu-id="a144e-125">_Msg_Attribute_Seq:_</span></span>
  
>  <span data-ttu-id="a144e-126">_Msg_Attribute Msg_Attribute Msg_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="a144e-126">_Msg_Attribute Msg_Attribute Msg_Attribute_Seq_</span></span>
    
 <span data-ttu-id="a144e-127">_Msg_Attribute:_</span><span class="sxs-lookup"><span data-stu-id="a144e-127">_Msg_Attribute:_</span></span>
  
> <span data-ttu-id="a144e-128">**LVL_MESSAGE**属性-ID 属性-長さ属性-データチェックサム</span><span class="sxs-lookup"><span data-stu-id="a144e-128">**LVL_MESSAGE** attribute-ID attribute-length attribute-data checksum</span></span> 
    
<span data-ttu-id="a144e-129">属性-ID は、発行されたものなど、TNEF \*\*\*\* 属性識別子の1つです。</span><span class="sxs-lookup"><span data-stu-id="a144e-129">Attribute-ID is one of the TNEF attribute identifiers, such as **attSubject**.</span></span> <span data-ttu-id="a144e-130">属性-length は、属性データの長さ (バイト単位) です。</span><span class="sxs-lookup"><span data-stu-id="a144e-130">Attribute-length is the length in bytes of the attribute data.</span></span> <span data-ttu-id="a144e-131">属性-data は、属性に関連付けられているデータです。</span><span class="sxs-lookup"><span data-stu-id="a144e-131">Attribute-data is the data associated with the attribute.</span></span>
  
 <span data-ttu-id="a144e-132">_Attach_Seq:_</span><span class="sxs-lookup"><span data-stu-id="a144e-132">_Attach_Seq:_</span></span>
  
>  <span data-ttu-id="a144e-133">_attRenddata attRenddata Att_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="a144e-133">_attRenddata attRenddata Att_Attribute_Seq_</span></span>
    
 <span data-ttu-id="a144e-134">_attRenddata:_</span><span class="sxs-lookup"><span data-stu-id="a144e-134">_attRenddata:_</span></span>
  
> <span data-ttu-id="a144e-135">**LVL_ATTACHMENT attRenddata\*\*\*\*sizeof (RENDDATA)** RENDDATA チェックサム</span><span class="sxs-lookup"><span data-stu-id="a144e-135">**LVL_ATTACHMENT attRenddata** **sizeof(RENDDATA)** renddata checksum</span></span> 
    
<span data-ttu-id="a144e-136">Renddata は、対応する添付ファイルのレンダリング情報を含む、 **Renddata**構造に関連付けられているデータです。</span><span class="sxs-lookup"><span data-stu-id="a144e-136">Renddata is the data associated with the **RENDDATA** structure that contains the rendering information for the corresponding attachment.</span></span> <span data-ttu-id="a144e-137">**RENDDATA**構造体は TNEF で定義されています。H ヘッダーファイル。</span><span class="sxs-lookup"><span data-stu-id="a144e-137">The **RENDDATA** structure is defined in the TNEF.H header file.</span></span> 
  
 <span data-ttu-id="a144e-138">_Att_Attribute_Seq:_</span><span class="sxs-lookup"><span data-stu-id="a144e-138">_Att_Attribute_Seq:_</span></span>
  
>  <span data-ttu-id="a144e-139">_Att_Attribute Att_Attribute Att_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="a144e-139">_Att_Attribute Att_Attribute Att_Attribute_Seq_</span></span>
    
 <span data-ttu-id="a144e-140">_Att_Attribute:_</span><span class="sxs-lookup"><span data-stu-id="a144e-140">_Att_Attribute:_</span></span>
  
> <span data-ttu-id="a144e-141">**LVL_ATTACHMENT**属性-ID 属性-長さ属性-データチェックサム</span><span class="sxs-lookup"><span data-stu-id="a144e-141">**LVL_ATTACHMENT** attribute-ID attribute-length attribute-data checksum</span></span> 
    
<span data-ttu-id="a144e-142">属性 ID、属性長、および属性データの意味は、Msg_Attribute item の場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="a144e-142">Attribute-ID, attribute-length, and attribute-data have the same meanings as for the Msg_Attribute item.</span></span>
  

