---
title: IMessageGetAttachmentTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMessage.GetAttachmentTable
api_type:
- COM
ms.assetid: e568917e-6085-4094-8728-89ba90a78c40
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6eb28f8e69010b138adbf7ec70daecfba149f8a6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592285"
---
# <a name="imessagegetattachmenttable"></a>IMessage::GetAttachmentTable

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの添付ファイル テーブルを返します。
  
```cpp
HRESULT GetAttachmentTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]テーブルの作成に関連するフラグのビットマスク。 次のフラグを設定できます。 
    
MAPI_UNICODE 
  
> 文字列列は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列列は ANSI 形式になります。
    
MAPI_DEFERRED_ERRORS 
  
> **GetAttachmentTable は、** 呼び出し元のクライアントがテーブルを完全に利用できる前に、正常に返す可能性があります。 テーブルが使用できない場合は、後続の呼び出しでエラーが発生する可能性があります。 
    
 _lppTable_
  
> [out]添付ファイル テーブルへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 添付ファイル テーブルが正常に取得されました。
    
## <a name="remarks"></a>注釈

**IMessage::GetAttachmentTable** メソッドは、メッセージ内のすべての添付ファイルに関する情報を含む、メッセージの添付ファイル テーブルへのポインターを返します。 クライアントは、添付ファイル テーブルを通じてのみ添付ファイルにアクセスできます。 添付ファイルの番号をPR_ATTACH_NUM **(** [PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティを取得すると、クライアントはいくつかの **IMessage** メソッドを使用して添付ファイルを処理できます。 
  
添付ファイルごとに 1 行があります。 添付ファイル テーブル内の列の完全な一覧については、「添付ファイル テーブル」 [を参照してください](attachment-tables.md)。
  
添付ファイルは、通常 [、IMAPIProp::SaveChanges](imapiprop-savechanges.md)への呼び出しで添付ファイルとメッセージの両方が保存されるまで、添付ファイルテーブルに表示されません。 添付ファイル テーブルは動的です。 クライアントが新しい添付ファイルを作成したり、既存の添付ファイルを削除したり、メッセージの添付ファイルで **SaveChanges** 呼び出しが行われたら、1 つ以上のプロパティを変更すると、新しい情報を反映するように添付ファイル テーブルが更新されます。 
  
一部の添付ファイル テーブルでは、さまざまな制限がサポートされています。他のユーザーはそうではありません。 制限のサポートは、メッセージ ストア プロバイダーの実装によって異なります。 
  
最初に開いた場合、添付ファイル テーブルは必ずしも特定の順序で並べ替えされません。 
  
_ulFlags_ パラメーター MAPI_UNICODEフラグを設定すると、添付ファイル テーブルへの次の呼び出しに影響します。 
  
- [列セットを取得する IMAPITable::QueryColumns。](imapitable-querycolumns.md) 
    
- [IMAPITable::QueryRows を使用して行](imapitable-queryrows.md) を取得します。 
    
- [並べ替え順序を取得する IMAPITable::QuerySortOrder。](imapitable-querysortorder.md) 
    
Unicode フラグを設定すると、これらの呼び出しから返される文字列列の情報を Unicode 形式で指定する必要があります。 ただし、すべてのメッセージ ストア プロバイダーが Unicode をサポートしているわけではありませんので、このフラグの設定は要求のみです。
  
## <a name="see-also"></a>関連項目



[IMessage::CreateAttach](imessage-createattach.md)
  
[IMessage::DeleteAttach](imessage-deleteattach.md)
  
[IMessage::OpenAttach](imessage-openattach.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

