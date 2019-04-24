---
title: IMAPITableQueryColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryColumns
api_type:
- COM
ms.assetid: d6341acc-c6ca-4605-93af-77230040339d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d142e19fc4721cec4dde0df7fc030a001121da63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328883"
---
# <a name="imapitablequerycolumns"></a>IMAPITable::QueryColumns

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブルの列のリストを返します。
  
```cpp
HRESULT QueryColumns(
ULONG ulFlags,
LPSPropTagArray FAR * lpPropTagArray
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番返される列セットを示すフラグのビットマスク。 次のフラグを設定できます。
    
TBL_ALL_COLUMNS 
  
> テーブルは使用可能なすべての列を返します。
    
 _lpPropTagArray_
  
> 読み上げ列セットのプロパティタグを含む[SPropTagArray](sproptagarray.md)構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 列セットが正常に返されました。
    
MAPI_E_BUSY 
  
> 別の操作が進行中であるため、列セットの取得操作を開始できません。 進行中の操作が完了することを許可するか、停止する必要があります。
    
## <a name="remarks"></a>解説

**IMAPITable:: querycolumns**メソッドを呼び出すと、次のものを取得できます。 
  
- テーブルの既定の列セット。
    
- [IMAPITable:: SetColumns](imapitable-setcolumns.md)メソッドの呼び出しによって確立された、テーブルの現在の列セット。 
    
- テーブルの完全な列セット。使用可能な列ですが、現在のセットの一部ではありません。
    
## <a name="notes-to-callers"></a>呼び出し側への注意

TBL_ALL_COLUMNS フラグを設定しない場合、 **imapitable:: querycolumns**は、テーブルの既定または現在の列セットを返します。これは、テーブルが**IMAPITable:: SetColumns**の呼び出しの影響を受けたかどうかによって決まります。 **SetColumns**は、テーブルの列セット内の列の順序と選択範囲を変更します。 
  
TBL_ALL_COLUMNS フラグを設定した場合、 **querycolumns**は、テーブルの列セットに設定可能なすべての列を返します。 
  
[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、 _lpPropTagArray_パラメーターによって示されるプロパティタグ配列のメモリを解放します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ContentsTableListCtrl  <br/> |CContentsTableListCtrl::D osetcolumns  <br/> |mfcmapi は、 **IMAPITable:: querycolumns**メソッドを使用して、テーブルの現在の列セットを取得し、ユーザーが編集できるようにします。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

