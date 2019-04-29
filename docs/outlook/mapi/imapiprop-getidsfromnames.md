---
title: imapipropgetidsfromnames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetIDsFromNames
api_type:
- COM
ms.assetid: e3f501a4-a8ee-43d7-bd83-c94e7980c398
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 28880b818bc80e31cae0c695d4aac92eb9555cac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433585"
---
# <a name="imapipropgetidsfromnames"></a>IMAPIProp::GetIDsFromNames

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1つまたは複数のプロパティ名に対応するプロパティ識別子を提供します。
  
```cpp
HRESULT GetIDsFromNames(
  ULONG cPropNames,
  LPMAPINAMEID FAR * lppPropNames,
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTags
);
```

## <a name="parameters"></a>パラメーター

 _cpropnames_
  
> 順番_lpppropnames_パラメーターによって示されるプロパティ名の数。 _lpppropnames_が NULL の場合、 _cpropnames_パラメーターは0である必要があります。 
    
 _lpppropnames_
  
> 順番プロパティ名の配列へのポインター、または NULL。 オブジェクトが情報を持っているすべてのプロパティセット内のすべてのプロパティ名に対して NULL 要求のプロパティ識別子を渡す。 MAPI_CREATE フラグが_ulflags_パラメーターで設定されている場合、 _lpppropnames_パラメーターを NULL にすることはできません。 
    
 _ulFlags_
  
> 順番プロパティ識別子を返す方法を示すフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_CREATE 
  
> プロパティ識別子がまだ割り当てられていない場合は、その識別子を、 _lpppropnames_で指定されたプロパティ名の配列に含まれる1つ以上の名前に割り当てます。 このフラグは、名前から識別子へのマッピングテーブルに、識別子を内部的に登録します。
    
 _lppproptags_
  
> 読み上げ既存または新規に割り当てられたプロパティ識別子を含むプロパティタグの配列へのポインターへのポインター。 この配列の property タグのプロパティの種類は、 **PT_UNSPECIFIED**に設定されています。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 指定したプロパティ名の識別子が正常に返されました。
    
MAPI_E_NO_SUPPORT 
  
> オブジェクトは、名前付きプロパティをサポートしていません。
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> メモリが不足しているため、識別子を取得できませんでした。
    
MAPI_E_TOO_BIG 
  
> 返されるプロパティタグが多すぎるため、操作を実行できません。
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しは全体的に成功しましたが、1つ以上のプロパティ識別子を返すことができませんでした。 使用できない各プロパティの対応するプロパティの種類が**PT_ERROR**に設定され、その識別子が0に設定されます。 この警告が返された場合は、呼び出しを成功として処理します。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。
    
## <a name="remarks"></a>注釈

**imapiprop:: getidsfromnames**メソッドは、1つ以上の名前付きプロパティのプロパティ識別子を保持するプロパティタグの配列を取得します。 **imapiprop:: getidsfromnames**を呼び出して、次の操作を行うことができます。 
  
- 新しい名前の識別子を作成します。
    
- 特定の名前の識別子を取得します。
    
- オブジェクトのマッピングに含まれているすべての名前付きプロパティの識別子を取得します。
    
名前付きプロパティは、通常、フォルダーおよびメッセージのメッセージストアプロバイダーによって使用されます。 メッセージングユーザーやプロファイルセクションなど、他のオブジェクトは、名前とプロパティ識別子との関連付けをサポートしていない場合があり、 **getidsfromnames**から MAPI_E_NO_SUPPORT を返す場合があります。
  
特定の名前の識別子を返すエラーがある場合、 **getidsfromnames**は MAPI_W_ERRORS_RETURNED を返し、プロパティタグ配列エントリのプロパティの型を**PT_ERROR**に対応するプロパティタグ配列エントリに設定し、識別子を0に設定します。 
  
名前から識別子へのマッピングは、オブジェクトの**PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) プロパティによって表されます。 **PR_MAPPING_SIGNATURE**には、オブジェクトを処理するサービスプロバイダーを示す[MAPIUID](mapiuid.md)構造が含まれています。 2つのオブジェクトの**PR_MAPPING_SIGNATURE**プロパティが同じ場合は、これらのオブジェクトが同じ名前と識別子のマッピングを使用することを前提としています。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

_lpppropnames_パラメーターによって指定されたプロパティタグ配列で返される識別子は、0x8000 ~ 0xFFFE の範囲内にある必要があります。 この配列のエントリは、 _lpppropnames_で指定されたプロパティ名配列で渡された名前と同じ順序にする必要があります。 
  
コンテナーで名前付きプロパティをサポートする場合は、コンテナー内のすべてのオブジェクトに同じ名前と識別子のマッピングを使用します (つまり、メッセージストア内の各フォルダーまたはフォルダー内の各メッセージに対して異なるマッピングを使用しません)。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_lppproptags_によって参照されるプロパティタグの配列で返される識別子のプロパティの種類は**PT_UNSPECIFIED**に設定されているため、 [imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出して正確な型を取得する必要があります。 
  
名前付きプロパティを持つオブジェクトを移動またはコピーするときに、source オブジェクトと destination オブジェクトのマッピングシグネチャがそれぞれの**PR_MAPPING_SIGNATURE**プロパティの値で示されている場合は、これらの操作の間に名前を保持する必要があります。 プロパティ名を保持するには、対応するプロパティ識別子を、対象のオブジェクトの名前から識別子へのマッピングと一致するように調整します。 
  
一部のオブジェクトには、名前を付けることができるプロパティ識別子の数に制限があります。 **getidsfromnames**を呼び出すとこの制限を超えると、メソッドは MAPI_E_TOO_BIG を返します。 この場合は、識別子でクエリを実行します。 
  
詳細については、「 [MAPI の名前付きプロパティ](mapi-named-properties.md)」を参照してください。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl  <br/> |CSingleMAPIPropListCtrl:: findallnamedpropsused  <br/> |mfcmapi は、 **imapiprop:: getidsfromnames**メソッドを使用して、マップされているすべての名前付きプロパティのプロパティタグを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[MAPINAMEID](mapinameid.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI ���O�t���v���p�e�B](mapi-named-properties.md)
  
[エラー処理にマクロを使用する](using-macros-for-error-handling.md)

