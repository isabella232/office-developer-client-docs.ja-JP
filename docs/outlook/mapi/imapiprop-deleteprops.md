---
title: imapipropdeleteprops
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5bfef87baa2dffa4605f9a7afa3833024f514430
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409238"
---
# <a name="imapipropdeleteprops"></a>IMAPIProp::DeleteProps

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトから1つ以上のプロパティを削除します。 
  
```cpp
HRESULT DeleteProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>パラメーター

 _lpPropTagArray_
  
> 順番削除するプロパティを示すプロパティタグの配列へのポインター。 _lpPropTagArray_によって参照される[SPropTagArray](sproptagarray.md)構造の**cvalues**メンバーは0であってはなりません。また、 _lpPropTagArray_パラメーター自体を NULL にすることはできません。 
    
 _lppproblems 問題_
  
> [入力]input の場合は、 [spropの配列](spropproblemarray.md)構造体へのポインターへのポインターを返します。それ以外の場合は、エラー情報を必要としないことを示す NULL。 _lppproblems_が入力の有効なポインターの場合、 **deleteprops**は、1つ以上のプロパティを削除するときのエラーについての詳細情報を返します。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロパティが正常に削除されました。
    
MAPI_E_NO_ACCESS 
  
> 呼び出し元に、プロパティを削除するための十分な権限がありません。
    
## <a name="remarks"></a>注釈

**imapiprop::D eleteprops**メソッドは、現在のオブジェクトから1つ以上のプロパティを削除します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

すべてのオブジェクトからプロパティを削除できるようにする必要はありません。 オブジェクトが変更できない場合は、 **deleteprops**メソッドから MAPI_E_NO_ACCESS を返します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_lpPropTagArray_パラメーターによって示されるプロパティタグ配列内の各 property タグに対して、プロパティの種類を設定する必要はありません。 プロパティの種類は無視されます。プロパティ識別子のみが使用されます。 
  
一部のオブジェクトは変更を許可しないため、これらのオブジェクトは**deleteprops**メソッドから MAPI_E_NO_ACCESS を返すことに注意してください。 その他のオブジェクトでは、一部のプロパティを削除できますが、他のオブジェクトを削除することはできません。 一部のプロパティの削除のみで問題が発生した場合、 **deleteprops**は S_OK を返します。 _lppproblems_パラメーターで有効なポインターを渡した場合、 **deleteprops**は、各プロパティの問題に関する詳細情報を含む**sprop問題の配列**構造体へのポインターを設定します。 たとえば、メッセージのすべてのプロパティを削除していて、その1つ以上の添付ファイルに問題がある場合、 **sprop問題の配列**構造には、 **PR_MESSAGE_ATTACHMENTS** (PidTagMessageAttachments のエントリが含まれます。[](pidtagmessageattachments-canonical-property.md)) プロパティ。 
  
_lppproblems_が指す構造体は、 **deleteprops**が S_OK を返す場合にのみ有効です。 **deleteprops**がエラーを返す場合は、sprop問題の**配列**構造を使用しないようにしてください。 代わりに、オブジェクトの[imapiprop:: GetLastError](imapiprop-getlasterror.md)メソッドを呼び出して、エラーに関する詳細情報を取得します。 
  
[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことで、返された**spropの配列**構造を解放します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFunctions  <br/> |DeleteProperty  <br/> |mfcmapi は、 **imapiprop::D eleteprops**メソッドを使用して、オブジェクトからプロパティを削除します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

