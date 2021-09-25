---
title: attSentFor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: aa8c8d64-d2a0-4cdf-a8aa-21c8d0a0a3fc
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e78fe61824984ab61a9b12fcc4866bc91848be79
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605147"
---
# <a name="attsentfor"></a>attSentFor

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**attSentFor** 属性は、エンドツーエンドに配置されたカウントされた文字列としてエンコードされます。 **attSentFor の形式は** 次のとおりです。 
  
 **attSentFor**: 
  
> display-name-length display-name address-length  _email-address_
    
 _電子メール アドレス_
  
> type **:** address 
    
他の長さの値とは異なり、表示名の長さとアドレスの長さは、符号なし長整数ではなく、符号なし 16 ビットの値です。 ただし、null 文字の終端は引き続き含まれます。 電子メール アドレス エントリ内の型とアドレスの文字列は、リテラルコロン (:)"smtp:joe@nowhere.com" などの文字。 結合された型 **: アドレス** 文字列だけが null 終端です。
  

