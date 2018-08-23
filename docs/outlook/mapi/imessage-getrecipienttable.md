---
title: IMessageGetRecipientTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.GetRecipientTable
api_type:
- COM
ms.assetid: a335dfca-44da-452e-b16f-25d314b1758f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 90ae9cee915296475d7fe64952b40ab7344e89e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800890"
---
# <a name="imessagegetrecipienttable"></a>IMessage::GetRecipientTable

  
  
**適用対象**: Outlook 
  
メッセージの受信者テーブルを取得します。
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]テーブルの戻り値を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_DEFERRED_ERRORS 
  
> 正常に戻す、可能性のあるテーブルが呼び出し側のクライアントに完全に使用する前に**GetRecipientTable**を使用できます。 テーブルが使用できない場合は、それ以降の呼び出しを行うとエラーが発生することができます。 
    
MAPI_UNICODE 
  
> 文字列型の列は、Unicode 形式である必要があります。 MAPI_UNICODE フラグが設定されていない場合、ANSI 形式の文字列の列を引き起こすことがあります。
    
 _lppTable_
  
> [out]受信者テーブルへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 受信者テーブルが正常に返されました。
    
## <a name="remarks"></a>注釈

**IMessage::GetRecipientTable**メソッドは、すべてのメッセージの受信者に関する情報を含むメッセージの受信者テーブルへのポインターを返します。 すべての受信者の 1 つの行があります。 
  
受信者テーブルには、メッセージが送信されたかどうかに応じて、設定の異なる列があります。 受信者テーブルの各列の一覧は、[受信者テーブル](recipient-tables.md)を参照してください。
  
いくつかの受信者テーブルのサポートまで、さまざまな制限です。そうでないです。 制限のサポートは、メッセージ ストア プロバイダーの実装に依存します。 
  
_UlFlags_パラメーターに MAPI_UNICODE フラグを設定する受信者テーブルには、次の呼び出しに影響します。 
  
- 列を取得する[IMAPITable::QueryColumns](imapitable-querycolumns.md)を設定します。 
    
- [IMAPITable::QueryRows](imapitable-queryrows.md)の行を取得します。 
    
- 並べ替え順序を取得するために[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)をします。 
    
これらの呼び出しから返される文字列の列の情報は、Unicode 形式である Unicode フラグの要求を設定します。 ただし、Unicode をサポートしていないすべてのメッセージ ストア プロバイダーであるためこのフラグを設定、のみ要求です。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

受信者テーブルが開いている間、 [IMessage::ModifyRecipients](imessage-modifyrecipients.md)メソッドを呼び出すことによって変更できます。 **ModifyRecipients**の受信者を追加するには、受信者を削除または受信者のプロパティを変更します。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

