---
title: IMessageGetAttachmentTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.GetAttachmentTable
api_type:
- COM
ms.assetid: e568917e-6085-4094-8728-89ba90a78c40
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9a77d335f3c8980de29dab6e14079c83bd711b43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349274"
---
# <a name="imessagegetattachmenttable"></a>IMessage::GetAttachmentTable

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの添付ファイルテーブルを返します。
  
```cpp
HRESULT GetAttachmentTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番テーブルの作成に関連するフラグのビットマスク。 次のフラグを設定できます。 
    
MAPI_UNICODE 
  
> 文字列列は Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列列は ANSI 形式になります。
    
MAPI_DEFERRED_ERRORS 
  
> 呼び出し元クライアントがテーブルを完全に使用できるようになる前に、 **getattachmenttable**を正常に返すことができるようにします。 テーブルを使用できない場合は、その後の呼び出しを行うとエラーが発生する可能性があります。 
    
 _lpptable_
  
> 読み上げ添付ファイルテーブルへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 添付ファイルテーブルが正常に取得されました。
    
## <a name="remarks"></a>解説

**IMessage:: getattachmenttable**メソッドは、メッセージの添付ファイルテーブルへのポインターを返します。このオブジェクトには、メッセージ内のすべての添付ファイルに関する情報が含まれています。 クライアントは、添付ファイルテーブルを介してのみ添付ファイルにアクセスできます。 添付ファイルの番号を取得することにより、クライアントはいくつかの**IMessage**メソッドを使用して添付ファイルを操作することができます**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティ。 
  
添付ファイルごとに1つの行があります。 添付ファイルテーブルの列の完全な一覧については、「 [attachment Tables](attachment-tables.md)」を参照してください。
  
添付ファイルは、通常、添付ファイルとメッセージが[imapiprop:: SaveChanges](imapiprop-savechanges.md)の呼び出しと共に保存されている限り、添付ファイルテーブルに表示されません。 添付ファイルテーブルは動的です。 クライアントが新しい添付ファイルを作成した場合、既存の添付ファイルを削除した場合、または1つまたは複数のプロパティを変更した場合は、メッセージの添付ファイルに対して**SaveChanges**呼び出しを行った後に、添付ファイルテーブルが更新され、新しい情報が反映されます。 
  
一部の添付ファイルテーブルでは、さまざまな制限がサポートしています。それ以外の場合は含まれません。 制限のサポートは、メッセージストアプロバイダーの実装によって異なります。 
  
最初に開かれたときには、添付ファイルテーブルが特定の順序で並べ替えられるとは限りません。 
  
_ulflags_パラメーターの MAPI_UNICODE フラグを設定すると、添付ファイルテーブルへの次の呼び出しに影響します。 
  
- [IMAPITable:: querycolumns](imapitable-querycolumns.md)は、列セットを取得します。 
    
- [IMAPITable:: QueryRows](imapitable-queryrows.md)が行を取得します。 
    
- [IMAPITable:: querysortorder](imapitable-querysortorder.md)は、並べ替えの順序を取得します。 
    
unicode フラグを設定すると、これらの呼び出しから返される文字列列の情報は unicode 形式になります。 ただし、すべてのメッセージストアプロバイダーが Unicode をサポートしているわけではないため、このフラグの設定は要求だけになります。
  
## <a name="see-also"></a>関連項目



[IMessage::CreateAttach](imessage-createattach.md)
  
[IMessage::DeleteAttach](imessage-deleteattach.md)
  
[IMessage::OpenAttach](imessage-openattach.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

