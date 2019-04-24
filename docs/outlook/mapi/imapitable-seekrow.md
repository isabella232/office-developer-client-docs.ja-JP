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
ms.openlocfilehash: fbc990a8c962883aa07987b200d1d2fd55434f93
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328827"
---
# <a name="imapitableseekrow"></a>IMAPITable::SeekRow

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
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
  
> 順番シーク操作の開始位置を識別するブックマーク。 ブックを作成するには、 [IMAPITable:: createbookmark](imapitable-createbookmark.md)メソッドを使用するか、次の定義済みの値のいずれかを渡すことができます。 
    
BOOKMARK_BEGINNING 
  
> テーブルの先頭からシーク操作を開始します。 
    
BOOKMARK_CURRENT 
  
> カーソルが置かれているテーブルの行からシーク操作を開始します。 
    
BOOKMARK_END 
  
> テーブルの最後からシーク操作を開始します。 
    
 _lrowcount_
  
> 順番_bkOrigin_パラメーターによって識別されるブックマークから開始して、移動する行数の符号付き数。 
    
 _lplrowssought_
  
> 読み上げ_lrowcount_が入力の有効なポインターである場合、 _lplrowssは_、シーク操作で処理された行数を指していることを示します。の符号は、検索の方向 (前方または後方) を示します。 _lrowcount_が負の場合、 _lplrowssは_負の値になります。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> シーク操作が正常に完了しました。
    
MAPI_E_BUSY 
  
> 別の操作が進行中であるため、行シーク操作を開始できません。 進行中の操作が完了することを許可するか、停止する必要があります。
    
MAPI_E_INVALID_BOOKMARK 
  
> _bkOrigin_パラメーターで指定されたブックマークは、削除されたか、要求された最後の行を超えているため、無効です。 
    
MAPI_W_POSITION_CHANGED 
  
> 呼び出しは成功しましたが、 _bkOrigin_パラメーターで指定されたブックマークは、最後に使用されたときと同じ行に設定されていません。 ブックマークが使用されていない場合は、作成時と同じ位置になりません。 この警告が返された場合、呼び出しは正常に処理されます。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。
    
## <a name="remarks"></a>解説

**IMAPITable:: seekrow**メソッドは、カーソルの新しい BOOKMARK_CURRENT 位置を確立します。 _lrowcount_パラメーターは、カーソルが移動する行の数と移動の方向を示します。 
  
結果の位置が表の最後の行を超える場合、カーソルは最後の行の後に配置されます。 結果の位置がテーブルの最初の行より前にある場合、カーソルは先頭行の先頭に配置されます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

_bkOrigin_によって参照される行がテーブルに存在しなくなり、ブックマークの新しい位置を設定できない場合は、MAPI_E_INVALID_BOOKMARK を返します。 _bkOrigin_によって参照される行が存在しなくなり、ブックマークの新しい位置を設定できる場合は、MAPI_W_POSITION_CHANGED を返します。 
  
テーブルビューから折りたたまれている行を指すブックマークは、引き続き使用できます。 呼び出し元がこのようなブックマークにカーソルを移動しようとした場合は、カーソルを次の表示される行に移動し、MAPI_W_POSITION_CHANGED を返します。 
  
使用時または行が折りたたまれたときに、表示されていない位置のブックマークを移動できます。 行が折りたたまれたときにブックマークが移動された場合は、ブックマークが最後に使用されてから移動したか、または作成後に一度も使用されていない場合は、ブックマークが移動したかどうかを示すビットを保持します。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**seekrow**の後方移動を指定するには、 _lrowcount_に負の値を渡します。 テーブルの先頭を検索するには、 _lrowcount_の0と、 _bkOrigin_の値 BOOKMARK_BEGINNING を渡します。 
  
テーブルに多数の行がある場合、 **seekrow**操作が遅くなることがあります。 _lplrowssought_パラメーターの内容で行数を返す必要がある場合は、パフォーマンスに影響することもあります。 
  
 **seekrow**は、 _lrowcount_によって参照される変数内で実際に検索された行の数 (正または負) を返します。 通常の操作では、検索によってテーブルの先頭または末尾に到達した場合を除いて、 _lrowcount_ _rowssが_渡されたときと同じ値を返す必要があります。 
  
_lrowcount_を50より大きい数値に設定しないでください。 より多くの行をシークするには、 [IMAPITable:: seekrowapprox](imapitable-seekrowapprox.md)メソッドを使用します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIProcessor  <br/> |cmapiprocessor::P rocessmailboxtable  <br/> |mfcmapi は、 **IMAPITable:: seekrow**メソッドを使用して、処理の前にテーブルの先頭を特定します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

