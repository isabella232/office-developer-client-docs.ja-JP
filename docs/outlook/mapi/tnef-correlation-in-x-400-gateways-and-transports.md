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
# <a name="tnef-correlation-in-x400-gateways-and-transports"></a>X.400 ゲートウェイとトランスポートの TNEF 相関

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
X.400 ベースのシステムに接続するゲートウェイとトランスポートは、IM_THIS_IPM X.400 属性の値と **attMessageID** TNEF 属性を使用して TNEF 相関を実装します。 
  
送信メッセージの IM_THIS_IPM 属性の値は、TNEF ストリームの **attMessageID** にコピーされます。 X.400 属性IM_THIS_IPM通常は文字列ですが **、attMessageID** TNEF 属性はバイナリ値を表す 16 進数の文字列です。 したがって、IM_THIS_IPM X.400 属性の各文字 (終端の null 文字を含む) は、その文字の ASCII 値を表す 2 文字の 16 進文字列に変換する必要があります。 たとえば、X.400 IM_THIS_IPM属性が次の文字列である場合。 
  
3030322D3030312D305337533A3A3A3936303631312D313533373030
  
**attMessageID の値は**、次の 16 進数字のシーケンスになります。 
  
33 30 33 30 33 32 32 44
  
33 30 33 30 33 31 32 44
  
33 30 35 33 33 37 35 33
  
33 41 33 41 33 39 33 36
  
33 30 33 36 33 31 33 31
  
32 44 33 31 33 35 33 33
  
33 37 33 30 33 30 00
  
この手法は、X.400 コネクタMicrosoft Exchange Server使用します。 この手法は、相互運用性を最大限に高めるには、Microsoft Exchange Server X.400 ゲートウェイとトランスポートで使用する必要があります。
  
将来および現在の Microsoft ソフトウェアとの最大の互換性のために、IM_THIS_IPM X.400 属性も **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) プロパティにコピーする必要があります。 ただし **、PR_TNEF_CORRELATION_KEY** はバイナリ プロパティですから、16 進文字列への変換は必要ありません。 
  

