---
title: IMessageGetRecipientTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMessage.GetRecipientTable
api_type:
- COM
ms.assetid: a335dfca-44da-452e-b16f-25d314b1758f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 466e0e8d5adee88b8e6a7d1b70c79bf075310cb0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610511"
---
# <a name="imessagegetrecipienttable"></a>IMessage::GetRecipientTable

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの受信者テーブルを返します。
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]テーブルの戻り値を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DEFERRED_ERRORS 
  
> **テーブルが呼び出** し元のクライアントで完全に使用できる前に、GetRecipientTable が正常に返されるのを許可します。 テーブルが使用できない場合は、後続の呼び出しでエラーが発生する可能性があります。 
    
MAPI_UNICODE 
  
> 文字列列は Unicode 形式である必要があります。 このフラグMAPI_UNICODE設定しない場合、文字列列は ANSI 形式である必要があります。
    
 _lppTable_
  
> [out]受信者テーブルへのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 受信者テーブルが正常に返されました。
    
## <a name="remarks"></a>注釈

**IMessage::GetRecipientTable** メソッドは、メッセージのすべての受信者に関する情報を含む、メッセージの受信者テーブルへのポインターを返します。 受信者ごとに 1 行があります。 
  
受信者テーブルの列セットは、メッセージが送信されたかどうかによって異なります。 受信者テーブル内の列の完全な一覧については、「受信者テーブル」 [を参照してください](recipient-tables.md)。
  
一部の受信者テーブルでは、さまざまな制限がサポートされています。他のユーザーはそうではありません。 制限のサポートは、メッセージ ストア プロバイダーの実装によって異なります。 
  
_ulFlags_ パラメーター MAPI_UNICODEフラグを設定すると、受信者テーブルへの次の呼び出しに影響します。 
  
- [列セットを取得する IMAPITable::QueryColumns。](imapitable-querycolumns.md) 
    
- [IMAPITable::QueryRows を使用して行](imapitable-queryrows.md) を取得します。 
    
- [並べ替え順序を取得する IMAPITable::QuerySortOrder。](imapitable-querysortorder.md) 
    
Unicode フラグを設定すると、これらの呼び出しから返される文字列列の情報を Unicode 形式で指定する必要があります。 ただし、すべてのメッセージ ストア プロバイダーが Unicode をサポートしているわけではありませんので、このフラグの設定は要求のみです。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

[IMessage::ModifyRecipients](imessage-modifyrecipients.md)メソッドを呼び出すことによって、受信者テーブルを開いている間に変更できます。 **ModifyRecipients は** 、受信者の追加、受信者の削除、または受信者のプロパティの変更を行います。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

