---
title: attSentFor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aa8c8d64-d2a0-4cdf-a8aa-21c8d0a0a3fc
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f961348e7be474202273aa97a2922566ef40c3a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408839"
---
# <a name="attsentfor"></a>attSentFor

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**attSentFor** 属性は、エンドツーエンドに配置されたカウントされた文字列としてエンコードされます。 **attSentFor の形式は** 次のとおりです。 
  
 **attSentFor**: 
  
> display-name-length display-name address-length  _email-address_
    
 _電子メール アドレス_
  
> type **:** address 
    
他の長さの値とは異なり、表示名の長さとアドレスの長さは、符号なし長整数ではなく、符号なし 16 ビットの値です。 ただし、null 文字の終端は引き続き含まれます。 電子メール アドレス エントリ内の型とアドレスの文字列は、リテラルコロン (:)"smtp:joe@nowhere.com" などの文字。 結合された型 **: アドレス** 文字列だけが null 終端です。
  

