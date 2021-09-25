---
title: attOwner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3c6a4050-fd97-42ce-abb1-118254b367bd
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d9f0254b275ea0245360eba39c249139e7b33288
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572110"
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
  

