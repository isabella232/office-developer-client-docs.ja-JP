---
title: IMsgStoreGetReceiveFolderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgStore.GetReceiveFolderTable
api_type:
- COM
ms.assetid: d115ab58-07d2-4b49-8e08-2881c2924102
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e9f8eb5e8c5bb21e7c1a9a61d6dfd85630d2f553
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620689"
---
# <a name="imsgstoregetreceivefoldertable"></a>IMsgStore::GetReceiveFolderTable

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストアのすべての受信フォルダーに関する情報を含む、受信フォルダー テーブルへのアクセスを提供します。
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]テーブル アクセスを制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DEFERRED_ERRORS 
  
> **GetReceiveFolderTable** は、テーブルが呼び出し元で完全に使用できる前に、正常に戻ります。 テーブルが完全に使用できない場合は、後続のテーブル呼び出しでエラーが発生する可能性があります。 
    
MAPI_UNICODE 
  
> 返される文字列は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。
    
 _lppTable_
  
> [out]受信フォルダー テーブルへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 受信フォルダー テーブルが正常に返されました。
    
## <a name="remarks"></a>注釈

**IMsgStore::GetReceiveFolderTable** メソッドは、メッセージ ストアのすべての受信フォルダーのプロパティ設定を示すテーブルへのアクセスを提供します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

受信フォルダー テーブルで必要な列の一覧については、「受信フォルダー テーブル [」を参照してください](receive-folder-tables.md)。 
  
受信フォルダー テーブルを実装して、プロパティ制限 [(PidTagRecordKey)](pidtagrecordkey-canonical-property.md)プロパティ **PR_RECORD_KEY設定を** サポートします。 これにより、特定の受信フォルダーに簡単にアクセスできます。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_ulFlags_ パラメーター MAPI_UNICODEフラグを設定すると [、IMAPITable::QueryColumns](imapitable-querycolumns.md)および [IMAPITable::QueryRows](imapitable-queryrows.md)メソッドから返される列の形式に影響します。 このフラグは [、IMAPITable::QuerySortOrder](imapitable-querysortorder.md) メソッドによって返される並べ替え順序のプロパティの種類も制御します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnDisplayReceiveFolderTable  <br/> |MFCMAPI は **、IMsgStore::GetReceiveFolderTable** メソッドを使用して、表示する受信フォルダー テーブルを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

