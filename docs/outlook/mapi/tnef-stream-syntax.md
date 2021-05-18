---
title: TNEF ストリーム構文
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1353d494-c266-4715-afe7-14543a1bbe1b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 12d2a92ff80897456707c7ab8af8f704605c85d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423028"
---
# <a name="tnef-stream-syntax"></a><span data-ttu-id="66e7d-103">TNEF ストリーム構文</span><span class="sxs-lookup"><span data-stu-id="66e7d-103">TNEF Stream Syntax</span></span>

  
  
<span data-ttu-id="66e7d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66e7d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66e7d-105">このトピックでは、TNEF ストリームBakus-Nauer説明のような方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="66e7d-105">This topic presents a Bakus-Nauer like description of the TNEF stream syntax.</span></span> <span data-ttu-id="66e7d-106">この説明では、それ以上の定義を持つ非ターミニナル要素が italics に含まれています。</span><span class="sxs-lookup"><span data-stu-id="66e7d-106">In this description, nonterminal elements that have a further definition are in italics.</span></span> <span data-ttu-id="66e7d-107">定数とリテラル項目は太字です。</span><span class="sxs-lookup"><span data-stu-id="66e7d-107">Constants and literal items are in bold.</span></span> <span data-ttu-id="66e7d-108">要素のシーケンスは、1 行に順番に一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="66e7d-108">Sequences of elements are listed in order on a single line.</span></span> <span data-ttu-id="66e7d-109">たとえば _、Stream_ アイテムは定数の値TNEF_SIGNATUREキー 、続いて Object で構成 _されます_。 </span><span class="sxs-lookup"><span data-stu-id="66e7d-109">For example, the  _Stream_ item consists of the constant **TNEF_SIGNATURE**, followed by a  _Key_, followed by an  _Object_.</span></span> <span data-ttu-id="66e7d-110">アイテムに複数の実装が可能な場合、代替案は連続した行に一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="66e7d-110">When an item has more than one possible implementation, the alternatives are listed on consecutive lines.</span></span> <span data-ttu-id="66e7d-111">たとえば、_オブジェクト_ は、オブジェクト、Message_Seq、Message_Seq、Attach_Seq、または単なるAttach_Seq _で構成Attach_Seq。_  </span><span class="sxs-lookup"><span data-stu-id="66e7d-111">For example, an  _Object_ can consist of a  _Message_Seq_, a  _Message_Seq_ followed by an  _Attach_Seq_, or just an  _Attach_Seq_.</span></span>
  
 <span data-ttu-id="66e7d-112">_TNEF_Stream:_</span><span class="sxs-lookup"><span data-stu-id="66e7d-112">_TNEF_Stream:_</span></span>
  
> <span data-ttu-id="66e7d-113">**TNEF_SIGNATURE**_キー_ _オブジェクト_</span><span class="sxs-lookup"><span data-stu-id="66e7d-113">**TNEF_SIGNATURE** _Key_ _Object_</span></span>
    
 <span data-ttu-id="66e7d-114">_キー:_</span><span class="sxs-lookup"><span data-stu-id="66e7d-114">_Key:_</span></span>
  
> <span data-ttu-id="66e7d-115">0 以外の 16 ビット符号なし整数</span><span class="sxs-lookup"><span data-stu-id="66e7d-115">a nonzero 16-bit unsigned integer</span></span>
    
<span data-ttu-id="66e7d-116">TNEF が有効なトランスポートは、TNEF 実装を使用して TNEF ストリームを生成する前に、この値を生成します。</span><span class="sxs-lookup"><span data-stu-id="66e7d-116">TNEF enabled transports generate this value before using the TNEF implementation to generate a TNEF stream.</span></span>
  
 <span data-ttu-id="66e7d-117">_オブジェクト:_</span><span class="sxs-lookup"><span data-stu-id="66e7d-117">_Object:_</span></span>
  
>  <span data-ttu-id="66e7d-118">_Message_Seq Message_Seq Attach_Seq Attach_Seq_</span><span class="sxs-lookup"><span data-stu-id="66e7d-118">_Message_Seq Message_Seq Attach_Seq Attach_Seq_</span></span>
    
 <span data-ttu-id="66e7d-119">_Message_Seq:_</span><span class="sxs-lookup"><span data-stu-id="66e7d-119">_Message_Seq:_</span></span>
  
>  <span data-ttu-id="66e7d-120">_attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="66e7d-120">_attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_</span></span>
    
 <span data-ttu-id="66e7d-121">_attTnefVersion:_</span><span class="sxs-lookup"><span data-stu-id="66e7d-121">_attTnefVersion:_</span></span>
  
> <span data-ttu-id="66e7d-122">**LVL_MESSAGE attTnefVersion sizeof(ULONG) 0x00010000\*\*\*\*チェックサム**</span><span class="sxs-lookup"><span data-stu-id="66e7d-122">**LVL_MESSAGE attTnefVersion sizeof(ULONG)** **0x00010000** checksum</span></span> 
    
 <span data-ttu-id="66e7d-123">_attMessageClass:_</span><span class="sxs-lookup"><span data-stu-id="66e7d-123">_attMessageClass:_</span></span>
  
> <span data-ttu-id="66e7d-124">**LVL_MESSAGE attMessageClass** _msg_class_length msg_class_ チェックサム</span><span class="sxs-lookup"><span data-stu-id="66e7d-124">**LVL_MESSAGE attMessageClass** _msg_class_length msg_class_ checksum</span></span> 
    
 <span data-ttu-id="66e7d-125">_Msg_Attribute_Seq:_</span><span class="sxs-lookup"><span data-stu-id="66e7d-125">_Msg_Attribute_Seq:_</span></span>
  
>  <span data-ttu-id="66e7d-126">_Msg_Attribute Msg_Attribute Msg_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="66e7d-126">_Msg_Attribute Msg_Attribute Msg_Attribute_Seq_</span></span>
    
 <span data-ttu-id="66e7d-127">_Msg_Attribute:_</span><span class="sxs-lookup"><span data-stu-id="66e7d-127">_Msg_Attribute:_</span></span>
  
> <span data-ttu-id="66e7d-128">**LVL_MESSAGE-ID** 属性長属性データ チェックサム</span><span class="sxs-lookup"><span data-stu-id="66e7d-128">**LVL_MESSAGE** attribute-ID attribute-length attribute-data checksum</span></span> 
    
<span data-ttu-id="66e7d-129">属性 ID は **、attSubject** などの TNEF 属性識別子の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="66e7d-129">Attribute-ID is one of the TNEF attribute identifiers, such as **attSubject**.</span></span> <span data-ttu-id="66e7d-130">属性の長さは、属性データのバイト単位の長さです。</span><span class="sxs-lookup"><span data-stu-id="66e7d-130">Attribute-length is the length in bytes of the attribute data.</span></span> <span data-ttu-id="66e7d-131">属性データは、属性に関連付けられたデータです。</span><span class="sxs-lookup"><span data-stu-id="66e7d-131">Attribute-data is the data associated with the attribute.</span></span>
  
 <span data-ttu-id="66e7d-132">_Attach_Seq:_</span><span class="sxs-lookup"><span data-stu-id="66e7d-132">_Attach_Seq:_</span></span>
  
>  <span data-ttu-id="66e7d-133">_attRenddata attRenddata Att_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="66e7d-133">_attRenddata attRenddata Att_Attribute_Seq_</span></span>
    
 <span data-ttu-id="66e7d-134">_attRenddata:_</span><span class="sxs-lookup"><span data-stu-id="66e7d-134">_attRenddata:_</span></span>
  
> <span data-ttu-id="66e7d-135">**LVL_ATTACHMENT attRenddata** **sizeof(RENDDATA) renddata** チェックサム</span><span class="sxs-lookup"><span data-stu-id="66e7d-135">**LVL_ATTACHMENT attRenddata** **sizeof(RENDDATA)** renddata checksum</span></span> 
    
<span data-ttu-id="66e7d-136">Renddata は、対応する添付ファイルのレンダリング情報を含む **RENDDATA** 構造体に関連付けられたデータです。</span><span class="sxs-lookup"><span data-stu-id="66e7d-136">Renddata is the data associated with the **RENDDATA** structure that contains the rendering information for the corresponding attachment.</span></span> <span data-ttu-id="66e7d-137">**RENDDATA 構造** は TNEF で定義されます。H ヘッダー ファイル。</span><span class="sxs-lookup"><span data-stu-id="66e7d-137">The **RENDDATA** structure is defined in the TNEF.H header file.</span></span> 
  
 <span data-ttu-id="66e7d-138">_Att_Attribute_Seq:_</span><span class="sxs-lookup"><span data-stu-id="66e7d-138">_Att_Attribute_Seq:_</span></span>
  
>  <span data-ttu-id="66e7d-139">_Att_Attribute Att_Attribute Att_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="66e7d-139">_Att_Attribute Att_Attribute Att_Attribute_Seq_</span></span>
    
 <span data-ttu-id="66e7d-140">_Att_Attribute:_</span><span class="sxs-lookup"><span data-stu-id="66e7d-140">_Att_Attribute:_</span></span>
  
> <span data-ttu-id="66e7d-141">**LVL_ATTACHMENT-ID** 属性長属性データ チェックサム</span><span class="sxs-lookup"><span data-stu-id="66e7d-141">**LVL_ATTACHMENT** attribute-ID attribute-length attribute-data checksum</span></span> 
    
<span data-ttu-id="66e7d-142">属性 ID、属性の長さ、および属性データは、属性アイテムと同Msg_Attributeです。</span><span class="sxs-lookup"><span data-stu-id="66e7d-142">Attribute-ID, attribute-length, and attribute-data have the same meanings as for the Msg_Attribute item.</span></span>
  

