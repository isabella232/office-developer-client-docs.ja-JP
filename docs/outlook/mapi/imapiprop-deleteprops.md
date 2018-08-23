---
title: IMAPIPropDeleteProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.DeleteProps
api_type:
- COM
ms.assetid: 5cc642de-21f0-4826-bf21-aac4bcfc1328
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8eb19f9a2d3458e153b0758b56c502ce612be0cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800667"
---
# <a name="imapipropdeleteprops"></a>IMAPIProp::DeleteProps

  
  
**適用対象**: Outlook 
  
オブジェクトから 1 つまたは複数のプロパティを削除します。 
  
```cpp
HRESULT DeleteProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>�p�����[�^�[

 _lpPropTagArray_
  
> [in]削除するにはプロパティを指定するプロパティ タグの配列へのポインター。 _LpPropTagArray_で示される[SPropTagArray](sproptagarray.md)構造体の**あう**メンバーが 0 でなければできませんし、 _lpPropTagArray_パラメーター自体を NULL にする必要があることはできません。 
    
 _lppProblems_
  
> [で [チェック アウト][SPropProblemArray](spropproblemarray.md)構造体へのポインターへのポインターの入力でそれ以外の場合、NULL、エラー情報の必要性がないことを示します。 _LppProblems_が入力時に有効なポインターである場合は、 **DeleteProps**は、1 つまたは複数のプロパティを削除中にエラーに関する詳細な情報を返します。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> プロパティは正常に削除されました。
    
MAPI_E_NO_ACCESS 
  
> 呼び出し側では、プロパティを削除するのには十分なアクセス許可を持っています。
    
## <a name="remarks"></a>注釈

**IMAPIProp::DeleteProps**メソッドは、現在のオブジェクトから 1 つまたは複数のプロパティを削除します。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

すべてのオブジェクトから削除するプロパティを許可する必要はありません。 オブジェクトが変更可能でない場合は、 **DeleteProps**メソッドから MAPI_E_NO_ACCESS を返します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_LpPropTagArray_パラメーターで指定されたプロパティ タグ配列内の各プロパティ タグのプロパティの型を設定する必要はありません。 プロパティの型は無視されます。プロパティの識別子だけが使用されます。 
  
いくつかのオブジェクトは、変更を許可しないことと、これらのオブジェクトの**DeleteProps**メソッドから MAPI_E_NO_ACCESS を返すことに注意します。 その他のオブジェクトは、いくつかのプロパティを削除するには、それ以外を使用します。 プロパティの一部のみを削除中に問題がある場合は、 **DeleteProps**は、S_OK を返します。 _LppProblems_パラメーターに有効なポインターを渡した場合**DeleteProps**は各プロパティを使用して問題に関する詳細情報を含む**SPropProblemArray**構造体へのポインターを設定します。 などのすべてのメッセージのプロパティを削除する 1 つまたは複数の添付ファイルの問題がある場合は、 **SPropProblemArray**構造体エントリが記録の**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) プロパティです。 
  
_LppProblems_が指す構造体は**DeleteProps**には、S_OK が返された場合です。 **DeleteProps**がエラーを返した場合に**SPropProblemArray**構造体を使用しないでください。 代わりに、エラーに関する詳細情報を取得するのには、オブジェクトの[IMAPIProp::GetLastError](imapiprop-getlasterror.md)メソッドを呼び出します。 
  
[MAPIFreeBuffer](mapifreebuffer.md)関数の呼び出しによって返された**SPropProblemArray**構造体を解放します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |DeleteProperty  <br/> |MFCMAPI では、 **IMAPIProp::DeleteProps**メソッドを使用して、オブジェクトからプロパティを削除します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

