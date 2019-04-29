---
title: imapipropsetprops
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.SetProps
api_type:
- COM
ms.assetid: 49f007c9-42e5-4391-8b83-988c9b0ebdba
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 87709f8a77471637d7652982669bcba93ca2e1dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412619"
---
# <a name="imapipropsetprops"></a>IMAPIProp::SetProps

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1つまたは複数のプロパティを更新します。
  
```cpp
HRESULT SetProps(
  ULONG cValues,
  LPSPropValue lpPropArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>パラメーター

 _cvalues_
  
> 順番_lpproparray_パラメーターが指すプロパティ値の数。 _cvalues_パラメーターは0以外でなければなりません。 
    
 _lpproparray_
  
> 順番更新するプロパティ値を含む[spropvalue](spropvalue.md)構造体の配列へのポインター。 
    
 _lppproblems 問題_
  
> [入力]input の場合は、 [spropの配列](spropproblemarray.md)構造体へのポインターへのポインターを返します。それ以外の場合、エラー情報を必要としないことを示す NULL。 _lppproblems_が入力の有効なポインターである場合、 **setprops**は、1つ以上のプロパティの更新中に発生したエラーに関する詳細情報を返します。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロパティが正常に更新されました。
    
次の値は、 **spropの配列**構造で返すことができますが、 **setprops**の戻り値としては返されません。
  
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。
    
MAPI_E_COMPUTED 
  
> プロパティは読み取り専用で、オブジェクトを処理するサービスプロバイダーによって計算されるため、更新できません。
    
MAPI_E_INVALID_TYPE 
  
> プロパティの種類が無効です。
    
MAPI_E_NO_ACCESS 
  
> 読み取り専用オブジェクトを変更しようとしたか、またはユーザーが十分なアクセス許可を持っていないオブジェクトにアクセスしようとしました。
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> このプロパティは、リモートプロシージャコール (RPC) のバッファーサイズよりも大きいため、更新できません。
    
MAPI_E_UNEXPECTED_TYPE 
  
> プロパティの型は、呼び出し元の実装で想定される型ではありません。
    
## <a name="notes-to-implementers"></a>実装に関するメモ

**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) プロパティタグと、 **PT_ERROR**型のすべてのプロパティを無視します。 **sprop問題の配列**構造で、変更を加えたり、問題を報告したりしないでください。 
  
プロパティ値の配列に**PT_OBJECT**型のプロパティが含まれている場合は、MAPI_E_INVALID_PARAMETER を返します。 また、複数値のプロパティが配列に含まれており、その**cvalues**メンバーが0に設定されている場合にも、このエラーを返します。 
  
呼び出しが全体的に成功しても、一部のプロパティの設定に問題がある場合は、S_OK を返し、 _lppproblems_パラメーターが指す**sprop問題の配列**構造の適切なエントリに問題に関する情報を格納します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

また、サービスプロバイダーによっては、プロパティの種類を変更できるようにするために、特定のプロパティ識別子で以前に使用されていたのとは異なる種類のプロパティタグを渡すことができます。
  
オブジェクトでサポートされていないプロパティのプロパティタグを指定し、 **setprops**の実装で新しいプロパティを作成できる場合、プロパティはオブジェクトに追加されます。 新しいプロパティに使用されたプロパティ識別子に格納されていた以前の値は、すべて破棄されます。 
  
S_OK 戻り値は、すべてのプロパティが正常に更新されたことを保証するものではないことに注意してください。 一部のプロバイダーは、 **setprops**呼び出しを受信するまで、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)または[imapiprop:: GetProps](imapiprop-getprops.md)などのプロバイダーの介入を必要とする呼び出しを受け取るまでキャッシュします。 そのため、以降の呼び出しで**setprops**呼び出しに関連するエラー値を受け取ることができます。 
  
**setprops**が S_OK を返す場合は、個々のプロパティの更新時に問題が発生したことを確認するために、 _lppproblems_に示されている**sprop問題の配列**構造を確認します。 **setprops**がエラーを返す場合は、プロパティの問題の配列をチェックしません。 代わりに、オブジェクトの[imapiprop:: GetLastError](imapiprop-getlasterror.md)メソッドを呼び出します。 
  
大きなプロパティを更新する場合、 **setprops**は失敗して MAPI_E_NOT_ENOUGH_MEMORY を返します。 プロパティの最大サイズはありません。また、オブジェクトごとに異なる制限を設定することもできます。 大きなプロパティを処理する場合は、 **setprops**がこのエラー値を返す場合、IID_IStream をインターフェイス識別子として使用して、 [imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出すように準備してください。 
  
[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、 **spropの配列**構造を解放します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|propertyeditor .cpp  <br/> |cpropertyeditor:: writespropvaluetoobject  <br/> |mfcmapi は、 **imapiprop:: setprops**メソッドを使用して、プロパティが編集された後、そのプロパティをオブジェクトに書き戻します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropValue](spropvalue.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)

