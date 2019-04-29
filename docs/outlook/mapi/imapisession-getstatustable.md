---
title: imapisessiongetstatustable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetStatusTable
api_type:
- COM
ms.assetid: 53428f8d-4838-46d1-a0ab-cafb194f4cc3
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 17e936093536f548d16021523d9434f09777c6d9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407138"
---
# <a name="imapisessiongetstatustable"></a>IMAPISession::GetStatusTable

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
状態テーブル (セッション内のすべての MAPI リソースに関する情報を含むテーブル) へのアクセスを提供します。
  
```cpp
HRESULT GetStatusTable(
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
  
> 読み上げ状態テーブルへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> テーブルが正常に返されました。
    
## <a name="remarks"></a>注釈

**imapisession:: getstatustable**メソッドは、セッション内のすべての MAPI リソースに関する情報を含む状態テーブルへのアクセスを提供します。 このテーブルには、mapi サブシステムに関する情報、mapi スプーラーの1行、統合アドレス帳の1行、プロファイル内のサービスプロバイダーごとに1つの行があります。 
  
[状態] テーブルの必須およびオプションの列の完全な一覧については、「 [status Tables](status-tables.md)」を参照してください。 
  
_ulflags_パラメーターの MAPI_UNICODE フラグを設定すると、 [imapitable:: querycolumns](imapitable-querycolumns.md)および[imapitable:: QueryRows](imapitable-queryrows.md)メソッドから返される列の形式に影響します。 このフラグは、 [IMAPITable:: querysortorder](imapitable-querysortorder.md)メソッドによって返される並べ替え順序で、プロパティの種類を制御することもできます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|maindlg .cpp  <br/> |CMainDlg:: onstatustable  <br/> |mfcmapi は、 **imapisession:: getstatustable**メソッドを使用して、レンダリングされる状態テーブルを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[状態テーブル](status-tables.md)

