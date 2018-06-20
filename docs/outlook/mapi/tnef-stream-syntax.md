---
title: TNEF ストリームの構文
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1353d494-c266-4715-afe7-14543a1bbe1b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: cbaf37415608dd1d79a06be65b34632f2b4afc89
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804133"
---
# <a name="tnef-stream-syntax"></a>TNEF ストリームの構文

  
  
**適用されます**: Outlook 
  
TNEF ストリームの構文の説明のような Bakus ・ Nauer をここに示します。 この説明では、斜体文字で終端要素をさらに定義を持ちます。 定数とリテラルの項目は、太字で。 要素のシーケンスは、1 つの行に順に並んでいます。 たとえば、_ストリーム_の項目は、定数**TNEF_SIGNATURE**、_キー_、_オブジェクト_の後に続くので構成されます。 アイテムに複数の可能な実装がある場合は、連続する行の代替案のとおりです。 たとえば、_オブジェクト_は、 _Message_Seq_、 _Message_Seq_ _Attach_Seq_、または単に_Attach_Seq_に続くので構成できます。
  
 _TNEF_Stream。_
  
> **TNEF_SIGNATURE**_キー__オブジェクト_
    
 _キー:_
  
> 0 以外の値を 16 ビット符号なし整数
    
TNEF を有効になっているトランスポートは、TNEF の実装を使用して、TNEF ストリームを生成する前にこの値を生成します。
  
 _オブジェクト:_
  
>  _Message_Seq Message_Seq Attach_Seq Attach_Seq_
    
 _Message_Seq。_
  
>  _attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_
    
 _attTnefVersion。_
  
> **LVL_MESSAGE attTnefVersion sizeof(ULONG)****0x00010000**チェックサム 
    
 _attMessageClass。_
  
> **LVL_MESSAGE attMessageClass**_msg_class_length msg_class_チェックサム 
    
 _Msg_Attribute_Seq。_
  
>  _Msg_Attribute Msg_Attribute Msg_Attribute_Seq_
    
 _Msg_Attribute。_
  
> **LVL_MESSAGE**属性 ID の属性の長さの属性データのチェックサム 
    
属性 ID は、TNEF 属性識別子の**attSubject**などの 1 つです。 属性の長さは、属性データの長さ (バイト単位) です。 属性データは、属性に関連付けられているデータです。
  
 _Attach_Seq。_
  
>  _attRenddata attRenddata Att_Attribute_Seq_
    
 _attRenddata。_
  
> **LVL_ATTACHMENT attRenddata****sizeof(RENDDATA)** renddata のチェックサム 
    
Renddata は、対応する添付ファイルのレンダリング情報を格納する**RENDDATA**構造体に関連付けられているデータです。 **RENDDATA**構造体は、TNEF で定義されます。H ヘッダー ファイルです。 
  
 _Att_Attribute_Seq。_
  
>  _Att_Attribute Att_Attribute Att_Attribute_Seq_
    
 _Att_Attribute。_
  
> **LVL_ATTACHMENT**属性 ID の属性の長さの属性データのチェックサム 
    
属性 ID、属性の長さ、および属性データは、Msg_Attribute の項目の場合と同じの意味を持ちます。
  

