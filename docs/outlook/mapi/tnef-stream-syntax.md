---
title: TNEF ストリームの構文
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1353d494-c266-4715-afe7-14543a1bbe1b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 12d2a92ff80897456707c7ab8af8f704605c85d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423028"
---
# <a name="tnef-stream-syntax"></a>TNEF ストリームの構文

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは、TNEF ストリームの構文についての、Bakus という名前の説明を示します。 この説明では、さらに詳細が定義されている nonterminal 要素は斜体になっています。 定数とリテラルアイテムは太字で示しています。 要素のシーケンスは、1行に順に表示されます。 たとえば、_ストリーム_アイテムは定数**TNEF_SIGNATURE**で構成され、その後に_キー_が続き、その後に_オブジェクト_が続きます。 アイテムに複数の実装がある場合、選択肢は連続した行に表示されます。 たとえば、_オブジェクト_は、 _Message_Seq_、 _Message_Seq_の後に_Attach_Seq_、または_Attach_Seq_だけで構成できます。
  
 _TNEF_Stream:_
  
> **TNEF_SIGNATURE**_キー__オブジェクト_
    
 _要点_
  
> 0以外の16ビットの符号なし整数
    
tnef が有効なトランスポート tnef の実装を使用して tnef ストリームを生成する前に、この値を生成します。
  
 _対象_
  
>  _Message_Seq Message_Seq Attach_Seq Attach_Seq_
    
 _Message_Seq:_
  
>  _attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion/attTnefVersion/Msg_Attribute_Seq の添付 messageclass Msg_Attribute_Seq Msg_Attribute_Seq_
    
 _attTnefVersion:_
  
> **LVL_MESSAGE attTnefVersion sizeof (ULONG)****0x00010000**チェックサム 
    
 _/添付:_
  
> **LVL_MESSAGE の添付の messageclass**_msg_class_length msg_class_チェックサム 
    
 _Msg_Attribute_Seq:_
  
>  _Msg_Attribute Msg_Attribute Msg_Attribute_Seq_
    
 _Msg_Attribute:_
  
> **LVL_MESSAGE**属性-ID 属性-長さ属性-データチェックサム 
    
属性-ID は、発行されたものなど、TNEF **** 属性識別子の1つです。 属性-length は、属性データの長さ (バイト単位) です。 属性-data は、属性に関連付けられているデータです。
  
 _Attach_Seq:_
  
>  _attRenddata attRenddata Att_Attribute_Seq_
    
 _attRenddata:_
  
> **LVL_ATTACHMENT attRenddata****sizeof (RENDDATA)** RENDDATA チェックサム 
    
Renddata は、対応する添付ファイルのレンダリング情報を含む、 **Renddata**構造に関連付けられているデータです。 **RENDDATA**構造体は TNEF で定義されています。H ヘッダーファイル。 
  
 _Att_Attribute_Seq:_
  
>  _Att_Attribute Att_Attribute Att_Attribute_Seq_
    
 _Att_Attribute:_
  
> **LVL_ATTACHMENT**属性-ID 属性-長さ属性-データチェックサム 
    
属性 ID、属性長、および属性データの意味は、Msg_Attribute item の場合と同じです。
  

