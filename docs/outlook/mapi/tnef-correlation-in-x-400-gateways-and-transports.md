---
title: x.400 ゲートウェイおよびトランスポートでの TNEF 相互関係
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0ffa0802-bfdd-4993-b4a3-142e5d15bfb4
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e08f16ff60a282f1be3adf93d858471e38d19957
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406375"
---
# <a name="tnef-correlation-in-x400-gateways-and-transports"></a><span data-ttu-id="a70b2-103">x.400 ゲートウェイおよびトランスポートでの TNEF 相互関係</span><span class="sxs-lookup"><span data-stu-id="a70b2-103">TNEF Correlation in X.400 Gateways and Transports</span></span>

  
  
<span data-ttu-id="a70b2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a70b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a70b2-105">ゲートウェイとトランスポートは、IM_THIS_IPM のシステムに接続します。この場合、TNEF 属性の値を使用して、 \*\*\*\* tnef の関連付けを実装します。</span><span class="sxs-lookup"><span data-stu-id="a70b2-105">Gateways and transports that connect to X.400-based systems, use the value of the IM_THIS_IPM X.400 attribute and the **attMessageID** TNEF attribute to implement TNEF correlation.</span></span> 
  
<span data-ttu-id="a70b2-106">送信メッセージの IM_THIS_IPM 属性の値は、TNEF ストリームの " \*\*\*\* 属性" にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="a70b2-106">The value of the IM_THIS_IPM attribute of the outbound message is copied to **attMessageID** in the TNEF stream.</span></span> <span data-ttu-id="a70b2-107">IM_THIS_IPM X. 400 属性は、通常は文字列ですが、 \*\*\*\* 属性はバイナリ値を表す16進数の文字列です。</span><span class="sxs-lookup"><span data-stu-id="a70b2-107">The IM_THIS_IPM X.400 attribute is typically a string, while the **attMessageID** TNEF attribute is a string of hexadecimal digits representing a binary value.</span></span> <span data-ttu-id="a70b2-108">したがって、IM_THIS_IPM X. 400 属性の各文字 (終端の null 文字を含む) は、その文字の ASCII 値を表す2文字の16進文字列に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a70b2-108">Therefore, each character in the IM_THIS_IPM X.400 attribute, including the terminating null character, must be converted to a 2-character hexadecimal string representing the ASCII value of that character.</span></span> <span data-ttu-id="a70b2-109">たとえば、IM_THIS_IPM .x 属性が次の文字列であるとします。</span><span class="sxs-lookup"><span data-stu-id="a70b2-109">For instance, if the IM_THIS_IPM X.400 attribute is the following string:</span></span> 
  
<span data-ttu-id="a70b2-110">3030322D3030312D305337533A3A3936303631312D313533373030</span><span class="sxs-lookup"><span data-stu-id="a70b2-110">3030322D3030312D305337533A3A3936303631312D313533373030</span></span>
  
<span data-ttu-id="a70b2-111">次に、[**添付**] の値は次の16進数値になります。</span><span class="sxs-lookup"><span data-stu-id="a70b2-111">then the value of **attMessageID** would be the following sequence of hexadecimal digits:</span></span> 
  
<span data-ttu-id="a70b2-112">33 30 33 30 33 32 32 44</span><span class="sxs-lookup"><span data-stu-id="a70b2-112">33 30 33 30 33 32 32 44</span></span>
  
<span data-ttu-id="a70b2-113">33 30 33 30 33 31 32 44</span><span class="sxs-lookup"><span data-stu-id="a70b2-113">33 30 33 30 33 31 32 44</span></span>
  
<span data-ttu-id="a70b2-114">33 30 35 33 33 37 35 33</span><span class="sxs-lookup"><span data-stu-id="a70b2-114">33 30 35 33 33 37 35 33</span></span>
  
<span data-ttu-id="a70b2-115">33 41 33 41 33 39 33 36</span><span class="sxs-lookup"><span data-stu-id="a70b2-115">33 41 33 41 33 39 33 36</span></span>
  
<span data-ttu-id="a70b2-116">33 30 33 36 33 31 33 31</span><span class="sxs-lookup"><span data-stu-id="a70b2-116">33 30 33 36 33 31 33 31</span></span>
  
<span data-ttu-id="a70b2-117">32 44 33 31 33 35 33 33</span><span class="sxs-lookup"><span data-stu-id="a70b2-117">32 44 33 31 33 35 33 33</span></span>
  
<span data-ttu-id="a70b2-118">33 37 33 30 33 30 00</span><span class="sxs-lookup"><span data-stu-id="a70b2-118">33 37 33 30 33 30 00</span></span>
  
<span data-ttu-id="a70b2-119">この手法は、Microsoft Exchange Server X. 400 コネクタによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="a70b2-119">This technique is used by the Microsoft Exchange Server X.400 Connector.</span></span> <span data-ttu-id="a70b2-120">この手法は、相互運用性を最大にするために Microsoft Exchange Server に接続するすべての X. 400 ゲートウェイおよびトランスポートで使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a70b2-120">This technique should be used by any X.400 gateways and transports that connect to Microsoft Exchange Server in order to maximize interoperability.</span></span>
  
<span data-ttu-id="a70b2-121">Microsoft のソフトウェアと共に今後の互換性を維持するために、IM_THIS_IPM の PR_TNEF_CORRELATION_KEY 属性も\*\*\*\* ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) プロパティにコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a70b2-121">For greatest compatibility with future as well as present Microsoft software, the IM_THIS_IPM X.400 attribute should also be copied to the **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) property.</span></span> <span data-ttu-id="a70b2-122">ただし、 **PR_TNEF_CORRELATION_KEY**はバイナリプロパティであるため、16進数文字列への変換は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="a70b2-122">However, since **PR_TNEF_CORRELATION_KEY** is a binary property, no translation into a hexadecimal string is necessary.</span></span> 
  

