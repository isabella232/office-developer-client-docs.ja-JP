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
  
属性**の添付文**は、エンドツーエンドで配置された文字列のカウントとしてエンコードされます。 **添付**ファイルの形式は次のとおりです。 
  
 **添付の対象**: 
  
> 表示名-長さの表示-名前アドレスの長さの_電子メールアドレス_
    
 _電子メールアドレス_
  
> 型 **:** address 
    
他の長さの値とは異なり、表示名の長さとアドレスの長さは、符号なしの長い整数ではなく、符号なしの16ビットの値になります。 ただし、終端の null 文字はそのまま残ります。 _電子メールアドレス_エントリの type および address 文字列は、リテラルのコロン (:) で区切られています。文字 ("smtp:joe@nowhere.com" など)。 結合された型 **:** address 文字列は null で終了します。
  

