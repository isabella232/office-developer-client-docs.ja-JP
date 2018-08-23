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
ms.openlocfilehash: 86dfaa8fbc9ff24d38472f1339a22534086d890b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593747"
---
# <a name="imapitablequerycolumns"></a>IMAPITable::QueryColumns

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
テーブルの列の一覧を返します。
  
```cpp
HRESULT QueryColumns(
ULONG ulFlags,
LPSPropTagArray FAR * lpPropTagArray
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]のどの列の設定を示すフラグのビットマスクが返されます。 次のフラグを設定することができます。
    
TBL_ALL_COLUMNS 
  
> テーブルは、すべての利用可能な列を返す必要があります。
    
 _lpPropTagArray_
  
> [out]列のプロパティ タグを含む[SPropTagArray](sproptagarray.md)構造体へのポインターを設定します。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 列セットが正常に返されました。
    
MAPI_E_BUSY 
  
> 別の操作により、列の進行状況の設定の取得操作の開始されます。 実行中の操作を完了できるか、それを停止する必要があります。
    
## <a name="remarks"></a>注釈

取得する場合に、 **IMAPITable::QueryColumns**メソッドを呼び出すことができます。 
  
- 既定の列をテーブルに設定します。
    
- 表については、 [IMAPITable::SetColumns](imapitable-setcolumns.md)メソッドの呼び出しによって設定されるを設定します。 
    
- テーブル、使用可能な列は必ずしも現在のセットの一部の設定の完全な列。
    
## <a name="notes-to-callers"></a>呼び出し側への注意

TBL_ALL_COLUMNS フラグが設定されていない場合、 **IMAPITable::QueryColumns**は、テーブルの既定値または**IMAPITable::SetColumns**を呼び出すことで、テーブルが影響を受けてかどうかによって、現在の列のセットを返します。 **SetColumns**では、順序とテーブルの列のセット内の列の選択範囲を変更します。 
  
TBL_ALL_COLUMNS フラグを設定すると、すべての列がテーブルの列のセットにすることのできる**QueryColumns**が返されます。 
  
関数を呼び出して、 [MAPIFreeBuffer](mapifreebuffer.md) 、 _lpPropTagArray_パラメーターで示されるプロパティ タグ配列用のメモリを解放します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::DoSetColumns  <br/> |MFCMAPI では、 **IMAPITable::QueryColumns**メソッドを使用して、現在の列をユーザーが編集できるように、テーブルの設定を取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

