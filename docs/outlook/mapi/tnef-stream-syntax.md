---
title: TNEF ストリーム構文
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 1353d494-c266-4715-afe7-14543a1bbe1b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 841404f5f7cb13fadd964f13174dc25c493e0015
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609328"
---
# <a name="tnef-stream-syntax"></a>TNEF ストリーム構文

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは、TNEF ストリームBakus-Nauer説明のような方法について説明します。 この説明では、それ以上の定義を持つ非ターミニナル要素が italics に含まれています。 定数とリテラル項目は太字です。 要素のシーケンスは、1 行に順番に一覧表示されます。 たとえば _、Stream_ アイテムは定数の値TNEF_SIGNATUREキー 、続いて Object で構成 _されます_。  アイテムに複数の実装が可能な場合、代替案は連続した行に一覧表示されます。 たとえば、_オブジェクト_ は、オブジェクト、Message_Seq、Message_Seq、Attach_Seq、または単なるAttach_Seq _で構成Attach_Seq。_  
  
 _TNEF_Stream:_
  
> **TNEF_SIGNATURE**_キー_ _オブジェクト_
    
 _キー:_
  
> 0 以外の 16 ビット符号なし整数
    
TNEF が有効なトランスポートは、TNEF 実装を使用して TNEF ストリームを生成する前に、この値を生成します。
  
 _オブジェクト:_
  
>  _Message_Seq Message_Seq Attach_Seq Attach_Seq_
    
 _Message_Seq:_
  
>  _attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_
    
 _attTnefVersion:_
  
> **LVL_MESSAGE attTnefVersion sizeof(ULONG) 0x00010000****チェックサム** 
    
 _attMessageClass:_
  
> **LVL_MESSAGE attMessageClass** _msg_class_length msg_class_ チェックサム 
    
 _Msg_Attribute_Seq:_
  
>  _Msg_Attribute Msg_Attribute Msg_Attribute_Seq_
    
 _Msg_Attribute:_
  
> **LVL_MESSAGE-ID** 属性長属性データ チェックサム 
    
属性 ID は **、attSubject** などの TNEF 属性識別子の 1 つです。 属性の長さは、属性データのバイト単位の長さです。 属性データは、属性に関連付けられたデータです。
  
 _Attach_Seq:_
  
>  _attRenddata attRenddata Att_Attribute_Seq_
    
 _attRenddata:_
  
> **LVL_ATTACHMENT attRenddata** **sizeof(RENDDATA) renddata** チェックサム 
    
Renddata は、対応する添付ファイルのレンダリング情報を含む **RENDDATA** 構造体に関連付けられたデータです。 **RENDDATA 構造** は TNEF で定義されます。H ヘッダー ファイル。 
  
 _Att_Attribute_Seq:_
  
>  _Att_Attribute Att_Attribute Att_Attribute_Seq_
    
 _Att_Attribute:_
  
> **LVL_ATTACHMENT-ID** 属性長属性データ チェックサム 
    
属性 ID、属性の長さ、および属性データは、属性アイテムと同Msg_Attributeです。
  

