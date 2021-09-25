---
title: IMAPIPropSetProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp.SetProps
api_type:
- COM
ms.assetid: 49f007c9-42e5-4391-8b83-988c9b0ebdba
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3d010d325f0668d2ab638544bc02713817491300
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584445"
---
# <a name="imapipropsetprops"></a>IMAPIProp::SetProps

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1 つ以上のプロパティを更新します。
  
```cpp
HRESULT SetProps(
  ULONG cValues,
  LPSPropValue lpPropArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>パラメーター

 _cValues_
  
> [in]  _lpPropArray_ パラメーターが指すプロパティ値の数。 _cValues パラメーター_ は 0 にすることはできません。 
    
 _lpPropArray_
  
> [in]更新するプロパティ値を含む [SPropValue](spropvalue.md) 構造体の配列へのポインター。 
    
 _lppProblems_
  
> [in, out]入力時に [、SPropProblemArray](spropproblemarray.md) 構造体へのポインターを指すポインター。それ以外の場合は、エラー情報が不要であることを示す NULL。 _lppProblems が_ 入力の有効なポインターである場合 **、SetProps** は 1 つ以上のプロパティを更新するエラーに関する詳細情報を返します。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロパティが正常に更新されました。
    
次の値は **、SPropProblemArray** 構造体で返されますが、SetProps の戻り値 **として返す値として返す必要があります**。
  
MAPI_E_BAD_CHARWIDTH 
  
> このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。
    
MAPI_E_COMPUTED 
  
> プロパティは、オブジェクトを担当するサービス プロバイダーによって計算される読み取り専用のため、更新できません。
    
MAPI_E_INVALID_TYPE 
  
> プロパティの種類が無効です。
    
MAPI_E_NO_ACCESS 
  
> 読み取り専用オブジェクトを変更しようとしたり、ユーザーのアクセス許可が不十分なオブジェクトにアクセスしようとしたりしました。
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> リモート プロシージャ 呼び出し (RPC) バッファー サイズよりも大きいので、プロパティを更新できません。
    
MAPI_E_UNEXPECTED_TYPE 
  
> プロパティの種類は、呼び出し元の実装で予期される型ではありません。
    
## <a name="notes-to-implementers"></a>実装に関するメモ

プロパティ **タグPR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) プロパティ タグおよびプロパティの種類を持つすべてのプロパティを **無視** PT_ERROR。 **SPropProblemArray** 構造体に変更を加え、問題を報告したりしない。 
  
プロパティMAPI_E_INVALID_PARAMETER値の配列 **に型の** プロパティPT_OBJECT含まれている場合は、この値を返します。 配列に複数値のプロパティが含まれていて、その **cValues** メンバーが 0 に設定されている場合も、このエラーを返します。 
  
呼び出しが全体的に成功したが、一部のプロパティの設定に問題がある場合は、S_OK を返し _、lppProblems_ パラメーターが示す **SPropProblemArray** 構造体の適切なエントリに問題に関する情報を入力します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

サービス プロバイダーによっては、特定のプロパティ識別子で以前に使用された型とは異なる型を含むプロパティ タグを渡して、プロパティの種類を変更できる場合があります。
  
オブジェクトでサポートされていないプロパティのプロパティ タグを含め **、SetProps** の実装によって新しいプロパティを作成できる場合、プロパティはオブジェクトに追加されます。 新しいプロパティに使用されたプロパティ識別子と一緒に格納された以前の値は破棄されます。 
  
戻り値S_OK、すべてのプロパティが正常に更新されたことを保証するものではありません。 一部のプロバイダーは [、IMAPIProp::SaveChanges](imapiprop-savechanges.md)や [IMAPIProp::GetProps](imapiprop-getprops.md)などのプロバイダーの介入を必要とする呼び出しを受信するまで **、SetProps** 呼び出しをキャッシュします。 したがって **、SetProps** 呼び出しに関連するエラー値を、後の呼び出しで受け取ることができます。 
  
**SetProps が** S_OKを返す場合は _、lppProblems_ が示す **SPropProblemArray** 構造体で、個々のプロパティの更新に関する問題を確認します。 **SetProps がエラー** を返す場合は、プロパティの問題の配列をチェックしない。 代わりに、オブジェクトの [IMAPIProp::GetLastError メソッドを呼び出](imapiprop-getlasterror.md) します。 
  
大規模なプロパティを更新すると **、SetProps が** 失敗し、エラーが発生MAPI_E_NOT_ENOUGH_MEMORY。 プロパティの最大サイズはありません。また、オブジェクトによって制限が異なる場合があります。 潜在的に大きいプロパティを処理する場合は **、SetProps** がこのエラー値を返す場合、インターフェイス識別子として IID_IStream を使用して [IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出す準備をしてください。 
  
[MAPIFreeBuffer 関数を呼び出](mapifreebuffer.md)して **、SPropProblemArray 構造体を解放** します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|PropertyEditor.cpp  <br/> |CPropertyEditor::WriteSPropValueToObject  <br/> |MFCMAPI は **IMAPIProp::SetProps** メソッドを使用して、プロパティの編集後にプロパティをオブジェクトに書き戻します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropValue](spropvalue.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)

