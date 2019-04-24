---
title: IMAPITableFindRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.FindRow
api_type:
- COM
ms.assetid: 6511368c-9777-497e-9eea-cf390c04b92e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a5364af229721d101f38d2f054f528169b48c09e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329081"
---
# <a name="imapitablefindrow"></a>IMAPITable::FindRow

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
特定の検索条件に一致するテーブル内の次の行を検索し、その行にカーソルを移動します。
  
```cpp
HRESULT FindRow(
LPSRestriction lpRestriction,
BOOKMARK BkOrigin,
ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpRestriction_
  
> 順番検索条件を記述する[srestriction](srestriction.md)構造体へのポインター。 
    
 _BkOrigin_
  
> 順番**FindRow**が検索を開始する行を識別するブックマーク。 ブックを作成するには、 [IMAPITable:: createbookmark](imapitable-createbookmark.md)メソッドを使用するか、次の定義済みの値のいずれかを渡すことができます。 
    
BOOKMARK_BEGINNING 
  
> 表の先頭から検索します。 
    
BOOKMARK_CURRENT 
  
> カーソルが置かれているテーブルの行から検索します。 
    
BOOKMARK_END 
  
> 表の末尾から検索します。 
    
 _ulFlags_
  
> 順番検索の方向を制御するフラグのビットマスク。 次のフラグを設定できます。
    
DIR_BACKWARD 
  
> ブックマークで指定された行から後方へ検索します。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 検索操作が正常に完了しました。
    
MAPI_E_INVALID_BOOKMARK 
  
> _BkOrigin_パラメーターのブックマークは、削除されたか、要求された最後の行を超えているため、無効です。 
    
MAPI_E_NOT_FOUND 
  
> 制限に一致する行が見つかりませんでした。
    
MAPI_W_POSITION_CHANGED
  
> 呼び出しは成功しましたが、操作に使用されたブックマークは、最後に使用されたときと同じ行に設定されていません。ブックマークが使用されていない場合は、作成時と同じ位置になりません。 この警告が返された場合、呼び出しは正常に処理されます。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。
    
## <a name="remarks"></a>解説

**IMAPITable:: FindRow**メソッドは、表の最初の行を検索し、 _lpRestriction_パラメーターで指定された**srestriction**構造で記述された一連の検索条件に一致するようにします。 
  
通常、 **FindRow**は指定されたブックマークから前方へ検索します。 呼び出し元は、 _ulflags_パラメーターに DIR_BACKWARD フラグを設定することによって、ブックマークから後方に移動するように検索を設定できます。 前方検索は現在のブックマークから開始されます。後方検索は、ブックマークの前の行から開始されます。 検索の終了位置は、制限を満たす最初の行の直前にあります。 
  
_BkOrigin_パラメーターで指定されたブックマークによって参照されている行がテーブルに存在しない場合、テーブルでブックマークの新しい位置を設定できない場合、 **FindRow**は MAPI_E_INVALID_BOOKMARK を返します。 _BkOrigin_によって参照される行が存在しなくなり、テーブルがブックマークの新しい位置を確立できる場合、 **FindRow**は MAPI_W_POSITION_CHANGED を返します。 
  
_BkOrigin_で渡されたブックマークが BOOKMARK_BEGINNING または BOOKMARK_END の**** いずれかである場合、一致する行が見つからない場合は MAPI_E_NOT_FOUND が返されます。 _BkOrigin_で使用されているブックマークが BOOKMARK_CURRENT の場合、 **FindRow**は MAPI_W_POSITION_CHANGED を返すことができますが、常に現在のカーソル位置があるため、MAPI_E_INVALID_BOOKMARK は返しません。 
  
**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) プロパティ列はすべてのテーブルに必要であり、PR_INSTANCE_KEY に基づいて行をシークする呼び出しをサポートするには、 **FindRow**のすべての実装が必要です。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**FindRow**によって実行されるプレフィックス検索の種類は、検索がテーブル組織と同じ方向にある場合にのみ役立ちます。 必要な動作を実現するために、プロパティ制限構造で渡された**RELOP_GE**によって暗黙的に指定された比較関数は、テーブルの並べ替え順序を基にした比較関数と同じである必要があります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**FindRow**を使用すると、ユーザーが入力した文字列 (特にアドレスダイアログボックス内のリストボックス) に基づいたスクロールをサポートできます。 この種類のスクロールでは、ユーザーは必要な文字列値のプレフィックスを徐々に入力し、 **FindRow**の呼び出しを定期的に発行して、プレフィックスに一致する最初の行にジャンプできます。 カーソルジャンプの方向は、検索を実行する方向によって決まります。 
  
**FindRow**を使用するには、ブックマークが設定されている必要があります。 文字列検索は、すべてのブックマーク (現在の位置と表の開始および終了を示す事前設定されたブックマークを含む) から開始できます。 テーブルに多数の行がある場合、検索操作に時間がかかることがあります。
  
次のようにスクロールする文字列プレフィックスを検索するには、制限を使用します。 昇順で並べ替えられた列の前方検索に対して、降順に並べ替えられた列の後方検索の場合は、 _lpRestriction_パラメータのプロパティ制限構造をリレーションシップ**RELOP_GE**に渡して、適切な_タグ_ **** __ とプレフィックスの形式を使用します。 
  
制限構造を使用してフィルターを指定する方法の詳細については、「[制限につい](about-restrictions.md)て」を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ContentsTableListCtrl  <br/> |dwthreadの loadtable  <br/> |mfcmapi は、 **IMAPITable:: FindRow**メソッドを使用して、制限に一致する行を検索します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SRestriction](srestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

