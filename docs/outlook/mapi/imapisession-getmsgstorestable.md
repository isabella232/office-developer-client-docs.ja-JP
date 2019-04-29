---
title: imapisessiongetmsgstorestable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetMsgStoresTable
api_type:
- COM
ms.assetid: 77db2dff-4534-440f-a05c-635711cbc2c3
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5fced633023ebf00efaf5b667dc7994eeb5de316
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428138"
---
# <a name="imapisessiongetmsgstorestable"></a>IMAPISession::GetMsgStoresTable

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
セッションプロファイル内のすべてのメッセージストアに関する情報を含むメッセージストアテーブルへのアクセスを提供します。
  
```cpp
HRESULT GetMsgStoresTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番文字列の列の形式を決定するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 文字列列は Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列列は ANSI 形式になります。
    
 _lpptable_
  
> 読み上げメッセージストアテーブルへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> テーブルが正常に返されました。
    
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されていて、セッションは UNICODE をサポートしていません。
    
## <a name="remarks"></a>注釈

**imapisession:: getmsgstorestable**メソッドは、メッセージストアテーブルへのポインターを取得します。このテーブルは、プロファイル内の開いている各メッセージストアに関する情報を含む MAPI によって保持されます。 
  
メッセージストアテーブルの必須およびオプションの列の完全な一覧については、「 [message store Tables](message-store-tables.md)」を参照してください。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

MAPI は、セッション中に変更が発生するたびにメッセージストアテーブルを更新するので、メッセージストアテーブルの**Advise**メソッドを呼び出して、これらの変更について通知されるように登録します。 変更できるのは、新しいメッセージストアの追加、既存のストアの削除、および既定のストアに対する変更です。 
  
_ulflags_パラメーターの MAPI_UNICODE フラグを設定すると、 [imapitable:: querycolumns](imapitable-querycolumns.md)および[imapitable:: QueryRows](imapitable-queryrows.md)メソッドから返される列の形式に影響します。 このフラグは、 [IMAPITable:: querysortorder](imapitable-querysortorder.md)メソッドによって返される並べ替え順序で、プロパティの種類を制御することもできます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|maindlg .cpp  <br/> |CMainDlg:: onopenmessagestoretable  <br/> |mfcmapi は、 **imapisession:: getmsgstorestable**メソッドを使用して、メッセージストアテーブルを取得して、mfcmapi のメインダイアログボックスに表示できるようにします。  <br/> |
   
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
  
[メッセージストアテーブル](message-store-tables.md)

