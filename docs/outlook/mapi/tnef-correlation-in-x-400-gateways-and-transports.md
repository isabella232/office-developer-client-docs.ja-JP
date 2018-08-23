---
title: X.400 ゲートウェイおよびトランスポートでの TNEF 関連付け
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0ffa0802-bfdd-4993-b4a3-142e5d15bfb4
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ea5ca41ef21c72377ade72370e0aee1b313c92d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804110"
---
# <a name="tnef-correlation-in-x400-gateways-and-transports"></a><span data-ttu-id="66d36-103">X.400 ゲートウェイおよびトランスポートでの TNEF 関連付け</span><span class="sxs-lookup"><span data-stu-id="66d36-103">TNEF Correlation in X.400 Gateways and Transports</span></span>

  
  
<span data-ttu-id="66d36-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="66d36-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="66d36-105">ゲートウェイおよび X.400 ベースのシステムに接続するためのトランスポートは、TNEF の相関関係を実装するために IM_THIS_IPM の X.400 属性および**attMessageID**の TNEF の属性の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="66d36-105">Gateways and transports that connect to X.400-based systems, use the value of the IM_THIS_IPM X.400 attribute and the **attMessageID** TNEF attribute to implement TNEF correlation.</span></span> 
  
<span data-ttu-id="66d36-106">TNEF ストリーム内の**attMessageID**には、送信メッセージの IM_THIS_IPM 属性の値がコピーされます。</span><span class="sxs-lookup"><span data-stu-id="66d36-106">The value of the IM_THIS_IPM attribute of the outbound message is copied to **attMessageID** in the TNEF stream.</span></span> <span data-ttu-id="66d36-107">IM_THIS_IPM の X.400 属性は、通常、文字列、です**attMessageID** TNEF の属性がバイナリ値を表す 16 進数の文字列の中に。</span><span class="sxs-lookup"><span data-stu-id="66d36-107">The IM_THIS_IPM X.400 attribute is typically a string, while the **attMessageID** TNEF attribute is a string of hexadecimal digits representing a binary value.</span></span> <span data-ttu-id="66d36-108">したがって、終端の null 文字を含む、IM_THIS_IPM の X.400 属性内の各文字はその文字の ASCII 値を表す 2 桁の 16 進数文字列に変換しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="66d36-108">Therefore, each character in the IM_THIS_IPM X.400 attribute, including the terminating null character, must be converted to a 2-character hexadecimal string representing the ASCII value of that character.</span></span> <span data-ttu-id="66d36-109">たとえば、IM_THIS_IPM の X.400 属性が次の文字列である場合。</span><span class="sxs-lookup"><span data-stu-id="66d36-109">For instance, if the IM_THIS_IPM X.400 attribute is the following string:</span></span> 
  
<span data-ttu-id="66d36-110">3030322D3030312D305337533A3A3936303631312D313533373030</span><span class="sxs-lookup"><span data-stu-id="66d36-110">3030322D3030312D305337533A3A3936303631312D313533373030</span></span>
  
<span data-ttu-id="66d36-111">**attMessageID**の値は、次の一連の 16 進数になります。</span><span class="sxs-lookup"><span data-stu-id="66d36-111">then the value of **attMessageID** would be the following sequence of hexadecimal digits:</span></span> 
  
<span data-ttu-id="66d36-112">33 30 33 33 30 32 32 44</span><span class="sxs-lookup"><span data-stu-id="66d36-112">33 30 33 30 33 32 32 44</span></span>
  
<span data-ttu-id="66d36-113">33 30 33 33 30 31 32 44</span><span class="sxs-lookup"><span data-stu-id="66d36-113">33 30 33 30 33 31 32 44</span></span>
  
<span data-ttu-id="66d36-114">33 30 35 33 33 37 35 33</span><span class="sxs-lookup"><span data-stu-id="66d36-114">33 30 35 33 33 37 35 33</span></span>
  
<span data-ttu-id="66d36-115">33 41 33 41 33 39 33 36</span><span class="sxs-lookup"><span data-stu-id="66d36-115">33 41 33 41 33 39 33 36</span></span>
  
<span data-ttu-id="66d36-116">33 30 33 36 33 31 33 31</span><span class="sxs-lookup"><span data-stu-id="66d36-116">33 30 33 36 33 31 33 31</span></span>
  
<span data-ttu-id="66d36-117">32 44 33 33 31 35 33 33</span><span class="sxs-lookup"><span data-stu-id="66d36-117">32 44 33 31 33 35 33 33</span></span>
  
<span data-ttu-id="66d36-118">33 37 33 30 33 30 00</span><span class="sxs-lookup"><span data-stu-id="66d36-118">33 37 33 30 33 30 00</span></span>
  
<span data-ttu-id="66d36-119">この手法は、Microsoft Exchange Server X.400 コネクタによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="66d36-119">This technique is used by the Microsoft Exchange Server X.400 Connector.</span></span> <span data-ttu-id="66d36-120">X.400 ゲートウェイとの相互運用性を最大化するための Microsoft Exchange Server に接続するためのトランスポートには、このテクニックを使用してください。</span><span class="sxs-lookup"><span data-stu-id="66d36-120">This technique should be used by any X.400 gateways and transports that connect to Microsoft Exchange Server in order to maximize interoperability.</span></span>
  
<span data-ttu-id="66d36-121">将来と、現在の Microsoft ソフトウェアとの互換性を最大限に IM_THIS_IPM の X.400 属性もコピーする**PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) のプロパティにします。</span><span class="sxs-lookup"><span data-stu-id="66d36-121">For greatest compatibility with future as well as present Microsoft software, the IM_THIS_IPM X.400 attribute should also be copied to the **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) property.</span></span> <span data-ttu-id="66d36-122">ただし、バイナリ プロパティを**PR_TNEF_CORRELATION_KEY**には、16 進数文字列に変換必要はありません。</span><span class="sxs-lookup"><span data-stu-id="66d36-122">However, since **PR_TNEF_CORRELATION_KEY** is a binary property, no translation into a hexadecimal string is necessary.</span></span> 
  

