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
# <a name="tnef-correlation-in-x400-gateways-and-transports"></a>x.400 ゲートウェイおよびトランスポートでの TNEF 相互関係

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ゲートウェイとトランスポートは、IM_THIS_IPM のシステムに接続します。この場合、TNEF 属性の値を使用して、 **** tnef の関連付けを実装します。 
  
送信メッセージの IM_THIS_IPM 属性の値は、TNEF ストリームの " **** 属性" にコピーされます。 IM_THIS_IPM X. 400 属性は、通常は文字列ですが、 **** 属性はバイナリ値を表す16進数の文字列です。 したがって、IM_THIS_IPM X. 400 属性の各文字 (終端の null 文字を含む) は、その文字の ASCII 値を表す2文字の16進文字列に変換する必要があります。 たとえば、IM_THIS_IPM .x 属性が次の文字列であるとします。 
  
3030322D3030312D305337533A3A3936303631312D313533373030
  
次に、[**添付**] の値は次の16進数値になります。 
  
33 30 33 30 33 32 32 44
  
33 30 33 30 33 31 32 44
  
33 30 35 33 33 37 35 33
  
33 41 33 41 33 39 33 36
  
33 30 33 36 33 31 33 31
  
32 44 33 31 33 35 33 33
  
33 37 33 30 33 30 00
  
この手法は、Microsoft Exchange Server X. 400 コネクタによって使用されます。 この手法は、相互運用性を最大にするために Microsoft Exchange Server に接続するすべての X. 400 ゲートウェイおよびトランスポートで使用する必要があります。
  
Microsoft のソフトウェアと共に今後の互換性を維持するために、IM_THIS_IPM の PR_TNEF_CORRELATION_KEY 属性も**** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) プロパティにコピーする必要があります。 ただし、 **PR_TNEF_CORRELATION_KEY**はバイナリプロパティであるため、16進数文字列への変換は必要ありません。 
  

