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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6478f2c6c8196fa332a7b019269e6a6266485d1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800849"
---
# <a name="imapitablegetstatus"></a>IMAPITable::GetStatus

  
  
**適用対象**: Outlook 
  
テーブルのステータスおよび種類を返します。
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a>パラメーター

 _lpulTableStatus_
  
> [out]テーブルのステータスを示す値へのポインター。 次の値のいずれかが返されます。
    
TBLSTAT_COMPLETE 
  
> 操作が進行中ではありません。
    
TBLSTAT_QCHANGED 
  
> テーブルの内容が変更された expectantly。 並べ替えまたは制限の操作に起因する変更は、このステータス値は返されません。
    
TBLSTAT_RESTRICT_ERROR 
  
> [IMAPITable::Restrict](imapitable-restrict.md)操作中にエラーが発生しました。 
    
TBLSTAT_RESTRICTING 
  
> **IMAPITable::Restrict**操作が進行中です。 
    
TBLSTAT_SETCOL_ERROR 
  
> [IMAPITable::SetColumns](imapitable-setcolumns.md)操作中にエラーが発生しました。 
    
TBLSTAT_SETTING_COLS 
  
> **IMAPITable::SetColumns**操作が進行中です。 
    
TBLSTAT_SORT_ERROR 
  
> [IMAPITable::SortTable](imapitable-sorttable.md)操作中にエラーが発生しました。 
    
TBLSTAT_SORTING 
  
> **IMAPITable::SortTable**操作が進行中です。 
    
 _lpulTableType_
  
> [out]テーブルのタイプを示す値へのポインター。 次の 3 つのテーブルの種類のいずれかが返されます。
    
TBLTYPE_DYNAMIC 
  
> テーブルの内容は動的です。行と列の値は、基になるデータの変化に応じて変更できます。
    
TBLTYPE_KEYSET 
  
> テーブル内の行は固定ですが、これらの行に列の値は動的で、基になるデータの変化に応じて変更できます。
    
TBLTYPE_SNAPSHOT 
  
> テーブルは、静的および基になるデータが変更されたとき、その内容が変更されません。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> テーブルの状態が正常に返されました。
    
## <a name="remarks"></a>注釈

**IMAPTable::GetStatus**メソッドは、テーブルの種類と現在の状態に関する情報を取得します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

ほかの 3 つの**IMAPITable**メソッドと組み合わせて**GetStatus**を使用するにはこれらの操作の状態を監視し、テーブル上の効果を確認します。 **IMAPITable**呼び出しを次のいずれかを行った後に、 **GetStatus**を呼び出します。 
  
- [IMAPITable::Restrict](imapitable-restrict.md)の制限を設定します。 
    
- [IMAPITable::SortTable](imapitable-sorttable.md)の並べ替え順序を確立します。 
    
- 列を定義するのには[IMAPITable::SetColumns](imapitable-setcolumns.md)を設定します。 
    
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::GetStatus  <br/> |MFCMAPI では、 **IMAPITable::GetStatus**メソッドを使用して、テーブルのステータスを報告します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

