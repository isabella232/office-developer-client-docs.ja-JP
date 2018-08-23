---
title: attSentFor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aa8c8d64-d2a0-4cdf-a8aa-21c8d0a0a3fc
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b292e65ddabcbe052832687a3dcf01658de5e379
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567476"
---
# <a name="attsentfor"></a>attSentFor

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
**AttSentFor**属性は、文字列の配置のエンド ・ ツー ・ エンドのようにエンコードされます。 **AttSentFor**の形式は次のとおりです。 
  
 **attSentFor**。 
  
> _電子メール アドレス_の表示名のアドレスと長さの表示名の長さ
    
 _電子メール アドレス_
  
> **::** の種類のアドレス 
    
その他の長さとは異なり値、表示名の長さ、およびアドレスの長さは、符号なし長整数ではなく符号なしの 16 ビット値です。 ただし終端の null 文字の場合は、それらも含まれます。 _電子メール アドレス_のエントリの種類とアドレスの文字列は、"smtp:joe@nowhere.com"などのリテラル コロン (:) 文字で区切られます。 のみ、組み合わされた型 **::** アドレス文字列には null で終わるです。
  

