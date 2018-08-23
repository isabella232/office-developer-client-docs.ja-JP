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
# <a name="tnef-correlation-in-x400-gateways-and-transports"></a>X.400 ゲートウェイおよびトランスポートでの TNEF 関連付け

  
  
**適用対象**: Outlook 
  
ゲートウェイおよび X.400 ベースのシステムに接続するためのトランスポートは、TNEF の相関関係を実装するために IM_THIS_IPM の X.400 属性および**attMessageID**の TNEF の属性の値を使用します。 
  
TNEF ストリーム内の**attMessageID**には、送信メッセージの IM_THIS_IPM 属性の値がコピーされます。 IM_THIS_IPM の X.400 属性は、通常、文字列、です**attMessageID** TNEF の属性がバイナリ値を表す 16 進数の文字列の中に。 したがって、終端の null 文字を含む、IM_THIS_IPM の X.400 属性内の各文字はその文字の ASCII 値を表す 2 桁の 16 進数文字列に変換しなければなりません。 たとえば、IM_THIS_IPM の X.400 属性が次の文字列である場合。 
  
3030322D3030312D305337533A3A3936303631312D313533373030
  
**attMessageID**の値は、次の一連の 16 進数になります。 
  
33 30 33 33 30 32 32 44
  
33 30 33 33 30 31 32 44
  
33 30 35 33 33 37 35 33
  
33 41 33 41 33 39 33 36
  
33 30 33 36 33 31 33 31
  
32 44 33 33 31 35 33 33
  
33 37 33 30 33 30 00
  
この手法は、Microsoft Exchange Server X.400 コネクタによって使用されます。 X.400 ゲートウェイとの相互運用性を最大化するための Microsoft Exchange Server に接続するためのトランスポートには、このテクニックを使用してください。
  
将来と、現在の Microsoft ソフトウェアとの互換性を最大限に IM_THIS_IPM の X.400 属性もコピーする**PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) のプロパティにします。 ただし、バイナリ プロパティを**PR_TNEF_CORRELATION_KEY**には、16 進数文字列に変換必要はありません。 
  

