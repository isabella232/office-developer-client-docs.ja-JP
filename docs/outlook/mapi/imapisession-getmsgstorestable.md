---
title: IMAPISessionGetMsgStoresTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.GetMsgStoresTable
api_type:
- COM
ms.assetid: 77db2dff-4534-440f-a05c-635711cbc2c3
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e7c00cc8fa6f651ded26b23522eb4943195c27f2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620934"
---
# <a name="imapisessiongetmsgstorestable"></a>IMAPISession::GetMsgStoresTable

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
セッション プロファイル内のすべてのメッセージ ストアに関する情報を含むメッセージ ストア テーブルへのアクセスを提供します。
  
```cpp
HRESULT GetMsgStoresTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]文字列である列の形式を決定するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 文字列列は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列列は ANSI 形式になります。
    
 _lppTable_
  
> [out]メッセージ ストア テーブルへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> テーブルが正常に返されました。
    
MAPI_E_BAD_CHARWIDTH 
  
> このMAPI_UNICODEが設定され、セッションは Unicode をサポートしていない。
    
## <a name="remarks"></a>注釈

**IMAPISession::GetMsgStoresTable** メソッドは、プロファイル内の開いている各メッセージ ストアに関する情報を含む MAPI によって管理されるテーブルであるメッセージ ストア テーブルへのポインターを取得します。 
  
メッセージ ストア テーブルの必須列と省略可能列の完全な一覧については、「メッセージ ストア テーブル」 [を参照してください](message-store-tables.md)。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

MAPI は、変更が発生するたびにセッション中にメッセージ ストア テーブルを更新しますので、メッセージ ストア テーブルの **Advise** メソッドを呼び出して、これらの変更の通知を受け取る登録を行います。 可能な変更には、新しいメッセージ ストアの追加、既存のストアの削除、既定のストアへの変更が含まれます。 
  
_ulFlags_ パラメーター MAPI_UNICODEフラグを設定すると [、IMAPITable::QueryColumns](imapitable-querycolumns.md)および [IMAPITable::QueryRows](imapitable-queryrows.md)メソッドから返される列の形式に影響します。 このフラグは [、IMAPITable::QuerySortOrder](imapitable-querysortorder.md) メソッドによって返される並べ替え順序のプロパティの種類も制御します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenMessageStoreTable  <br/> |MFCMAPI は **IMAPISession::GetMsgStoresTable** メソッドを使用してメッセージ ストア テーブルを取得し、MFCMAPI のメイン ダイアログ ボックスで表示できます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[メッセージ ストア テーブル](message-store-tables.md)

