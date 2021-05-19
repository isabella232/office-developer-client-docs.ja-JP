---
title: attOwner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c6a4050-fd97-42ce-abb1-118254b367bd
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 17e900ac28481388379133a95b4b206ca4bc1805
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427655"
---
# <a name="attowner"></a>attOwner

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**attOwner 属性** は、エンドツーエンドに配置されたカウントされた文字列としてエンコードされます。 **attOwner の形式は** 次のとおりです。 
  
 **attOwner**: 
  
> display-name-length display-name address-length  _email-address_
    
 _電子メール アドレス_
  
> type **:** address 
    
他の長さの値とは異なり、表示名の長さとアドレスの長さは、符号なし長整数ではなく、符号なし 16 ビットの値です。 ただし、null 文字の終端は引き続き含まれます。 電子メール アドレス エントリ内の型とアドレスの文字列は、リテラルコロン (:)"smtp:joe@nowhere.com" などの文字。 結合された型 **: アドレス** 文字列だけが null 終端です。
  
MAPI プロパティと **attOwner** 属性のマッピングは、エンコードされるメッセージのメッセージ クラスによって異なります。 
  

