---
title: attFrom
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2d405268-bb33-4863-be38-2d17e8fc956e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 496bd5439b9f004d3b13d2d73b31b5cac3f9eec9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432416"
---
# <a name="attfrom"></a>attFrom

**適用対象**: Outlook 2013 | Outlook 2016 
  
**attFrom** 属性は、送信者の表示名と電子メール アドレスをエンコードし、その後に送信者の表示名とアドレスをエンコードし、その後に必要な埋め込みを行う **TRP** 構造としてエンコードされます。 **attFrom の形式は** 次のとおりです。 
  
**attFrom**: _TRP-structure_ sender-display-name _ sender-address _ padding 
    
sender-display-name は、2 バイト境界に到達するために、必要に応じて追加の null 文字が埋め込まれます。null 終端文字列です。 **attFrom** エンコードの末尾のパディングは **、sizeof(TRP)** 境界に到達するために必要な数の null 文字で構成されます。 
  
_TRP-structure:_ **trpidOneOff** cbgrtrp cch cb 
    
**attFrom** アイテムの **場合、TRP**-structure は常に 1 回限りエンコードなので **、TRP**-structure フィールドの trpid は常に **trpidOneOff** です。 cbgrtrp、cch、cb アイテムは **、TRP** 構造の残りのフィールドに対応します。 
  
cbgrtrp フィールドは、合計 **(sizeof(TRP) \* 2)、** 埋め込み値を持つ null 終端の送信者表示名の長さ、および null 終端の送信者アドレスの長さとして計算されます。
  
cch フィールドは、余白を持つ null 終端表示名の長さとして計算されます。
  
cb フィールドは、null 終端の送信者アドレスの長さとして計算されます。
  
_sender-address:_ address-type **:** address **'\0'**
    
送信者アドレスは、アドレスの種類、リテラルコロン (:)、アドレス自体、および終端の null 文字) の 4 つの部分で構成される文字列です。 たとえば、文字列は `fax:1-909-555-1234\0` 、合法的な送信者アドレス値になります。
  

