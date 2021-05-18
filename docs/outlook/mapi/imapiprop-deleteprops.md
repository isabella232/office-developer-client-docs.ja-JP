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
  
オブジェクトから 1 つ以上のプロパティを削除します。 
  
```cpp
HRESULT DeleteProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>パラメーター

 _lpPropTagArray_
  
> [in]削除するプロパティを示すプロパティ タグの配列へのポインター。 _lpPropTagArray_ が指す [SPropTagArray](sproptagarray.md)構造体の **cValues** メンバーは 0 にし _、lpPropTagArray_ パラメーター自体は NULL にすることはできません。 
    
 _lppProblems_
  
> [in, out]入力時に [、SPropProblemArray](spropproblemarray.md) 構造体へのポインターを指すポインター。それ以外の場合は、エラー情報が不要な NULL を指定します。 _lppProblems が_ 入力の有効なポインターである場合 **、DeleteProps** は 1 つ以上のプロパティを削除するエラーに関する詳細情報を返します。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロパティが正常に削除されました。
    
MAPI_E_NO_ACCESS 
  
> 呼び出し元には、プロパティを削除するためのアクセス許可が不十分です。
    
## <a name="remarks"></a>注釈

**IMAPIProp::D eleteProps** メソッドは、現在のオブジェクトから 1 つ以上のプロパティを削除します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

すべてのオブジェクトからプロパティを削除できる必要はない。 オブジェクトが変更できない場合は **、DeleteProps** MAPI_E_NO_ACCESSを返します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_lpPropTagArray_ パラメーターが指すプロパティ タグ配列内の各プロパティ タグのプロパティの種類を設定する必要があります。 プロパティの種類は無視されます。プロパティ識別子だけが使用されます。 
  
一部のオブジェクトは変更を許可していないので、これらのオブジェクトは **DeleteProps** メソッドMAPI_E_NO_ACCESS返します。 その他のオブジェクトでは、一部のプロパティを削除できますが、他のプロパティは削除されません。 プロパティの一部のみを削除する際に問題が発生した場合 **、DeleteProps** はプロパティをS_OK。 _lppProblems_ パラメーターで有効なポインターを渡した場合 **、DeleteProps** は、各プロパティの問題に関する詳細情報を含む **SPropProblemArray** 構造体にポインターを設定します。 たとえば、メッセージのすべてのプロパティを削除し、1 つ以上の添付ファイルに問題がある場合 **、SPropProblemArray** 構造体には **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) プロパティのエントリが含まれます。 
  
_lppProblems_ が指す構造は **、DeleteProps** が値を返す場合にのみ有効S_OK。 **DeleteProps がエラー** を返す場合は **、SPropProblemArray 構造体の使用を試み** ない。 代わりに、オブジェクトの [IMAPIProp::GetLastError](imapiprop-getlasterror.md) メソッドを呼び出して、エラーの詳細を取得します。 
  
MAPIFreeBuffer 関数を呼び出して、返された[SPropProblemArray 構造体を解放](mapifreebuffer.md)します。  
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |DeleteProperty  <br/> |MFCMAPI は **IMAPIProp::D eleteProps** メソッドを使用して、オブジェクトからプロパティを削除します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

