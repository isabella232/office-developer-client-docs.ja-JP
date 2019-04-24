---
title: IMsgStoreGetReceiveFolderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetReceiveFolderTable
api_type:
- COM
ms.assetid: d115ab58-07d2-4b49-8e08-2881c2924102
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 303c2ef855d5cfc1d6614bda92b46c2da97717c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317354"
---
# <a name="imsgstoregetreceivefoldertable"></a>IMsgStore::GetReceiveFolderTable

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
受信フォルダーテーブル (メッセージストアのすべての受信フォルダーに関する情報を含むテーブル) へのアクセスを提供します。
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番テーブルアクセスを制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DEFERRED_ERRORS 
  
> 呼び出し元がテーブルを完全に使用できるようになる前に、 **getreceivefoldertable**を正常に返すことができるようにします。 テーブルが完全に使用できない場合は、次のテーブル呼び出しを行うとエラーが発生する可能性があります。 
    
MAPI_UNICODE 
  
> 返される文字列は、Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。
    
 _lpptable_
  
> 読み上げ受信フォルダーテーブルへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 受信フォルダーテーブルが正常に返されました。
    
## <a name="remarks"></a>解説

**IMsgStore:: getreceivefoldertable**メソッドは、すべてのメッセージストアの受信フォルダーのプロパティ設定を示すテーブルへのアクセスを提供します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

受信フォルダーテーブルに必要な列の一覧については、「[受信フォルダーテーブル](receive-folder-tables.md)」を参照してください。 
  
受信フォルダーテーブルを実装して、 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) プロパティのプロパティ制限の設定をサポートします。 これにより、特定の受信フォルダーへのアクセスが容易になります。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_ulflags_パラメーターの MAPI_UNICODE フラグを設定すると、 [imapitable:: querycolumns](imapitable-querycolumns.md)および[imapitable:: QueryRows](imapitable-queryrows.md)メソッドから返される列の形式に影響します。 このフラグは、 [IMAPITable:: querysortorder](imapitable-querysortorder.md)メソッドによって返される並べ替え順序で、プロパティの種類を制御することもできます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MsgStoreDlg  <br/> |CMsgStoreDlg:: ondisplayreceivefoldertable  <br/> |mfcmapi は、 **IMsgStore:: getreceivefoldertable**メソッドを使用して、表示する受信フォルダーテーブルを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

