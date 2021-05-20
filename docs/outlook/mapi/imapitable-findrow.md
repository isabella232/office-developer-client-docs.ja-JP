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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a5364af229721d101f38d2f054f528169b48c09e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429573"
---
# <a name="imapitablefindrow"></a>IMAPITable::FindRow

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
特定の検索条件に一致するテーブル内の次の行を検索し、カーソルをその行に移動します。
  
```cpp
HRESULT FindRow(
LPSRestriction lpRestriction,
BOOKMARK BkOrigin,
ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpRestriction_
  
> [in]検索条件を記述 [する SRestriction](srestriction.md) 構造体へのポインター。 
    
 _BkOrigin_
  
> [in]FindRow が検索を開始する **行を** 識別するブックマーク。 ブックマークは [、IMAPITable::CreateBookmark](imapitable-createbookmark.md) メソッドを使用して作成するか、次のいずれかの定義済みの値を渡します。 
    
BOOKMARK_BEGINNING 
  
> テーブルの先頭から検索します。 
    
BOOKMARK_CURRENT 
  
> カーソルがあるテーブル内の行から検索します。 
    
BOOKMARK_END 
  
> テーブルの末尾から検索します。 
    
 _ulFlags_
  
> [in]検索の方向を制御するフラグのビットマスク。 次のフラグを設定できます。
    
DIR_BACKWARD 
  
> ブックマークで識別された行から後方に検索します。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 検索操作が成功しました。
    
MAPI_E_INVALID_BOOKMARK 
  
> _BkOrigin_ パラメーターのブックマークは、削除されたため、または要求された最後の行を超えているため無効です。 
    
MAPI_E_NOT_FOUND 
  
> 制限に一致する行が見つかりませんでした。
    
MAPI_W_POSITION_CHANGED
  
> 呼び出しは成功しましたが、操作で使用されるブックマークは、最後に使用された行と同じ行に設定されなくなりました。ブックマークが使用されていない場合、ブックマークは作成された位置と同じ位置になくなりました。 この警告が返されると、呼び出しは正常に処理されます。 この警告をテストするには、次のマクロ **HR_FAILED** します。 「エラー [処理のためのマクロの使用」を参照してください](using-macros-for-error-handling.md)。
    
## <a name="remarks"></a>注釈

**IMAPITable::FindRow** メソッドは _、lpRestriction_ パラメーターが指す **SRestriction** 構造で説明されている一連の検索条件に一致するように表の最初の行を検索します。 
  
通常 **、FindRow は** 指定したブックマークから前方に検索します。 呼び出し元は  _、ulFlags_ パラメーターで DIR_BACKWARDフラグを設定することで、ブックマークから後方に移動する検索を設定できます。 前方検索は、現在のブックマークから開始します。ブックマークの前の行から後方検索が開始されます。 検索の終了位置は、制限を満たした最初の行が見つかる直前です。 
  
_BkOrigin_ パラメーター内のブックマークが指す行がテーブルに存在しなくなった場合、テーブルはブックマークの新しい位置を確立できない場合 **、FindRow** は新しい位置をMAPI_E_INVALID_BOOKMARK。 _BkOrigin_ が指す行が存在しなくなった場合に、テーブルがブックマークの新しい位置を確立できる場合 **、FindRow** はブックマークをMAPI_W_POSITION_CHANGED。 
  
_BkOrigin_ で渡されたブックマークがBOOKMARK_BEGINNINGまたはBOOKMARK_END、一致する行MAPI_E_NOT_FOUND場合 **、FindRow** は値を返します。 _BkOrigin_ で使用されるブックマークが BOOKMARK_CURRENT の場合 **、FindRow** は常に現在のカーソル位置MAPI_W_POSITION_CHANGEDを返すが、MAPI_E_INVALID_BOOKMARK を返すことはありません。 
  
すべての **テーブルPR_INSTANCE_KEY** プロパティ ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) プロパティ列が必要であり **、FindRow** のすべての実装は、PR_INSTANCE_KEY に基づいて行を求める呼び出しをサポートするために必要です。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**FindRow** によって実行されるプレフィックス検索の種類は、検索がテーブルの組織と同じ方向に従う場合にのみ役立ちます。 必要な動作を実現するために、プロパティ制限構造で渡される **RELOP_GE** によって暗示される比較関数は、テーブルの並べ替え順序が基になるのと同じ比較関数である必要があります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**FindRow を使用すると**、特にアドレス ダイアログ ボックス内のリスト ボックスで、ユーザーが入力した文字列に基づいてスクロールをサポートできます。 この種類のスクロールでは、ユーザーは目的の文字列値の徐々に長いプレフィックスを入力し **、FindRow** 呼び出しを定期的に発行して、プレフィックスに一致する最初の行にジャンプできます。 カーソルがジャンプする方向は、検索を実行する方向によって異なります。 
  
**FindRow を使用するには、** ブックマークを設定する必要があります。 文字列検索は、現在の位置とテーブルの先頭と末尾を示す事前設定のブックマークを含む、任意のブックマークから発生する可能性があります。 テーブル内に多数の行がある場合、検索操作が遅くなる可能性があります。
  
次のようにスクロールする文字列プレフィックスを検索するには、制限を使用します。 昇順で並べ替えた列で順方向検索を行い、降順に並べ替えた列を逆方向に検索するには _、lpRestriction_ パラメーターのプロパティ制限構造を、関連付け **RELOP_GE** と適切なプロパティ タグとプレフィックスを使用して、形式タグ **GE** プレフィックスを使用して渡します。 
  
制限構造を使用してフィルターを指定する方法の詳細については、「 [制限について」を参照してください](about-restrictions.md)。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI は **IMAPITable::FindRow** メソッドを使用して、制限に一致する行を検索します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SRestriction](srestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

