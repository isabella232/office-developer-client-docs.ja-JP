---
title: IMAPITableSeekRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SeekRow
api_type:
- COM
ms.assetid: 93ac63ae-f254-45e1-a9b1-347d69d2ed9f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 143ca03a5e98d638d29394f5c0803e349ab4de25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800848"
---
# <a name="imapitableseekrow"></a>IMAPITable::SeekRow

  
  
**適用対象**: Outlook 
  
テーブル内の特定の位置にカーソルを移動します。
  
```cpp
HRESULT SeekRow(
BOOKMARK bkOrigin,
LONG lRowCount,
LONG FAR * lplRowsSought
);
```

## <a name="parameters"></a>パラメーター

 _bkOrigin_
  
> [in]シーク操作の開始位置を識別するブックマークです。 、 [IMAPITable::CreateBookmark](imapitable-createbookmark.md)メソッドを使用してブックマークを作成することができますか、次の定義済み値の 1 つ渡すことができます。 
    
BOOKMARK_BEGINNING 
  
> テーブルの先頭からシーク操作を開始します。 
    
BOOKMARK_CURRENT 
  
> シーク操作は、カーソルが配置されているテーブル内の行から開始します。 
    
BOOKMARK_END 
  
> テーブルの末尾からシーク操作を開始します。 
    
 _lRowCount_
  
> [in]移動する行の数の符号付きの数、ブックマークから、 _bkOrigin_パラメーターで識別されます。 
    
 _lplRowsSought_
  
> [out]_LRowCount_がシーク操作で処理された行の数を入力すると、 _lplRowsSought_のポイントの有効なポインターである場合は、先の符号は、前方または後方検索の方向を示します。 _LRowCount_が負の場合は、 _lplRowsSought_が負の値です。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> シーク操作が正常に完了しました。
    
MAPI_E_BUSY 
  
> 別の操作は、行のシーク操作の開始を防止する処理中です。 実行中の操作を完了できるか、それを停止する必要があります。
    
MAPI_E_INVALID_BOOKMARK 
  
> 削除されたため、または要求された最後の行を越えることがあるために、 _bkOrigin_パラメーターで指定されたブックマークは無効です。 
    
MAPI_W_POSITION_CHANGED 
  
> 呼び出しが成功したが、最後に使用されたときと同じ行に、 _bkOrigin_パラメーターで指定されたブックマークが設定されないことです。 ブックマークが使用されていない場合は不要になった同じ位置に作成されたときと同じ この警告が返されると、呼び出しを成功として処理する必要があります。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。
    
## <a name="remarks"></a>注釈

**IMAPITable::SeekRow**メソッドは、カーソルの新しい BOOKMARK_CURRENT の位置を確立します。 _LRowCount_パラメーターでは、カーソルを移動する行と移動の方向の数を示します。 
  
結果の位置がテーブルの最後の行以外の場合は、最後の行の後、カーソルが配置されます。 結果の位置がテーブルの最初の行の前にある場合は、最初の行の先頭にカーソルが配置されます。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

_BkOrigin_で指定された行がテーブルに存在していませんし、新しいブックマークの位置を確立することはできません、する場合は、MAPI_E_INVALID_BOOKMARK を返します。 _BkOrigin_で指定された行が存在しないと、新しいブックマークの位置を確立することができます、MAPI_W_POSITION_CHANGED を返します。 
  
テーブルの表示が折りたたまれている行を示すブックマークを使用することがまだできます。 呼び出し元がこのようなブックマークにカーソルを移動しようとすると場合、は、次の表示されている行にカーソルを移動し、MAPI_W_POSITION_CHANGED を返します。 
  
位置の使用時に、または行が折りたたまれているときに見えなくなり、折りたたまれているためにブックマークを移動することができます。 ブックマークは、行が折りたたまれているときに移動する場合は、かを示すかどうか、ブックマークが最後に使用してから移動、ことはありませんが使用されて、作成されてからブックマークに少ししてください。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**SeekRow**の逆方向の移動を示す、 _lRowCount_の負の値を渡します。 テーブルの先頭を検索するには、 _lRowCount_と_bkOrigin_の BOOKMARK_BEGINNING の値に 0 を渡します。 
  
多くのテーブル内の行がある場合は、 **SeekRow**操作が低下することができます。 パフォーマンスは、 _lplRowsSought_パラメーターの内容で返される行の数を必要とする場合にも影響します。 
  
 **SeekRow**は、実際を検索、正または負の場合、 _lRowCount_が指す変数の行の数を返します。 通常の操作で、返す必要があります_lplRowsSought_の値が同じように_lRowCount_、ために渡された検索は先頭またはテーブルの末尾に到達しない限り。 
  
設定しないで_lRowCount_を番号に 50 を超える。 多数の行をシーク、 [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)メソッドを使用します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIProcessor.cpp  <br/> |CMAPIProcessor::ProcessMailboxTable  <br/> |MFCMAPI では、 **IMAPITable::SeekRow**メソッドを使用して、処理する前にテーブルの先頭を見つけます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

