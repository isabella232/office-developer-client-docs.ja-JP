---
title: IMAPIPropGetIDsFromNames
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5247ca71c88b9c0f8591a732746a17204265741c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800660"
---
# <a name="imapipropgetidsfromnames"></a>IMAPIProp::GetIDsFromNames

  
  
**適用されます**: Outlook 
  
1 つまたは複数のプロパティ名に対応するプロパティの識別子を提供します。
  
```cpp
HRESULT GetIDsFromNames(
  ULONG cPropNames,
  LPMAPINAMEID FAR * lppPropNames,
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTags
);
```

## <a name="parameters"></a>Parameters

 _cPropNames_
  
> [in]_LppPropNames_パラメーターで指定されたプロパティ名の数。 _LppPropNames_が NULL の場合は、 _cPropNames_パラメーターは 0 である必要があります。 
    
 _lppPropNames_
  
> [in]プロパティ名、または NULL の配列へのポインター。 パラメーターに NULL は、オブジェクトに情報があるについては、すべてのプロパティ セットのすべてのプロパティ名のプロパティの識別子を要求します。 _LppPropNames_パラメーターには NULL 必要がありますできません_ulFlags_パラメーターで、タグのフラグが設定されている場合。 
    
 _ulFlags_
  
> [in]プロパティ識別子が返される方法を示すフラグのビットマスクです。 次のフラグを設定することができます。
    
タグ 
  
> プロパティの識別子では、1 つがまだ割り当てられていない場合、 _lppPropNames_で指定されたプロパティ名の配列に含まれている名前の 1 つ以上が割り当てられます。 このフラグは、名前の識別子をマッピング テーブルで内部的に id を登録します。
    
 _lppPropTags_
  
> [out]既存または新たに割り当てられたプロパティの識別子を含むプロパティ タグの配列へのポインターへのポインター。 この配列内のプロパティ タグのプロパティの型は、 **PT_UNSPECIFIED**に設定されます。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 指定したプロパティ名の識別子が正常に返されました。
    
MAPI_E_NO_SUPPORT 
  
> オブジェクトは、名前付きプロパティをサポートしていません。
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> メモリ不足のためでは、識別子を取得できませんでした。
    
MAPI_E_TOO_BIG 
  
> 返される多くのプロパティ タグが必要なために、操作を実行できません。
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しは完了しましたが、1 つまたは複数のプロパティの識別子は返されませんでした。 使用できないプロパティごとに対応するプロパティの型は、 **PT_ERROR**とその id を 0 に設定されています。 この警告が返されると、その成功と呼び出しを処理します。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 [エラー処理のためのマクロを使用する](using-macros-for-error-handling.md)を参照してください。
    
## <a name="remarks"></a>備考

**IMAPIProp::GetIDsFromNames**メソッドは、1 つまたは複数の名前付きプロパティのプロパティの識別子を保持するプロパティ タグの配列を取得します。 **IMAPIProp::GetIDsFromNames**は、次の操作を呼び出すことができます。 
  
- 新しい名前の識別子を作成します。
    
- 特定の名前の識別子を取得します。
    
- オブジェクトのマッピングに含まれるすべての名前付きプロパティの識別子を取得します。
    
名前付きプロパティは、通常、フォルダーやメッセージのメッセージ ストア プロバイダーが使用します。 メッセージングのユーザーとプロファイルのセクションなど、他のオブジェクトは、プロパティの識別子を名前との関連付けをサポートしていない可能性があり、 **GetIDsFromNames**から MAPI_E_NO_SUPPORT を返すことがあります。
  
エラーを特定の名前の識別子を返す場合は、 **GetIDsFromNames** MAPI_W_ERRORS_RETURNED を返し**PT_ERROR**と id を 0 にする名前に対応するプロパティ タグ配列のエントリのプロパティの型を設定します。 
  
識別子に名前のマッピングは、オブジェクトの**PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) で表されます。 **PR_MAPPING_SIGNATURE**には、オブジェクトを担当するサービス プロバイダーを指定する[MAPIUID](mapiuid.md)構造体が含まれています。 **PR_MAPPING_SIGNATURE**プロパティ、2 つのオブジェクトに対して同じである場合は、これらのオブジェクトが同じ名前の識別子をマッピングを使用することを想定しています。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

_LppPropNames_パラメーターで指定されたプロパティ タグ配列に渡された識別子は、0x8000 を 0 xfffe の範囲でなければなりません。 この配列のエントリ必要があるプロパティ名の配列に渡された名前と同じ順序で指す_lppPropNames_です。 
  
コンテナーの名前付きプロパティをサポートする場合は、同じ名前の識別子にマッピングを使用して、コンテナー内のすべてのオブジェクト (つまり、マッピングを使用しない、別のメッセージ ストア内の各フォルダーまたはフォルダー内の各メッセージの)。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_LppPropTags_で指定されたプロパティ タグ配列で返される識別子のプロパティの型は、 **PT_UNSPECIFIED**に設定されているためには、正確な型を取得するために[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出す必要があります。 
  
移動する、または名前付きプロパティを持つオブジェクトのコピーと、ソースと変換先オブジェクトの**PR_MAPPING_SIGNATURE**プロパティの値で示される別のマッピングのシグネチャを持つ、これらの操作中に名前を保持する必要があります。 プロパティ名を保持するには、目的のオブジェクトの識別子に名前のマッピングに一致するように対応するプロパティの識別子を調整します。 
  
いくつかのオブジェクトには、プロパティ識別子の名前を数の制限があります。 **GetIDsFromNames**への呼び出しでは、この制限を越えるが発生する場合は、MAPI_E_TOO_BIG を返します。 この例では、識別子によってクエリを実行します。 
  
詳細については、 [MAPI 名前付きプロパティ](mapi-named-properties.md)を参照してください。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::FindAllNamedPropsUsed  <br/> |MFCMAPI では、 **IMAPIProp::GetIDsFromNames**メソッドを使用して、マップされたすべての名前付きプロパティのプロパティ タグを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[MAPINAMEID](mapinameid.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPIProp: IUnknown](imapipropiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI ���O�t���v���p�e�B](mapi-named-properties.md)
  
[エラー処理のためのマクロを使用してください。](using-macros-for-error-handling.md)

