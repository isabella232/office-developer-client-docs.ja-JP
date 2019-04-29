---
title: IMAPITableGetStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetStatus
api_type:
- COM
ms.assetid: f114f1fa-bc05-4587-875b-71548c5912ea
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ec305fc872d1bf1718592dabdd230617d50d3f54
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434334"
---
# <a name="imapitablegetstatus"></a>IMAPITable::GetStatus

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブルの状態と種類を返します。
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a>パラメーター

 _lpultablestatus_
  
> 読み上げテーブルの状態を示す値へのポインター。 次のいずれかの値を返すことができます。
    
TBLSTAT_COMPLETE 
  
> 進行中の操作はありません。
    
TBLSTAT_QCHANGED 
  
> 表の内容が expectantly 変更されました。 この状態値は、並べ替えまたは制限の操作によって発生した変更に対しては返されません。
    
TBLSTAT_RESTRICT_ERROR 
  
> [IMAPITable:: Restrict](imapitable-restrict.md)操作中にエラーが発生しました。 
    
TBLSTAT_RESTRICTING 
  
> **IMAPITable:: Restrict**操作が進行中です。 
    
TBLSTAT_SETCOL_ERROR 
  
> [IMAPITable:: SetColumns](imapitable-setcolumns.md)操作中にエラーが発生しました。 
    
TBLSTAT_SETTING_COLS 
  
> **IMAPITable:: SetColumns**操作が進行中です。 
    
TBLSTAT_SORT_ERROR 
  
> [IMAPITable:: sorttable](imapitable-sorttable.md)操作中にエラーが発生しました。 
    
TBLSTAT_SORTING 
  
> **IMAPITable:: sorttable**操作が進行中です。 
    
 _lpulTableType_
  
> 読み上げテーブルの種類を示す値へのポインター。 次の3種類のテーブルのいずれかを返すことができます。
    
TBLTYPE_DYNAMIC 
  
> テーブルの内容は動的です。行と列の値は、基になるデータが変更されたときに変更されることがあります。
    
TBLTYPE_KEYSET 
  
> テーブル内の行は固定されていますが、これらの行の列の値は動的であり、基になるデータの変更として変更できます。
    
TBLTYPE_SNAPSHOT 
  
> テーブルは静的であり、基になるデータが変更されてもその内容は変更されません。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> テーブルの状態が正常に返されました。
    
## <a name="remarks"></a>注釈

**IMAPTable:: GetStatus**メソッドは、テーブルの種類と現在の状態に関する情報を取得します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**GetStatus**を3つの他の**IMAPITable**メソッドと組み合わせて使用すると、これらの操作の状態を監視し、テーブルに対する効果を確認できます。 次の**IMAPITable**呼び出しのいずれかを行った後、 **GetStatus**を呼び出します。 
  
- [IMAPITable::](imapitable-restrict.md)制限を設定します。 
    
- [IMAPITable:: sorttable](imapitable-sorttable.md)は、並べ替えの順序を設定します。 
    
- [IMAPITable:: SetColumns](imapitable-setcolumns.md)列セットを定義します。 
    
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ContentsTableListCtrl  <br/> |CContentsTableListCtrl:: GetStatus  <br/> |mfcmapi は、 **IMAPITable:: GetStatus**メソッドを使用して、テーブルの状態を報告します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

