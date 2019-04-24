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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318159"
---
# <a name="attfrom"></a>attFrom

**適用対象**: Outlook 2013 | Outlook 2016 
  
この**** 属性は、送信者の表示名と電子メールアドレス、送信者の表示名とアドレス、および必要なスペースをエンコードする**trp**構造体としてエンコードされます。 **添付**ファイルの形式は次のとおりです。 
  
**添付元**: _trp 構造_送信者-表示名 _ 送信者-アドレス _ padding 
    
送信者の表示名は、null で終了する文字列で、必要に応じて2バイト境界になるまで、追加の null 文字が埋め込まれます。 **添付**文字の末尾のスペースは、 **sizeof (trp)** 境界に到達するために必要な数の null 文字で構成されます。 
  
_trp 構造:_**trpidOneOff** cbgrtrp cch cb 
    
[**添付**] アイテムの場合、 **trp**構造は常に1回限りのエンコードであるため、trp 構造**** フィールドからの trp は常に**trpidOneOff**になります。 cbgrtrp、cch、および cb の各項目は、 **trp**構造体の残りのフィールドに対応しています。 
  
cbgrtrp フィールドは、合計 **(sizeof (trp) \*2)**、null で終了する送信者の表示名の長さと、null で終了する送信者のアドレスの長さとして計算されます。
  
cch フィールドは、スペースを含む null で終わる表示名の長さとして計算されます。
  
cb フィールドは、null で終了する送信者アドレスの長さとして計算されます。
  
_sender-address:_ address-type **:** address **' \ 0 '**
    
送信者のアドレスは、アドレスの種類、リテラルのコロン (:)、アドレス自体、終端の null 文字で構成される、4つの部分で構成される文字列です。 たとえば、文字列`fax:1-909-555-1234\0`は法的な送信者アドレスの値になります。
  

