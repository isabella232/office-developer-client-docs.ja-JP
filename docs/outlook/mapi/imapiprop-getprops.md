---
title: IMAPIPropGetProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp.GetProps
api_type:
- COM
ms.assetid: 1c7a9cd2-d765-4218-9aee-52df1a2aae6c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 26ab8d67687038118c2dfbbf8d6fc6baddbdcccf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625536"
---
# <a name="imapipropgetprops"></a>IMAPIProp::GetProps

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトの 1 つ以上のプロパティのプロパティ値を取得します。
  
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
  
> [in]値を取得するプロパティを識別するプロパティ タグの配列へのポインター。 _lpPropTagArray_ パラメーターは NULL で、オブジェクトのすべてのプロパティの値を返す必要があります、または 1 つ以上のプロパティ タグを含む [SPropTagArray](sproptagarray.md)構造体を指す必要があります。 
    
 _ulFlags_
  
> [in]型を持つプロパティの形式を示すフラグのビットマスクPT_UNSPECIFIED。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> これらのプロパティの文字列値は、Unicode 形式で返す必要があります。 このフラグMAPI_UNICODE設定しない場合は、ANSI 形式で文字列値を返す必要があります。
    
 _lpcValues_
  
> [out]  _lppPropArray_ パラメーターが指すプロパティ値の数を指すポインター。 _lppPropArray が_ NULL の場合 _、lpcValues_ パラメーターの内容は 0 です。 
    
 _lppPropArray_
  
> [out]取得したプロパティ値へのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロパティの値が正常に取得されました。
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しは全体的に成功しましたが、1 つ以上のプロパティにアクセスする必要がありました。 使用できない各プロパティのプロパティ値の **aulPropTag** メンバーには、プロパティの種類PT_ERROR識別子が 0 です。 この警告が返されると、呼び出しは正常に処理されます。 この警告をテストするには、次のマクロ **HR_FAILED** します。 詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。
    
MAPI_E_INVALID_PARAMETER 
  
> _lpPropTagArray_ が指す **SPropTagArray** 構造体の **cValues** メンバーにゼロが渡されています。
    
## <a name="remarks"></a>注釈

**IMAPIProp::GetProps** メソッドは、オブジェクトの 1 つ以上のプロパティのプロパティ値を取得します。 
  
プロパティの値は、要求された順序と同じ順序で返されます (つまり  _、lpPropTagArray_ が指すプロパティ タグ配列内のプロパティの順序は  _、lppPropArray_ が指すプロパティ値構造体の配列の順序と一致します)。 
  
プロパティ タグ配列の **aulPropTag** メンバーで指定されたプロパティ型は、各プロパティ値構造体の **Value** メンバーで返される値の種類を示します。 ただし、呼び出し元がプロパティの種類を知らない場合は **、aulPropTag** メンバーの型を代わりにプロパティにPT_UNSPECIFIED。 値を取得する際に **、GetProps は** プロパティのプロパティ値構造体 **の aulPropTag** メンバーに正しい型を設定します。 
  
_lpPropTagArray の SPropTagArray_ でプロパティ型が指定されている場合 _、lppPropArray_ で返される **SPropValue** のプロパティ値には、エラー値が代わりに返されていない限り、要求された型と完全に一致する型があります。  
  
文字列プロパティには、Unicode 形式を表すプロパティPT_UNICODE ANSI 形式を表PT_STRING8プロパティの 2 つのいずれかを指定できます。 _ulFlags_ パラメーターで MAPI_UNICODE フラグが設定されている場合 **、GetProps** が文字列プロパティの適切な形式を決定できない場合は常に、Unicode 形式で値を返します。 **GetProps は** 、次の状況で正確な文字列プロパティの種類を特定できません。 
  
- _lpPropTagArray パラメーターは_ NULL に設定して、すべてのプロパティを要求します。 
    
- **aulPropTag** メンバーには、プロパティ タグPT_UNSPECIFIEDプロパティの種類として指定された値が含まれます。 
    
_lpPropTagArray_ パラメーターが NULL に設定され、オブジェクトのすべてのプロパティを取得し、プロパティが存在しない場合 **、GetProps は** 次の処理を実行します。 
  
- 値をS_OKします。
    
- プロパティ値構造体の **cValues** メンバーの count 値を 0 に設定します。 
    
- _lpcValues の内容を_ 0 に設定します。 
    
- _lppPropArray を_ NULL に設定します。 
    
 **GetProps は****、cValues** を 0 に設定した複数値のプロパティを返す必要があります。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

[MAPIAllocateBuffer](mapiallocatebuffer.md)関数を呼び出して _、lpPropTagArray_ が指す [SPropValue](spropvalue.md)構造体のメモリを最初に割り当てる。[MAPIAllocateMore を呼](mapiallocatemore.md)び出して、構造体のメンバーに必要な追加のメモリを割り当てる。 
  
要求MAPI_W_ERRORS_RETURNEDプロパティの値を取得できない場合は、この値を返します。 プロパティ値構造で **、aulPropTag** メンバーの型を PT_ERROR に設定し **、Value** メンバーにエラーを説明する状態コードを設定します。 たとえば、文字列を Unicode に変換する必要がある場合、Unicode をサポートしていない場合は **、Value** メンバーを次の文字列にMAPI_E_BAD_CHARWIDTH。 プロパティが大きすぎる場合は、プロパティを [プロパティ] MAPI_E_NOT_ENOUGH_MEMORY。 オブジェクトがプロパティをサポートしていない場合は、このプロパティを [プロパティ] MAPI_E_NOT_FOUND。 
  
リモート トランスポート プロバイダーによる **GetProps** メソッドの実装では、呼び出し元が要求したプロパティのフォルダーのプロパティ値を返す必要があります。 実装では、次の操作を行う必要があります。 
  
- 呼び出し元に返すプロパティ値配列を割り当て、その目的で渡されたプロパティ値ポインター パラメーターにアドレスを格納します。
    
- GetProps に渡されるプロパティ タグの配列に従って、フォルダーのプロパティからプロパティ値配列のプロパティ タグにプロパティ タグ **をコピーします**。
    
- GetProps に渡されるすべてのプロパティ タグに対してプロパティの種類が **設定されている必要があります**。 呼び出し元は、プロパティの種類のプロパティ PT_UNSPECIFIED渡すことができます。その場合 **、GetProps** は、そのプロパティ タグの正しいプロパティの種類を設定する必要があります。 
    
- タグに従ってプロパティ値配列の各プロパティの値を設定します。 たとえば、呼び出し元から要求されたプロパティ タグが PR_OBJECT_TYPE **(** [PidTagObjectType)](pidtagobjecttype-canonical-property.md)の場合 **、GetProps** は値を MAPI_FOLDER に設定できます。 
    
- 呼び出し元が実装で処理しないプロパティ タグを渡す場合は、それらのプロパティのプロパティ タグを PT_ERROR に設定し、プロパティ値を MAPI_E_NOT_FOUND に設定できます。
    
- エラー S_OKが発生した場合、またはエラーが発生MAPI_W_ERRORS_RETURNED場合は、エラーを返します。
    
リモート トランスポート プロバイダーによる **GetProps** メソッドの実装では、少なくとも次のプロパティをサポートする必要があります。 
  
- **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))
    
- **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))
    
- **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))
    
- **PR_OBJECT_TYPE**
    
- **PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))
    
## <a name="notes-to-callers"></a>呼び出し側への注意

型プロパティのプロパティPT_OBJECT、GetProps の代わりに [IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッド **を呼び出します**。 
  
セキュリティで保護されたプロパティの場合は _、lppPropTagArray_ パラメーターを NULL に設定して **GetProps** を呼び出して取得する必要はありません。 GetProps を呼び出す場合は、プロパティ タグ配列 **の aulPropTag** メンバーでセキュリティで保護されたプロパティの識別子を明示的に **設定する必要があります**。 セキュリティで保護されたプロパティを使用できる場合と方法は、サービス プロバイダーによって管理されます。 
  
**GetProps** が関数または関数を返す場合にのみ [、MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、返される **SPropValue** 構造体S_OK解放MAPI_W_ERRORS_RETURNED。 
  
**GetProps** が 1 つMAPI_W_ERRORS_RETURNEDプロパティにアクセスできないため、プロパティを返す場合は、返されるプロパティのプロパティ タグを確認します。 失敗したプロパティには、プロパティ値構造に次の値が設定されます。 
  
- **aulPropTag メンバーのプロパティ** の種類は、プロパティに設定PT_ERROR。 
    
- Value メンバーのプロパティ **の値** は、エラーの状態コード (エラーなど) に設定MAPI_E_NOT_FOUND。 
    
プロパティ値構造体で返すには大きすぎるため失敗するプロパティには **、Value** メンバーが値に設定MAPI_E_NOT_ENOUGH_MEMORY。 通常、これは、プロパティの値が 4 KB 以上の場合に、PT_STRING8、PT_UNICODE、または PT_BINARY 型の文字列プロパティまたはバイナリ プロパティで発生します。 **IMAPIProp::OpenProperty を呼び出して、大** きなプロパティを取得します。 
  
**GetProps のすべての実装で、文字列** の Unicode 形式と ANSI 形式の両方がサポートされているという場合があります。 特定のプロパティで文字列形式の変換が必要で **、GetProps** でサポートできない場合は、プロパティの **Value** メンバーが文字列形式にMAPI_E_BAD_CHARWIDTH。 
  
PST が SharePoint PST である場合は [、IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)を使用して PST をマウントし、このプロパティを要求するメッセージ ストア オブジェクトで **GetProps** を呼び出します。 存在する場合は、PST がユーザーに対して構成SharePoint。指定されていない場合、PST は PST の構成SharePointされていません。 
  
**GetProps** を使用してプロパティにアクセスする方法の詳細については、「MAPI プロパティの取得 [」を参照してください](retrieving-mapi-properties.md)。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI は **、IMAPIProp::GetProps** メソッドを使用して _、LPPropTagArray_ パラメーターで [IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドによって返される NULL または配列を渡して、オブジェクトのすべてのプロパティを取得します。  <br/> |
   
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

