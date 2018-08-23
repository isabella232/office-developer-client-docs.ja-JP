---
title: attFrom
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2d405268-bb33-4863-be38-2d17e8fc956e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c7c0d1df32a0ad6359fad20128a6a1e3dd225143
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799725"
---
# <a name="attfrom"></a>attFrom

**適用対象**: Outlook 
  
**AttFrom**属性は、表示名と、必要なスペースの後に、送信者のアドレスの後に、送信者の表示名と電子メール アドレスをエンコードする**TRP**構造体としてエンコードされます。 **AttFrom**の形式は次のとおりです。 
  
**attFrom**: 送信者の表示名 _ 送信者アドレス _ パディングの_TRP 構造_ 
    
送信者の表示名では、null で終わる文字列を null 文字を追加、必要に応じて、2 バイト境界に到達します。 **AttFrom**エンコーディングの末尾のスペースは、 **sizeof(TRP)** の境界に到達するために必要な null 文字で構成されます。 
  
_TRP 構造:_**trpidOneOff** cbgrtrp cch cb 
    
**AttFrom**アイテム、 **TRP**の-構造体は常に、1 回限りのエンコーディングをそのため**TRP**から trpid の構造体のフィールドは、常に**trpidOneOff**。 Cbgrtrp や cch、cb の項目は、 **TRP**の構造体の残りのフィールドに対応します。 
  
Cbgrtrp フィールドは、の合計として計算 **(sizeof(TRP) \*2)** の null で終わる送信者の表示名、パディング、長さ、null で終端された送信者のアドレスの長さ。
  
Cch フィールドは、そのスペースを持つ null で終わる表示名の長さとして計算されます。
  
Cb フィールドは、null で終端された送信者のアドレスの長さとして計算されます。
  
_送信者アドレス:_ **::** のアドレスの種類 **'\0'** を解決します。
    
送信者アドレスは、4 つの部分、アドレスの種類が、リテラルのコロン (:)、アドレス自体、および終端の null 文字で構成される文字列です。 文字列では、 `fax:1-909-555-1234\0` 、有効な送信者アドレスの値になります。
  

