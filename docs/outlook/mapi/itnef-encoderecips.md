---
title: ITnefEncodeRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.EncodeRecips
api_type:
- COM
ms.assetid: b3ce4b0e-4f48-4a7e-a30c-c4754bccb12c
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d8caa503e557d35e259db743505d39ea4809dbfd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437652"
---
# <a name="itnefencoderecips"></a>ITnef::EncodeRecips

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージのカプセル化形式 (TNEF) データ ストリームで、Transport-Neutralの受信者テーブルのビューをエンコードします。
  
```cpp
HRESULT EncodeRecips(
  ULONG ulFlags,
  LPMAPITABLE lpRecipientTable
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpRecipientTable_
  
> [in]ビューがエンコードされる受信者テーブルへのポインター。 _lpRecipientTable パラメーター_ には NULL を指定できます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しは成功し、予期される値または値を返しました。
    
## <a name="remarks"></a>注釈

トランスポート プロバイダー、メッセージ ストア プロバイダー、およびゲートウェイは **、ITnef::EncodingRecips** メソッドを呼び出して、特定の受信者テーブル ビューに対して TNEF エンコードを実行します。 TNEF エンコードは、たとえば、プロバイダーまたはゲートウェイが受信者テーブルの特定の列セット、並べ替え順序、または制限を必要とする場合に役立ちます。 
  
プロバイダーまたはゲートウェイは  _、lpRecipientTable_ パラメーターでエンコードされるテーブル ビューを渡します。 TNEF 実装では、指定された列セット、並べ替え順序、制限、および位置を使用して、受信者テーブルを指定したビューでエンコードします。 プロバイダーまたはゲートウェイが  _lpRecipientTable_ で NULL を渡した場合、TNEF は [IMessage::GetRecipientTable](imessage-getrecipienttable.md) メソッドを使用してエンコードされているメッセージから受信者テーブルを取得し、テーブルのすべての行をテーブルの現在の設定を使用して TNEF ストリームに処理します。 
  
_lpRecipientTable_ で NULL を使用して **EncodeRecips** を呼び出すのは、すべてのメッセージ受信者をエンコードするため、ulFlags パラメーターに TNEF_PROP_INCLUDE フラグを指定して [ITnef::AddProps](itnef-addprops.md)メソッドを呼び出し _、lpPropList_ パラメーターで PR_MESSAGE_RECIPIENTS ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) プロパティを呼び出すのと同じです。  
  
特定の受信者テーブル ビューをエンコードする必要がない限り **、EncodeRecips** を呼び出す必要はほとんどありません。 外部メッセージング システムには、受信者リストのエンコードに関する一般的なニーズを処理するのに十分な強力な受信者リストを処理する機能がほとんど常に備わっています。したがって、これらのシステムは、この目的のために TNEF をほとんど必要としません。 
  
## <a name="see-also"></a>関連項目



[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[ITnef::AddProps](itnef-addprops.md)
  
[PidTagMessageRecipients 標準プロパティ](pidtagmessagerecipients-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

