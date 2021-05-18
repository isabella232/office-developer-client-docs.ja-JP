---
title: X.400 ゲートウェイとトランスポートの TNEF 相関
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
# <a name="tnef-correlation-in-x400-gateways-and-transports"></a><span data-ttu-id="db007-103">X.400 ゲートウェイとトランスポートの TNEF 相関</span><span class="sxs-lookup"><span data-stu-id="db007-103">TNEF Correlation in X.400 Gateways and Transports</span></span>

  
  
<span data-ttu-id="db007-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db007-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db007-105">X.400 ベースのシステムに接続するゲートウェイとトランスポートは、IM_THIS_IPM X.400 属性の値と **attMessageID** TNEF 属性を使用して TNEF 相関を実装します。</span><span class="sxs-lookup"><span data-stu-id="db007-105">Gateways and transports that connect to X.400-based systems, use the value of the IM_THIS_IPM X.400 attribute and the **attMessageID** TNEF attribute to implement TNEF correlation.</span></span> 
  
<span data-ttu-id="db007-106">送信メッセージの IM_THIS_IPM 属性の値は、TNEF ストリームの **attMessageID** にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="db007-106">The value of the IM_THIS_IPM attribute of the outbound message is copied to **attMessageID** in the TNEF stream.</span></span> <span data-ttu-id="db007-107">X.400 属性IM_THIS_IPM通常は文字列ですが **、attMessageID** TNEF 属性はバイナリ値を表す 16 進数の文字列です。</span><span class="sxs-lookup"><span data-stu-id="db007-107">The IM_THIS_IPM X.400 attribute is typically a string, while the **attMessageID** TNEF attribute is a string of hexadecimal digits representing a binary value.</span></span> <span data-ttu-id="db007-108">したがって、IM_THIS_IPM X.400 属性の各文字 (終端の null 文字を含む) は、その文字の ASCII 値を表す 2 文字の 16 進文字列に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="db007-108">Therefore, each character in the IM_THIS_IPM X.400 attribute, including the terminating null character, must be converted to a 2-character hexadecimal string representing the ASCII value of that character.</span></span> <span data-ttu-id="db007-109">たとえば、X.400 IM_THIS_IPM属性が次の文字列である場合。</span><span class="sxs-lookup"><span data-stu-id="db007-109">For instance, if the IM_THIS_IPM X.400 attribute is the following string:</span></span> 
  
<span data-ttu-id="db007-110">3030322D3030312D305337533A3A3A3936303631312D313533373030</span><span class="sxs-lookup"><span data-stu-id="db007-110">3030322D3030312D305337533A3A3936303631312D313533373030</span></span>
  
<span data-ttu-id="db007-111">**attMessageID の値は**、次の 16 進数字のシーケンスになります。</span><span class="sxs-lookup"><span data-stu-id="db007-111">then the value of **attMessageID** would be the following sequence of hexadecimal digits:</span></span> 
  
<span data-ttu-id="db007-112">33 30 33 30 33 32 32 44</span><span class="sxs-lookup"><span data-stu-id="db007-112">33 30 33 30 33 32 32 44</span></span>
  
<span data-ttu-id="db007-113">33 30 33 30 33 31 32 44</span><span class="sxs-lookup"><span data-stu-id="db007-113">33 30 33 30 33 31 32 44</span></span>
  
<span data-ttu-id="db007-114">33 30 35 33 33 37 35 33</span><span class="sxs-lookup"><span data-stu-id="db007-114">33 30 35 33 33 37 35 33</span></span>
  
<span data-ttu-id="db007-115">33 41 33 41 33 39 33 36</span><span class="sxs-lookup"><span data-stu-id="db007-115">33 41 33 41 33 39 33 36</span></span>
  
<span data-ttu-id="db007-116">33 30 33 36 33 31 33 31</span><span class="sxs-lookup"><span data-stu-id="db007-116">33 30 33 36 33 31 33 31</span></span>
  
<span data-ttu-id="db007-117">32 44 33 31 33 35 33 33</span><span class="sxs-lookup"><span data-stu-id="db007-117">32 44 33 31 33 35 33 33</span></span>
  
<span data-ttu-id="db007-118">33 37 33 30 33 30 00</span><span class="sxs-lookup"><span data-stu-id="db007-118">33 37 33 30 33 30 00</span></span>
  
<span data-ttu-id="db007-119">この手法は、X.400 コネクタMicrosoft Exchange Server使用します。</span><span class="sxs-lookup"><span data-stu-id="db007-119">This technique is used by the Microsoft Exchange Server X.400 Connector.</span></span> <span data-ttu-id="db007-120">この手法は、相互運用性を最大限に高めるには、Microsoft Exchange Server X.400 ゲートウェイとトランスポートで使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="db007-120">This technique should be used by any X.400 gateways and transports that connect to Microsoft Exchange Server in order to maximize interoperability.</span></span>
  
<span data-ttu-id="db007-121">将来および現在の Microsoft ソフトウェアとの最大の互換性のために、IM_THIS_IPM X.400 属性も **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) プロパティにコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="db007-121">For greatest compatibility with future as well as present Microsoft software, the IM_THIS_IPM X.400 attribute should also be copied to the **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) property.</span></span> <span data-ttu-id="db007-122">ただし **、PR_TNEF_CORRELATION_KEY** はバイナリ プロパティですから、16 進文字列への変換は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="db007-122">However, since **PR_TNEF_CORRELATION_KEY** is a binary property, no translation into a hexadecimal string is necessary.</span></span> 
  

