---
title: IMAPIPropSetProps
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 304295e3ac77fb67ec5875620a7a269377b542c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800658"
---
# <a name="imapipropsetprops"></a>IMAPIProp::SetProps

  
  
**適用されます**: Outlook 
  
1 つまたは複数のプロパティを更新します。
  
```cpp
HRESULT SetProps(
  ULONG cValues,
  LPSPropValue lpPropArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parameters

 _あう_
  
> [in]_LpPropArray_パラメーターで指定されたプロパティ値の数。 _あう_パラメーターを 0 にする必要がありますはできません。 
    
 _lpPropArray_
  
> [in]更新するプロパティの値を含む[SPropValue](spropvalue.md)構造体の配列へのポインター。 
    
 _lppProblems_
  
> [で [チェック アウト][SPropProblemArray](spropproblemarray.md)構造体へのポインターへのポインターの入力でそれ以外の場合、NULL の場合、エラー情報の必要性がないことを示します。 _LppProblems_が入力時に有効なポインターである場合は、 **SetProps**は、1 つまたは複数のプロパティを更新中にエラーに関する詳細な情報を返します。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> プロパティは正常に更新されました。
    
次の値が返される、 **SPropProblemArray**構造体には戻り値としてではなく**SetProps**。
  
MAPI_E_BAD_CHARWIDTH 
  
> か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。
    
MAPI_E_COMPUTED 
  
> 読み取り専用オブジェクトを担当するサービス ・ プロバイダーによって計算されるため、プロパティを更新できません。
    
MAPI_E_INVALID_TYPE 
  
> プロパティの型が正しくありません。
    
MAPI_E_NO_ACCESS 
  
> しようとは、読み取り専用オブジェクトを変更するか、ユーザーが十分なアクセス許可を持っているオブジェクトへのアクセスにしました。
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> プロパティは、リモート プロシージャ コール (RPC) のバッファー サイズを超えているために更新できません。
    
MAPI_E_UNEXPECTED_TYPE 
  
> プロパティの型は、呼び出し元の実装の型ではありません。
    
## <a name="notes-to-implementers"></a>実装者へのメモ

**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) のプロパティ タグと**PT_ERROR**の型を持つすべてのプロパティを無視します。 **SPropProblemArray**構造の変更や問題の報告は行いません。 
  
**PT_OBJECT**の型のプロパティは、プロパティ値の配列に含まれている場合は、MAPI_E_INVALID_PARAMETER を返します。 複数値プロパティは、配列と**あう**メンバーに含まれている場合、このエラーは 0 に設定を返します。 
  
全体の呼び出しが成功すると、一部のプロパティの設定に問題がある場合は、S_OK を返すし、 _lppProblems_パラメーターが指す**SPropProblemArray**構造体の適切なエントリで、問題に関する情報を格納します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

サービス プロバイダーによって指定されたプロパティの識別子を使用していたよりも、別の種類を含むプロパティ タグを渡すことによってプロパティの型を変更することがあります。
  
オブジェクトでサポートされていないプロパティのプロパティ タグを含めるし、 **SetProps**の実装では、新しいプロパティの作成、プロパティがオブジェクトに追加されます。 新しいプロパティのために使用されたプロパティの識別子が格納されている、以前の値は破棄されます。 
  
S_OK の戻り値が正常に更新されたすべてのプロパティを保証していないことに注意します。 一部のプロバイダーは、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)や[IMAPIProp::GetProps](imapiprop-getprops.md)などのプロバイダーの介入が必要な呼び出しを受け取るまで、 **SetProps**呼び出しをキャッシュします。 したがって、以降の呼び出しで**SetProps**の呼び出しに関連するエラー値を受け取ることが。 
  
**SetProps**には、S_OK が返された場合は、個々 のプロパティの更新に問題の_lppProblems_が指す**SPropProblemArray**の構造体を確認してください。 **SetProps**がエラーを返した場合、プロパティの問題の配列をチェックすることはしません。 オブジェクトの[IMAPIProp::GetLastError](imapiprop-getlasterror.md)メソッドを呼び出す代わりに、します。 
  
大きなプロパティを更新するとき**SetProps**は失敗し、MAPI_E_NOT_ENOUGH_MEMORY を返すことができます。 プロパティの最大サイズがないと、さまざまなオブジェクトは、さまざまな制限を持つことができます。 大きな可能性のあるプロパティを扱う場合は、 **SetProps**がこのエラーの値を返す場合は、インターフェイス識別子として IID_IStream と[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出すように準備します。 
  
**SPropProblemArray**構造体を解放する[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|PropertyEditor.cpp  <br/> |CPropertyEditor::WriteSPropValueToObject  <br/> |MFCMAPI では、プロパティに書き込むオブジェクトのプロパティが編集された後に、 **IMAPIProp::SetProps**メソッドを使用します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropValue](spropvalue.md)
  
[IMAPIProp: IUnknown](imapipropiunknown.md)

