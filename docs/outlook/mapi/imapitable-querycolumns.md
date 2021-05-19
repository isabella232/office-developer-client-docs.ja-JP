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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d142e19fc4721cec4dde0df7fc030a001121da63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410106"
---
# <a name="imapitablequerycolumns"></a>IMAPITable::QueryColumns

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブルの列の一覧を返します。
  
```cpp
HRESULT QueryColumns(
ULONG ulFlags,
LPSPropTagArray FAR * lpPropTagArray
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]返す列セットを示すフラグのビットマスク。 次のフラグを設定できます。
    
TBL_ALL_COLUMNS 
  
> テーブルは、使用可能なすべての列を返す必要があります。
    
 _lpPropTagArray_
  
> [out]列セットの [プロパティ タグを含む SPropTagArray](sproptagarray.md) 構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 列セットが正常に返されました。
    
MAPI_E_BUSY 
  
> 列セットの取得操作が開始されるのを防ぐ別の操作が進行中です。 進行中の操作の完了を許可するか、停止する必要があります。
    
## <a name="remarks"></a>注釈

**IMAPITable::QueryColumns** メソッドを呼び出して取得できます。 
  
- テーブルの既定の列セット。
    
- [IMAPITable::SetColumns](imapitable-setcolumns.md)メソッドの呼び出しによって確立される、テーブルの現在の列セット。 
    
- テーブルの完全な列セット、使用可能な列ですが、必ずしも現在のセットの一部ではありません。
    
## <a name="notes-to-callers"></a>呼び出し側への注意

TBL_ALL_COLUMNS フラグを設定しない場合 **、IMAPITable::QueryColumns** は、テーブルが **IMAPITable::SetColumns** の呼び出しの影響を受けたかどうかに応じて、テーブルの既定または現在の列セットを返します。 **SetColumns は** 、テーブルの列セット内の列の順序と選択を変更します。 
  
TBL_ALL_COLUMNS フラグを設定すると **、QueryColumns** は、テーブルの列セットに含め得るすべての列を返します。 
  
[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して _、lpPropTagArray_ パラメーターが指すプロパティ タグ配列のメモリを解放します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::D oSetColumns  <br/> |MFCMAPI では **、IMAPITable::QueryColumns** メソッドを使用して、テーブルの現在の列セットを取得し、ユーザーがテーブルを編集できます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

