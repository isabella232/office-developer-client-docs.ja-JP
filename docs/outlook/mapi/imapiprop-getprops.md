---
title: IMAPIPropGetProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetProps
api_type:
- COM
ms.assetid: 1c7a9cd2-d765-4218-9aee-52df1a2aae6c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9b03775d495f7d1f51142eb0ed06fc9ecdf6d1a3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412458"
---
# <a name="imapipropgetprops"></a>IMAPIProp::GetProps

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトの1つ以上のプロパティのプロパティ値を取得します。
  
```cpp
HRESULT GetProps(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppPropArray
);
```

## <a name="parameters"></a>パラメーター

 _lpPropTagArray_
  
> 順番値を取得するプロパティを識別するプロパティタグの配列へのポインター。 _lpPropTagArray_パラメーターは、オブジェクトのすべてのプロパティの値を返す必要があるか、または1つ以上の property タグを含む[SPropTagArray](sproptagarray.md)構造をポイントする必要があることを示す NULL である必要があります。 
    
 _ulFlags_
  
> 順番PT_UNSPECIFIED 型のプロパティの形式を示すフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> これらのプロパティの文字列値は、Unicode 形式で返される必要があります。 MAPI_UNICODE フラグが設定されていない場合、文字列値は ANSI 形式で返されます。
    
 _lpcValues_
  
> 読み上げ_lppproparray_パラメーターが指すプロパティ値の数へのポインター。 _lppproparray_が NULL の場合、 _lpcValues_パラメーターの内容は0になります。 
    
 _lppproparray_
  
> 読み上げ取得したプロパティ値へのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロパティの値が正常に取得されました。
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しは全体的に成功しましたが、1つ以上のプロパティにアクセスできませんでした。 使用できない各プロパティのプロパティ値の**aulPropTag**メンバには、プロパティの種類が PT_ERROR で、識別子が0になっています。 この警告が返された場合、呼び出しは正常に処理されます。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。
    
MAPI_E_INVALID_PARAMETER 
  
> _lpPropTagArray_で参照されている**SPropTagArray**構造の**cvalues**メンバーに0が渡されました。
    
## <a name="remarks"></a>注釈

**imapiprop:: GetProps**メソッドは、オブジェクトの1つ以上のプロパティのプロパティ値を取得します。 
  
プロパティ値は、要求されたときと同じ順序で返されます (つまり、 _lpPropTagArray_によって参照されているプロパティタグ配列内のプロパティの順序は、lppproparray が指すプロパティ値構造の配列内の順序と一致します) __). 
  
property タグ配列の**aulPropTag**メンバーで指定されているプロパティの種類は、各プロパティの値構造の**value**メンバーで返される値の種類を示します。 ただし、呼び出し元がプロパティの型を知らない場合は、代わりに**aulPropTag**メンバーの型を PT_UNSPECIFIED に設定できます。 **GetProps**は、値を取得するときに、プロパティのプロパティ値構造の**aulPropTag**メンバーで適切な型を設定します。 
  
プロパティの種類が_lpPropTagArray_の**SPropTagArray**で指定されている場合、 _lppproparray_に返される**spropvalue**のプロパティ値は、エラー値が返されない限り、要求された型と正確に一致する型を持っています。その代わりに。 
  
文字列プロパティには、次の2つのプロパティの種類のいずれかを指定できます: PT_UNICODE は、UNICODE 形式と PT_STRING8 を表す ANSI 形式を表します。 MAPI_UNICODE フラグが_ulflags_パラメーターで設定されている場合は、 **GetProps**が文字列プロパティの適切な形式を決定できないときに、その値を UNICODE 形式で返します。 **GetProps**は、次の状況では、正確な文字列プロパティの種類を特定できません。 
  
- _lpPropTagArray_パラメーターは、すべてのプロパティを要求するために NULL に設定されています。 
    
- **aulPropTag**メンバーには、プロパティのタグ配列に、プロパティの型として PT_UNSPECIFIED 値が含まれています。 
    
オブジェクトのすべてのプロパティを取得するために_lpPropTagArray_パラメーターが NULL に設定されていて、プロパティが存在しない場合、 **GetProps**は次の処理を行います。 
  
- S_OK を返します。
    
- プロパティ値構造の**cvalues**メンバーの count 値を0に設定します。 
    
- _lpcValues_の内容を0に設定します。 
    
- _lppproparray_を NULL に設定します。 
    
 **GetProps**は、 **cvalues**が0に設定された複数値のプロパティを返すことはできません。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

[MAPIAllocateBuffer](mapiallocatebuffer.md)関数を呼び出して、 _lpPropTagArray_によってポイントされている[spropvalue](spropvalue.md)構造体の初期メモリを割り当てます。[MAPIAllocateMore](mapiallocatemore.md)を呼び出して、構造体のメンバーに必要な追加メモリを割り当てます。 
  
要求された1つ以上のプロパティの値を取得できない場合は、MAPI_W_ERRORS_RETURNED を返します。 プロパティ値の構造で、 **aulPropTag**メンバーの型を PT_ERROR に設定し、 **value**メンバーを、エラーを説明する状態コードに設定します。 たとえば、文字列を unicode に変換する必要があり、unicode をサポートしていない場合は、 **Value**メンバーを MAPI_E_BAD_CHARWIDTH に設定します。 プロパティが大きすぎる場合は、MAPI_E_NOT_ENOUGH_MEMORY に設定します。 オブジェクトがプロパティをサポートしていない場合は、MAPI_E_NOT_FOUND に設定します。 
  
リモートトランスポートプロバイダーの**GetProps**メソッドの実装は、呼び出し元によって要求されたプロパティのフォルダーのプロパティ値を返す必要があります。 実装では、次のことを行う必要があります。 
  
- 呼び出し元に返されるプロパティ値の配列を割り当て、そのアドレスを、その目的のために渡されたプロパティ値ポインターパラメーターに格納します。
    
- **GetProps**に渡されたプロパティタグの配列に従って、フォルダーのプロパティのプロパティタグを、プロパティの値の配列のプロパティタグにコピーします。
    
- **GetProps**に渡されるすべてのプロパティタグについて、プロパティの型が設定されていることを確認します。 呼び出し元は、PT_UNSPECIFIED のプロパティの種類を渡すことができます。この場合、 **GetProps**は、そのプロパティタグに適切なプロパティの種類を設定する必要があります。 
    
- プロパティ値配列の各プロパティの値をタグに従って設定します。 たとえば、呼び出し元によって要求されたプロパティタグが**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) である場合、 **GetProps**は値を MAPI_FOLDER に設定できます。 
    
- 呼び出し元が、実装で処理されていないプロパティタグを渡した場合は、そのプロパティのプロパティタグを PT_ERROR に設定し、プロパティ値を MAPI_E_NOT_FOUND に設定します。
    
- エラーが発生しなかった場合は S_OK を返し、エラーが発生した場合は MAPI_W_ERRORS_RETURNED を返します。
    
リモートトランスポートプロバイダーの**GetProps**メソッドの実装では、少なくとも次のプロパティをサポートする必要があります。 
  
- **PR_ACCESS**([PidTagAccess](pidtagaccess-canonical-property.md))
    
- **PR_ACCESS_LEVEL**([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))
    
- **PR_ASSOC_CONTENT_COUNT**([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))
    
- **PR_CONTENT_COUNT**([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CREATION_TIME**([PidTagCreationTime](pidtagcreationtime-canonical-property.md))
    
- **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_FOLDER_TYPE**([PidTagFolderType](pidtagfoldertype-canonical-property.md))
    
- **PR_OBJECT_TYPE**
    
- **PR_SUBFOLDERS**([PidTagSubfolders](pidtagsubfolders-canonical-property.md))
    
## <a name="notes-to-callers"></a>呼び出し側への注意

PT_OBJECT 型のプロパティの場合は、 **GetProps**ではなく、 [imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出します。 
  
セキュリティで保護されたプロパティの場合は、 _lppPropTagArray_パラメーターを NULL に設定して**GetProps**を呼び出すことによって、プロパティを取得する必要はありません。 **GetProps**を呼び出すときには、そのプロパティタグ配列の**aulPropTag**メンバーで、セキュリティで保護されたプロパティの識別子を明示的に設定する必要があります。 セキュリティで保護されたプロパティを使用可能にする時期と方法は、サービスプロバイダーによって設定されます。 
  
**GetProps**が S_OK または MAPI_W_ERRORS_RETURNED を返す場合にのみ、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことで、返される**spropvalue**構造を解放します。 
  
1つ以上のプロパティにアクセスできなかったために**GetProps**が MAPI_W_ERRORS_RETURNED を返す場合は、返されたプロパティのプロパティタグを確認してください。 失敗したプロパティの値は、プロパティの値の構造に次の値が設定されます。 
  
- **aulPropTag**メンバーのプロパティの型が PT_ERROR に設定されます。 
    
- **value**メンバーのプロパティ値がエラーの状態コードに設定されています (MAPI_E_NOT_FOUND など)。 
    
プロパティの値の構造体に返されるのが非常に大きいために失敗するプロパティは、その**値**のメンバーが MAPI_E_NOT_ENOUGH_MEMORY に設定されています。 通常、このエラーは、プロパティの値が 4 KB 以上の場合に、PT_STRING8、PT_UNICODE、または PT_BINARY 型の文字列またはバイナリのプロパティを使用して発生します。 大きなプロパティを取得するには、 **imapiprop:: openproperty**を呼び出します。 
  
**GetProps**のすべての実装で、文字列の Unicode 形式と ANSI 形式の両方をサポートしているわけではありません。 特定のプロパティが文字列形式の変換を必要とし、 **GetProps**がそれをサポートできない場合、プロパティの**値**のメンバーは MAPI_E_BAD_CHARWIDTH に設定されます。 
  
pst が SharePoint pst であるかどうかを確認するには、 [imapisession:: openmsgstore](imapisession-openmsgstore.md)を使用して pst をマウントし、このプロパティを要求しているメッセージストアオブジェクトで**GetProps**を呼び出します。 存在する場合は、SharePoint 用に PST が構成されていると想定できます。含まれていない場合、pst は SharePoint pst として構成されていません。 
  
**GetProps**を使用してプロパティにアクセスする方法の詳細については、「 [MAPI プロパティの取得](retrieving-mapi-properties.md)」を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFunctions  <br/> |GetPropsNULL  <br/> |mfcmapi は、 **imapiprop:: GetProps**メソッドを使用して、オブジェクトのすべてのプロパティを取得します。 NULL または、 _lpPropTagArray_パラメーターの[imapiprop:: getproplist](imapiprop-getproplist.md)メソッドによって返される配列を渡します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)
  
[SPropValue](spropvalue.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI プロパティの取得](retrieving-mapi-properties.md)
  
[エラー処理にマクロを使用する](using-macros-for-error-handling.md)

