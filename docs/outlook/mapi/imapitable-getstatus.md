---
title: IMAPITableGetStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.GetStatus
api_type:
- COM
ms.assetid: f114f1fa-bc05-4587-875b-71548c5912ea
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8127a09582c98fc82fb5be92dbf24a4e84911ada
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575786"
---
# <a name="imapitablegetstatus"></a>IMAPITable::GetStatus

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブルの状態と型を返します。
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a>パラメーター

 _lpulTableStatus_
  
> [out]テーブルの状態を示す値へのポインター。 次のいずれかの値を返します。
    
TBLSTAT_COMPLETE 
  
> 操作は進行中です。
    
TBLSTAT_QCHANGED 
  
> テーブルの内容が予想通り変更されました。 この状態の値は、並べ替え操作または制限操作による変更に対して返されません。
    
TBLSTAT_RESTRICT_ERROR 
  
> [IMAPITable::Restrict 操作中にエラーが発生](imapitable-restrict.md)しました。 
    
TBLSTAT_RESTRICTING 
  
> **IMAPITable::Restrict 操作** が進行中です。 
    
TBLSTAT_SETCOL_ERROR 
  
> [IMAPITable::SetColumns 操作中にエラーが発生](imapitable-setcolumns.md)しました。 
    
TBLSTAT_SETTING_COLS 
  
> **IMAPITable::SetColumns 操作** が進行中です。 
    
TBLSTAT_SORT_ERROR 
  
> [IMAPITable::SortTable 操作中にエラーが発生](imapitable-sorttable.md)しました。 
    
TBLSTAT_SORTING 
  
> **IMAPITable::SortTable** 操作が進行中です。 
    
 _lpulTableType_
  
> [out]テーブルの種類を示す値へのポインター。 次の 3 つのテーブルの種類のいずれかを返します。
    
TBLTYPE_DYNAMIC 
  
> テーブルの内容は動的です。基になるデータの変更に応じ、行と列の値が変更される可能性があります。
    
TBLTYPE_KEYSET 
  
> テーブル内の行は固定されますが、これらの行内の列の値は動的であり、基になるデータが変更されるに従って変更される可能性があります。
    
TBLTYPE_SNAPSHOT 
  
> テーブルは静的であり、基になるデータが変更された場合、その内容は変更されません。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> テーブルの状態が正常に返されました。
    
## <a name="remarks"></a>注釈

**IMAPTable::GetStatus** メソッドは、テーブルの種類と現在の状態に関する情報を取得します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**GetStatus** を他の 3 つの **IMAPITable** メソッドと組み合わせて使用して、これらの操作の状態を監視し、テーブルに対する影響を判断できます。 次のいずれかの **IMAPITable** 呼び出しを行った後 **、GetStatus を呼び出** します。 
  
- [IMAPITable::制限を](imapitable-restrict.md) 設定します。 
    
- [IMAPITable::SortTable を使用](imapitable-sorttable.md) して並べ替え順序を確立します。 
    
- [IMAPITable::SetColumns を使用](imapitable-setcolumns.md) して列セットを定義します。 
    
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::GetStatus  <br/> |MFCMAPI は **IMAPITable::GetStatus** メソッドを使用してテーブルの状態を報告します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

