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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: cb777074d1657a3ee5c2f1e9f70d2b304858c1b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800832"
---
# <a name="imapitablefindrow"></a>IMAPITable::FindRow

  
  
**適用されます**: Outlook 
  
特定の検索条件に一致し、その行にカーソルを移動するテーブル内の次の行を検索します。
  
```cpp
HRESULT FindRow(
LPSRestriction lpRestriction,
BOOKMARK BkOrigin,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpRestriction_
  
> [in]検索条件を記述する[SRestriction](srestriction.md)構造体へのポインター。 
    
 _BkOrigin_
  
> [in]**FindRow**が検索を開始する位置を示す行を識別するブックマークです。 、 [IMAPITable::CreateBookmark](imapitable-createbookmark.md)メソッドを使用してブックマークを作成することができますか、次の定義済み値の 1 つ渡すことができます。 
    
BOOKMARK_BEGINNING 
  
> テーブルの先頭から検索します。 
    
BOOKMARK_CURRENT 
  
> カーソルが配置されているテーブルの行を検索します。 
    
BOOKMARK_END 
  
> テーブルの最後から検索します。 
    
 _ulFlags_
  
> [in]検索の方向を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
DIR_BACKWARD 
  
> ブックマークで識別される行から逆方向に検索します。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 検索操作が正常に完了しました。
    
MAPI_E_INVALID_BOOKMARK 
  
> 削除されているため、または要求された最後の行を越えることがあるために、 _BkOrigin_パラメーター内のブックマークは無効です。 
    
MAPI_E_NOT_FOUND 
  
> 制限に一致する行が見つかりませんでした。
    
MAPI_W_POSITION_CHANGED
  
> 呼び出しが成功したが、ときに最後に使用されたのと同じ行に、操作で使用するブックマークが設定されていません。ブックマークが使用されていない場合は不要になったと同じ位置に作成されたとき この警告が返されると、呼び出しを成功として処理する必要があります。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 [エラー処理のためのマクロを使用する](using-macros-for-error-handling.md)を参照してください。
    
## <a name="remarks"></a>備考

**IMAPITable::FindRow**メソッドは、 _lpRestriction_パラメーターが指す**SRestriction**構造で説明されている検索条件のセットに一致するテーブル内の最初の行を検索します。 
  
通常、 **FindRow**は指定されたブックマークから順方向に検索します。 _UlFlags_パラメーターに DIR_BACKWARD フラグを設定することで、ブックマークから後方へ移動するのには検索、呼び出し元を設定します。 現在のブックマークの開始方向へ検索しますブックマークより前の行から下方向へ検索を開始します。 検索の終了位置は、制限を満たす最初の行が見つかる前にだけです。 
  
そのブックマークは、 _BkOrigin_パラメーターで指定された行がテーブルに存在しないテーブルは、新しいブックマークの位置を確立できない場合、 **FindRow**は MAPI_E_INVALID_BOOKMARK を返します。 _BkOrigin_で指定された行が存在しないテーブルは、新しいブックマークの位置を確立することが場合、 **FindRow**は MAPI_W_POSITION_CHANGED を返します。 
  
_BkOrigin_に渡されるブックマークが BOOKMARK_BEGINNING または BOOKMARK_END のいずれかの場合、 **FindRow**は、一致する行が見つからない場合は MAPI_E_NOT_FOUND を返します。 _BkOrigin_で使用されているブックマークが BOOKMARK_CURRENT である場合、 **FindRow**は必要は常に、現在のカーソル位置があるため MAPI_W_POSITION_CHANGED が MAPI_E_INVALID_BOOKMARK ではないと返すことができます。 
  
**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) のプロパティ列は、他のすべてのテーブルに必要な**FindRow**のすべての実装は、PR_INSTANCE_KEY に基づいている行をシークの呼び出しをサポートする必要が. 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

**FindRow**によって実行されるプレフィックスの検索の型は、テーブルの構成と同じ方向に依存して、検索するときにのみ役立ちます。 必要な動作を実現するためにプロパティ制限の構造体に渡された**RELOP_GE**によって暗黙的に指定の比較関数に同じ比較関数がテーブルの並べ替え順序を基になることがあります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**FindRow**を使用すると、特にアドレス] ダイアログ ボックス内のリスト ボックスで、ユーザーが入力した文字列のスクロールをサポートします。 この種類のスクロールでは、ユーザー入力、目的の文字列値のプレフィックスを徐々 に長く、および**FindRow**の呼び出しのプレフィックスに一致する最初の行にジャンプするのには定期的に発行することができます。 検索依存のどちらの方向にカーソルが移動する方向は、実行に設定されています。 
  
**FindRow**を使用するには、ブックマークを設定する必要があります。 現在の位置の先頭と末尾の表に示す既定のブックマークを含む、任意のブックマークから開始できるは、文字列の検索します。 テーブル内の行の数が多い場合は、検索操作が遅くなることがあります。
  
制限を使用すると、次のようにスクロールするための文字列の接頭辞を検索できます。 前方の昇順で並べ替えられた列で検索し、降順で並べ替えられた列の後方に検索するための関係の**RELOP_GE**に_lpRestriction_パラメーターは、適切なプロパティ制限構造体を渡しプロパティ タグと_タグ_ **GE**の形式_のプレフィックス_を使用して、プレフィックス。 
  
フィルターを指定する構造体の制限の使用に関する詳細については、[制限の詳細](about-restrictions.md)を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI では、 **IMAPITable::FindRow**メソッドを使用して、制約に一致する行を検索します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SRestriction](srestriction.md)
  
[IMAPITable: IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

