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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 33351235db2a9a3f9d9b67f59e8356a0fa8abfa8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800656"
---
# <a name="imapipropgetprops"></a>IMAPIProp::GetProps

  
  
**適用対象**: Outlook 
  
オブジェクトの 1 つまたは複数のプロパティのプロパティ値を取得します。
  
```cpp
HRESULT GetProps(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppPropArray
);
```

## <a name="parameters"></a>�p�����[�^�[

 _lpPropTagArray_
  
> [in]取得するのには、値がプロパティを識別するプロパティ タグの配列へのポインター。 _LpPropTagArray_パラメーターは、NULL であるか、オブジェクトのすべてのプロパティの値、返されることを示す 1 つまたは複数のプロパティ タグを含む[SPropTagArray](sproptagarray.md)構造体をポイントにする必要があります。 
    
 _ulFlags_
  
> [in]PT_UNSPECIFIED の種類のプロパティの形式を示すフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> Unicode 形式でこれらのプロパティの文字列値が返されます。 MAPI_UNICODE フラグが設定されていない場合、ANSI 形式の文字列値が返されます。
    
 _lpcValues_
  
> [out]_LppPropArray_パラメーターで指定されたプロパティの値の数へのポインター。 _LppPropArray_が NULL の場合は、 _lpcValues_パラメーターの内容は 0 になります。 
    
 _lppPropArray_
  
> [out]取得したプロパティの値へのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> プロパティの値が正常に取得されました。
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しは完了しましたが、1 つまたは複数のプロパティにアクセスできませんでした。 各使用できないプロパティのプロパティ値の**aulPropTag**メンバーには、PT_ERROR とゼロの識別子のプロパティ型があります。 この警告が返されると、呼び出しを成功として処理する必要があります。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。
    
MAPI_E_INVALID_PARAMETER 
  
> **あう**、 **SPropTagArray**構造体のメンバー _lpPropTagArray_で示される 0 が渡されました。
    
## <a name="remarks"></a>注釈

**IMAPIProp::GetProps**メソッドは、オブジェクトの 1 つまたは複数のプロパティのプロパティ値を取得します。 
  
プロパティの値が同じ順序で返されます、要求された (つまり、プロパティ タグ配列内のプロパティの順序で示される_lpPropTagArray_と一致する_の lppPropArray で指定されたプロパティ値の構造体の配列内の順序_). 
  
プロパティ タグ配列の**aulPropTag**のメンバーで指定されたプロパティの型は、各プロパティ値の構造体のメンバー**の値**で返される値の型を指定します。 ただし、呼び出し元がプロパティの型を把握していない場合、 **aulPropTag**メンバーの種類設定できます代わりに PT_UNSPECIFIED を。 値を取得するには、 **GetProps**は、 **aulPropTag**のメンバー、プロパティ、構造体のプロパティ値の正しい型を設定します。 
  
エラー値が返される場合を除きに、 _lppPropArray_で返される**SPropValue**のプロパティ値が、要求された型と一致する型を持つ_lpPropTagArray_の**SPropTagArray**では、プロパティの型が指定されている場合その代わりに。 
  
文字列プロパティは、2 つのプロパティ タイプのいずれかを持つことができます: PT_UNICODE PT_STRING8 ANSI 形式を表す Unicode 形式を表す。 **GetProps**が文字列型のプロパティの適切な形式を判断できないときに、 _ulFlags_のパラメーターに MAPI_UNICODE フラグが設定されて、する場合は、Unicode 形式でその値を返します。 **GetProps**には、以下の状況で、正確な文字列プロパティの型を判断できません。 
  
- _LpPropTagArray_パラメーターは、すべてのプロパティを要求するのには NULL に設定されています。 
    
- **AulPropTag**メンバーには、プロパティ タグ配列にそのプロパティの型としての PT_UNSPECIFIED の値が含まれています。 
    
_LpPropTagArray_パラメーターが NULL に設定してすべてのオブジェクトのプロパティを取得、プロパティが存在しない場合は、 **GetProps**は次を行います。 
  
- S_OK を返します。
    
- 引数 count の値を**あう**プロパティ値構造体のメンバーを 0 に設定します。 
    
- _LpcValues_の内容を 0 に設定します。 
    
- _LppPropArray_を NULL に設定します。 
    
 **GetProps**に**あう**と複数値プロパティが 0 に設定を返す必要がありますされません。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

[SPropValue](spropvalue.md)構造体_lpPropTagArray_; での最初にメモリを割り当てることの[MAPIAllocateBuffer](mapiallocatebuffer.md)関数を呼び出す構造体のメンバーに必要な追加のメモリを割り当てるには、 [MAPIAllocateMore](mapiallocatemore.md)を呼び出します。 
  
要求されたプロパティの 1 つ以上の値を取得できない場合は、MAPI_W_ERRORS_RETURNED を返します。 プロパティの値の構造に PT_ERROR に**aulPropTag**のメンバーと、エラーを説明するステータス コード**値**のメンバーの種類を設定します。 などの文字列を Unicode に変換する必要がある、Unicode をサポートしていない場合、**値**メンバーを MAPI_E_BAD_CHARWIDTH に設定します。 プロパティが大きすぎる場合は、MAPI_E_NOT_ENOUGH_MEMORY に設定します。 オブジェクトがプロパティをサポートしていない場合は、MAPI_E_NOT_FOUND を設定します。 
  
**GetProps**メソッドのリモート トランスポート プロバイダーの実装は、プロパティの呼び出し元によって要求されたフォルダーのプロパティの値を返す必要があります。 実装では、次の操作を行う必要があります。 
  
- 呼び出し元に戻るし、その目的のために渡されたプロパティ値のポインター パラメーターにそのアドレスを格納するプロパティ値の配列を割り当てます。
    
- **GetProps**に渡されるプロパティ タグの配列に基づいて、プロパティ値の配列内のプロパティ タグに、フォルダーのプロパティからプロパティ タグをコピーします。
    
- **GetProps**に渡されるすべてのプロパティ タグのプロパティのデータ型が設定されていることを確認します。 ケース**GetProps**がそのプロパティ タグの適切なプロパティの型を設定する必要があります、PT_UNSPECIFIED のプロパティの型で呼び出し側が渡すことができます。 
    
- に従って、タグ、プロパティ値の配列内の各プロパティの値を設定します。 など、この呼び出し元によって要求されたプロパティ タグが**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) の場合は、 **GetProps**は MAPI_FOLDER に値を設定できます。 
    
- 実装が処理しない任意のプロパティ タグの呼び出しが成功した場合は、PT_ERROR にこれらのプロパティのプロパティ タグを設定し、MAPI_E_NOT_FOUND をプロパティの値を設定します。
    
- エラーが発生した場合は、エラーが発生していない場合は S_OK、または MAPI_W_ERRORS_RETURNED を返します。
    
**GetProps**メソッドのリモート トランスポート プロバイダーの実装では、最低限次のプロパティをサポートする必要があります。 
  
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

PT_OBJECT の種類のプロパティの場合に、 **GetProps**の代わりに[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出します。 
  
セキュリティで保護されたプロパティは、必要ありません**GetProps**を呼び出すと、 _lppPropTagArray_パラメーターを NULL に設定してしまいます。 必要があります明示的に設定するセキュリティで保護されたプロパティの識別子のプロパティ タグ配列の**aulPropTag**メンバーに**GetProps**を呼び出すとします。 サービス プロバイダーは、セキュリティで保護されたプロパティは利用可能な時期と方法です。 
  
**GetProps** MAPI_W_ERRORS_RETURNED は s_ok を返す場合にのみ、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって返された**SPropValue**構造体を解放します。 
  
**GetProps**では、1 つまたは複数のプロパティにアクセスできなかったために MAPI_W_ERRORS_RETURNED が返された場合は、返されるプロパティのプロパティ タグを確認してください。 失敗したプロパティには、次の値がそのプロパティ値の構造体に設定があります。 
  
- PT_ERROR に**aulPropTag**メンバーのプロパティの型。 
    
- MAPI_E_NOT_FOUND など、エラーの状態コードを入力する設定**値**のメンバーのプロパティの値。 
    
プロパティはプロパティの値の構造体で簡単に取得するには大きすぎるために失敗した MAPI_E_NOT_ENOUGH_MEMORY に設定されて、**値**のメンバーがあります。 通常、この場合に型の文字列またはバイナリのプロパティを持つ PT_STRING8、PT_UNICODE、または PT_BINARY プロパティの値は 4 KB 以上です。 大きなプロパティを取得するために**IMAPIProp::OpenProperty**を呼び出します。 
  
**GetProps**のすべての実装では、文字列を Unicode と ANSI の両方の形式をサポートします。 特定のプロパティには、文字列形式の変換が必要です、 **GetProps**がサポートできないと、プロパティの**値**のメンバーが MAPI_E_BAD_CHARWIDTH に設定されています。 
  
PST をマウントする pst ファイルが SharePoint pst ファイルを確認して、このプロパティを要求するメッセージ ストアのオブジェクトの**GetProps**を呼び出し、 [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)を使用して。 、存在する場合は、SharePoint の pst ファイルが構成されていると見なすことがそれ以外の場合は、SharePoint の PST と pst ファイルが構成されていません。 
  
**GetProps**を使用してプロパティにアクセスする方法の詳細については、 [MAPI プロパティを取得する](retrieving-mapi-properties.md)を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI では、 **IMAPIProp::GetProps**メソッドを使用して、NULL または_lpPropTagArray_パラメーターでは、 [IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドによって返される配列を渡すことによって、オブジェクトのすべてのプロパティを取得します。  <br/> |
   
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
  
[MAPI プロパティを取得します。](retrieving-mapi-properties.md)
  
[エラー処理のためのマクロの使用](using-macros-for-error-handling.md)

