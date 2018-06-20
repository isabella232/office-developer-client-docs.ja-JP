---
title: attOwner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c6a4050-fd97-42ce-abb1-118254b367bd
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0cb40c3c644618bdf65a2c90a91580a5be8fc88c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799719"
---
# <a name="attowner"></a>attOwner

  
  
**適用されます**: Outlook 
  
**AttOwner**属性は、文字列の配置のエンド ・ ツー ・ エンドのようにエンコードされます。 **AttOwner**の形式は次のとおりです。 
  
 **attOwner**。 
  
> _電子メール アドレス_の表示名のアドレスと長さの表示名の長さ
    
 _電子メール アドレス_
  
> **::** の種類のアドレス 
    
その他の長さとは異なり値、表示名の長さ、およびアドレスの長さは、符号なし長整数ではなく符号なしの 16 ビット値です。 ただし終端の null 文字の場合は、それらも含まれます。 _電子メール アドレス_のエントリの種類とアドレスの文字列は、"smtp:joe@nowhere.com"などのリテラル コロン (:) 文字で区切られます。 のみ、組み合わされた型 **::** アドレス文字列には null で終わるです。
  
**AttOwner**属性に、MAPI プロパティのマッピングは、エンコードされているメッセージのメッセージ クラスに依存します。 
  

