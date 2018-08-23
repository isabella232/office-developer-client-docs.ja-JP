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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 6324dcc567aee48f190f8568c6c94b5ee87c731f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584568"
---
# <a name="itnefencoderecips"></a>ITnef::EncodeRecips

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージのトランスポート ニュートラル カプセル化形式 (TNEF) データ ストリーム内のメッセージの受信者テーブルのビューをエンコードします。
  
```cpp
HRESULT EncodeRecips(
  ULONG ulFlags,
  LPMAPITABLE lpRecipientTable
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpRecipientTable_
  
> [in]ビューがエンコードされている受信者テーブルへのポインター。 _LpRecipientTable_パラメーターは NULL にできます。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 呼び出しが成功し、予期される値または値が返されます。
    
## <a name="remarks"></a>注釈

プロバイダー、メッセージ ストア プロバイダーでは、TNEF エンコード受信者テーブルの特定のビューを実行するのにはゲートウェイの呼び出し、 **ITnef::EncodeRecips**メソッドを転送します。 TNEF エンコードは便利ですが、たとえば、プロバイダーまたはゲートウェイが必要な場合、特定の列のセット、並べ替え順、または制限、受信者テーブルのです。 
  
プロバイダーまたはゲートウェイは、 _lpRecipientTable_パラメーターでエンコードするテーブルのビューに渡されます。 TNEF の実装では、指定したビューを指定した列のセット、並べ替え順、制限、および位置を使用して受信者テーブルをエンコードします。 場合は、プロバイダーまたはゲートウェイ_lpRecipientTable_に NULL を渡すと、TNEF は、 [IMessage::GetRecipientTable](imessage-getrecipienttable.md)メソッドを使用してエンコードされているメッセージの受信者テーブルを取得し、TNEF ストリームを使用して、テーブルのすべての行を処理しますテーブルの現在の設定です。 
  
_LpRecipientTable_に NULL を使用して**EncodeRecips**を呼び出す、すべてのメッセージ受信者をエンコードし、 _ulFlags_パラメーターと**PR_ に TNEF_PROP_INCLUDE フラグを指定して[ITnef::AddProps](itnef-addprops.md)メソッドを呼び出すことと同じです。MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) のプロパティの_lpPropList_パラメーターにします。 
  
受信者テーブルの特定のビューをエンコードする必要がない限り、 **EncodeRecips**を呼び出すことはほとんど必要があることに注意してください。 外部のメッセージング システムが受信者リストをエンコードの一般的なニーズを処理するのに十分では受信者の一覧を処理するための機能をほぼ常にあります。したがって、これらのシステムでは、この目的のための TNEF ほとんどありませんが必要です。 
  
## <a name="see-also"></a>関連項目



[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[ITnef::AddProps](itnef-addprops.md)
  
[PidTagMessageRecipients 標準プロパティ](pidtagmessagerecipients-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

