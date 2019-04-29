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
  
メッセージのトランスポート中立カプセル化形式 (TNEF) データストリームで、メッセージの受信者テーブルのビューをエンコードします。
  
```cpp
HRESULT EncodeRecips(
  ULONG ulFlags,
  LPMAPITABLE lpRecipientTable
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lp受信者テーブル_
  
> 順番ビューがエンコードされている受信者テーブルへのポインター。 _lp受信者テーブル_パラメーターは NULL にすることができます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが成功し、予想される値または値が返されました。
    
## <a name="remarks"></a>注釈

トランスポートプロバイダー、メッセージストアプロバイダー、およびゲートウェイは、 **ITnef:: EncodeRecips**メソッドを呼び出して、特定の受信者テーブルビューの TNEF エンコードを実行します。 TNEF エンコードは、たとえばプロバイダーまたはゲートウェイで、特定の列セット、並べ替え順序、または受信者テーブルの制限が必要な場合などに便利です。 
  
プロバイダーまたはゲートウェイは、 _lp受信者テーブル_パラメーターでエンコードされるテーブルビューを渡します。 TNEF 実装は、指定された列セット、並べ替え順序、制限、および位置を使用して、指定されたビューで受信者テーブルをエンコードします。 _lprecipient テーブル_でプロバイダーまたはゲートウェイが NULL になると、tnef は[IMessage:: get table](imessage-getrecipienttable.md)メソッドを使用してエンコードされているメッセージから受信者テーブルを取得し、次のコードを使用して、テーブルの各行をすべて TNEF ストリームに処理します。表の現在の設定。 
  
_lprecipienttable_で NULL で**EncodeRecips**を呼び出すと、すべてのメッセージの受信者がエンコードされ、 _ulflags_パラメーターと PR_ で TNEF_PROP_INCLUDE フラグを使用して[ITnef:: addprops](itnef-addprops.md)メソッドを呼び出すことと同じになります。 **** _lpproplist_パラメーターの MESSAGE_RECIPIENTS ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) プロパティ。 
  
特定の受信者テーブルビューをエンコードする必要がある場合を除き、 **EncodeRecips**を呼び出す必要はほとんどありません。 外部メッセージングシステムには、受信者の一覧をエンコードする一般的な要件を十分に処理できる、多くの場合、受信者の一覧を処理する機能が用意されています。そのため、これらのシステムは、この目的のために TNEF を必要としません。 
  
## <a name="see-also"></a>関連項目



[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[ITnef::AddProps](itnef-addprops.md)
  
[PidTagMessageRecipients 標準プロパティ](pidtagmessagerecipients-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

