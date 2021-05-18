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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fbc990a8c962883aa07987b200d1d2fd55434f93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413046"
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
  
> [in]シーク操作の開始位置を識別するブックマーク。 ブックマークは [、IMAPITable::CreateBookmark](imapitable-createbookmark.md) メソッドを使用して作成するか、次のいずれかの定義済みの値を渡します。 
    
BOOKMARK_BEGINNING 
  
> テーブルの先頭からシーク操作を開始します。 
    
BOOKMARK_CURRENT 
  
> カーソルがあるテーブルの行からシーク操作を開始します。 
    
BOOKMARK_END 
  
> テーブルの最後からシーク操作を開始します。 
    
 _lRowCount_
  
> [in]  _bkOrigin_ パラメーターで識別されるブックマークから始まる、移動する行数の符号付きカウント。 
    
 _lplRowsSought_
  
> [out]  _lRowCount_ が入力上の有効なポインターである場合  _、lplRowsSought_ はシーク操作で処理された行の数を指し示し、その符号は検索方向、前方方向、または後方方向を示します。 _lRowCount が_ 負の場合 _、lplRowsSought は_ 負の値になります。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> シーク操作が成功しました。
    
MAPI_E_BUSY 
  
> 行シーク操作の開始を妨げる別の操作が進行中です。 進行中の操作の完了を許可するか、停止する必要があります。
    
MAPI_E_INVALID_BOOKMARK 
  
> _bkOrigin_ パラメーターで指定されたブックマークは、削除されたため、または要求された最後の行を超えているため無効です。 
    
MAPI_W_POSITION_CHANGED 
  
> 呼び出しは成功しましたが  _、bkOrigin_ パラメーターで指定されたブックマークは、前回の使用時と同じ行に設定されなくなりました。 ブックマークが使用されていない場合、ブックマークは作成された位置と同じ位置になくなりました。 この警告が返されると、呼び出しは正常に処理されます。 この警告をテストするには、次のマクロ **HR_FAILED** します。 詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。
    
## <a name="remarks"></a>注釈

**IMAPITable::SeekRow** メソッドは、カーソルの新BOOKMARK_CURRENT位置を確立します。 _lRowCount パラメーター_ は、カーソルが移動する行数と移動方向を示します。 
  
結果の位置が表の最後の行を超える場合、カーソルは最後の行の後に配置されます。 結果の位置が表の最初の行の前にある場合、カーソルは最初の行の先頭に配置されます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

_bkOrigin_ が指す行がテーブルに存在しなくなった場合、ブックマークの新しい位置を確立できない場合は、次の値をMAPI_E_INVALID_BOOKMARK。 _bkOrigin_ が指す行が存在しなくなった場合、ブックマークの新しい位置を確立できる場合は、次のMAPI_W_POSITION_CHANGED。 
  
テーブル ビューから折りたたむ行を指すブックマークは、引き続き使用できます。 呼び出し元がそのようなブックマークにカーソルを移動しようとした場合は、カーソルを次の表示行に移動し、カーソルを戻MAPI_W_POSITION_CHANGED。 
  
折りたたむ位置のブックマークは、使用時または行が折りたたむ時点で、表示から外れて移動できます。 行が折りたたむ時点でブックマークを移動する場合は、ブックマークが最後に使用された後に移動したかどうかを示すブックマークに少し保持するか、作成後にブックマークが使用されたことがない場合は、ブックマークを移動します。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

SeekRow の逆方向の移動 **を示す場合** は  _、lRowCount で負の値を渡します_。 テーブルの先頭まで検索するには  _、lRowCount_ で 0 を渡し  _、bkOrigin_ の値BOOKMARK_BEGINNING渡します。 
  
テーブルに多数の行がある場合 **、SeekRow** 操作が遅くなる可能性があります。 lplRowsSought パラメーターの内容で行数を返す必要がある場合にも、パフォーマンス  _が影響を受ける可能性_ があります。 
  
 **SeekRow** は  _、lRowCount_ が指す変数で、実際に検索された行数 (正または負) を返します。 通常の操作では、検索がテーブルの先頭または末尾に達しない限り _、lRowCount_ に渡された _lplRowsSought_ と同じ値を返す必要があります。 
  
_lRowCount を_ 50 より大きい数値に設定しない。 より多くの行をシークするには [、IMAPITable::SeekRowApprox メソッドを使用](imapitable-seekrowapprox.md) します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIProcessor.cpp  <br/> |CMAPIProcessor::P rocessMailboxTable  <br/> |MFCMAPI では **、IMAPITable::SeekRow** メソッドを使用して、処理前にテーブルの先頭を検索します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

