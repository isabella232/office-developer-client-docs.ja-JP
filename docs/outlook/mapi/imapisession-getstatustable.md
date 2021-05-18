---
title: IMAPISessionGetStatusTable
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
  
セッション内のすべての MAPI リソースに関する情報を含むテーブルである状態テーブルへのアクセスを提供します。
  
```cpp
HRESULT GetStatusTable(
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
  
> [out]状態テーブルへのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> テーブルが正常に返されました。
    
## <a name="remarks"></a>注釈

**IMAPISession::GetStatusTable** メソッドは、セッション内のすべての MAPI リソースに関する情報を含む状態テーブルへのアクセスを提供します。 表には、MAPI サブシステムに関する情報を示す 1 行、MAPI スプーラー用の 1 行、統合アドレス帳用の 1 行、プロファイル内のサービス プロバイダーごとに 1 行があります。 
  
状態テーブルの必須列と省略可能列の完全な一覧については、「Status [Tables」を参照してください](status-tables.md)。 
  
_ulFlags_ パラメーター MAPI_UNICODEフラグを設定すると [、IMAPITable::QueryColumns](imapitable-querycolumns.md)および [IMAPITable::QueryRows](imapitable-queryrows.md)メソッドから返される列の形式に影響します。 このフラグは [、IMAPITable::QuerySortOrder](imapitable-querysortorder.md) メソッドによって返される並べ替え順序のプロパティの種類も制御します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnStatusTable  <br/> |MFCMAPI は **IMAPISession::GetStatusTable** メソッドを使用して、レンダリングする状態テーブルを取得します。  <br/> |
   
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

