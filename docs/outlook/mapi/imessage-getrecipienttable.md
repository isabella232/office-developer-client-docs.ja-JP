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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ca42e91528cdb7e61ae3620989c4a89966db1061
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424610"
---
# <a name="imessagegetrecipienttable"></a>IMessage::GetRecipientTable

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの recipient テーブルを返します。
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番テーブルの戻り値を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DEFERRED_ERRORS 
  
> 呼び出し元のクライアントがテーブルを完全に使用できるようになる前に、 **getrecipienttable**を正常に返すことができるようにします。 テーブルを使用できない場合は、その後の呼び出しを行うとエラーが発生する可能性があります。 
    
MAPI_UNICODE 
  
> 文字列列は、Unicode 形式である必要があります。 MAPI_UNICODE フラグが設定されていない場合、文字列列は ANSI 形式である必要があります。
    
 _lpptable_
  
> 読み上げ受信者テーブルへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 受信者テーブルが正常に返されました。
    
## <a name="remarks"></a>注釈

**IMessage:: get table**メソッドは、メッセージの受信者テーブルへのポインターを返します。これには、メッセージのすべての受信者に関する情報が含まれています。 すべての受信者に1つの行があります。 
  
受信者テーブルは、メッセージが送信されたかどうかに応じて異なる列セットを持ちます。 受信者テーブルの列の完全な一覧については、「 [recipient Tables](recipient-tables.md)」を参照してください。
  
一部の受信者テーブルでは、さまざまな制限がサポートしています。それ以外の場合は含まれません。 制限のサポートは、メッセージストアプロバイダーの実装によって異なります。 
  
_ulflags_パラメーターの MAPI_UNICODE フラグを設定すると、受信者テーブルへの次の呼び出しに影響します。 
  
- [IMAPITable:: querycolumns](imapitable-querycolumns.md)は、列セットを取得します。 
    
- [IMAPITable:: QueryRows](imapitable-queryrows.md)が行を取得します。 
    
- [IMAPITable:: querysortorder](imapitable-querysortorder.md)は、並べ替えの順序を取得します。 
    
unicode フラグを設定すると、これらの呼び出しから返される文字列列の情報は unicode 形式になります。 ただし、すべてのメッセージストアプロバイダーが Unicode をサポートしているわけではないため、このフラグの設定は要求だけになります。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

[IMessage:: modifyrecipients](imessage-modifyrecipients.md)メソッドを呼び出すことによって、受信者テーブルを開いたまま変更することができます。 **modifyrecipients**受信者の追加、受信者の削除、または受信者のプロパティの変更を行います。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

