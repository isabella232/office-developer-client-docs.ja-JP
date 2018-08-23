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
ms.openlocfilehash: fd7f79ad7a36fd174bf9817ff463b00e6a334104
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799739"
---
# <a name="attsentfor"></a>attSentFor

  
  
**適用対象**: Outlook 
  
**AttSentFor**属性は、文字列の配置のエンド ・ ツー ・ エンドのようにエンコードされます。 **AttSentFor**の形式は次のとおりです。 
  
 **attSentFor**。 
  
> _電子メール アドレス_の表示名のアドレスと長さの表示名の長さ
    
 _電子メール アドレス_
  
> **::** の種類のアドレス 
    
その他の長さとは異なり値、表示名の長さ、およびアドレスの長さは、符号なし長整数ではなく符号なしの 16 ビット値です。 ただし終端の null 文字の場合は、それらも含まれます。 _電子メール アドレス_のエントリの種類とアドレスの文字列は、"smtp:joe@nowhere.com"などのリテラル コロン (:) 文字で区切られます。 のみ、組み合わされた型 **::** アドレス文字列には null で終わるです。
  

