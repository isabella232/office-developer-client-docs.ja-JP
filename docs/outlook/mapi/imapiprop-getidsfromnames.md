---
title: IMAPIPropGetIDsFromNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp.GetIDsFromNames
api_type:
- COM
ms.assetid: e3f501a4-a8ee-43d7-bd83-c94e7980c398
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4f79e82c1ecbca9f006d60a2eb724fc5900a5d68
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564142"
---
# <a name="imapipropgetidsfromnames"></a>IMAPIProp::GetIDsFromNames

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1 つ以上のプロパティ名に対応するプロパティ識別子を提供します。
  
```cpp
HRESULT GetIDsFromNames(
  ULONG cPropNames,
  LPMAPINAMEID FAR * lppPropNames,
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTags
);
```

## <a name="parameters"></a>パラメーター

 _cPropNames_
  
> [in]  _lppPropNames_ パラメーターが指すプロパティ名の数。 _lppPropNames が_ NULL の場合 _、cPropNames_ パラメーターは 0 である必要があります。 
    
 _lppPropNames_
  
> [in]プロパティ名または NULL の配列へのポインター。 NULL を渡す場合は、オブジェクトが情報を持つすべてのプロパティ セットのすべてのプロパティ名のプロパティ識別子を要求します。 _ulFlags_ パラメーターにフラグを設定する場合 _、lppPropNames_ パラメーター MAPI_CREATE NULL にすることはできません。 
    
 _ulFlags_
  
> [in]プロパティ識別子を返す方法を示すフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_CREATE 
  
> プロパティ識別子がまだ割り当てられていない場合は  _、lppPropNames_ によって指されるプロパティ名配列に含まれる 1 つ以上の名前に割り当てられます。 このフラグは、名前から識別子へのマッピング テーブルに識別子を内部的に登録します。
    
 _lppPropTags_
  
> [out]既存のプロパティ識別子または新しく割り当てられたプロパティ識別子を含むプロパティ タグの配列へのポインター。 この配列のプロパティ タグのプロパティの種類は、次の値 **にPT_UNSPECIFIED。**
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 指定したプロパティ名の識別子が正常に返されました。
    
MAPI_E_NO_SUPPORT 
  
> オブジェクトは名前付きプロパティをサポートしていない。
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> 識別子を取得するために使用できるメモリが不足しています。
    
MAPI_E_TOO_BIG 
  
> 返されるプロパティ タグが多すぎるため、操作を実行できません。
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しは全体的に成功しましたが、1 つ以上のプロパティ識別子を返す必要がありました。 使用できない各プロパティの対応するプロパティの種類は、PT_ERROR **に設定** され、その識別子は 0 に設定されます。 この警告が返された場合は、呼び出しを成功として処理します。 この警告をテストするには、次のマクロ **HR_FAILED** します。 「エラー [処理のためのマクロの使用」を参照してください](using-macros-for-error-handling.md)。
    
## <a name="remarks"></a>注釈

**IMAPIProp::GetIDsFromNames** メソッドは、1 つ以上の名前付きプロパティのプロパティ識別子を保持するプロパティ タグの配列を取得します。 **IMAPIProp::GetIDsFromNames** を呼び出して、次の操作を実行できます。 
  
- 新しい名前の識別子を作成します。
    
- 特定の名前の識別子を取得します。
    
- オブジェクトのマッピングに含まれるすべての名前付きプロパティの識別子を取得します。
    
名前付きプロパティは、通常、フォルダーとメッセージのメッセージ ストア プロバイダーによって使用されます。 メッセージング ユーザーやプロファイル セクションなどの他のオブジェクトは、名前とプロパティ識別子の関連付けをサポートしていない可能性があります **。GetIDsFromNames** から MAPI_E_NO_SUPPORTを返す場合があります。
  
特定の名前の識別子を返すエラーがある場合 **、GetIDsFromNames** は MAPI_W_ERRORS_RETURNED を返し、名前に対応するプロパティ タグ配列エントリのプロパティの種類を PT_ERROR に設定し、識別子を **0** に設定します。 
  
名前から識別子へのマッピングは、オブジェクトのプロパティ ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md) **)** PR_MAPPING_SIGNATUREプロパティで表されます。 **PR_MAPPING_SIGNATURE** には、オブジェクトを担当するサービス プロバイダーを示す [MAPIUID](mapiuid.md) 構造が含まれている必要があります。 2 つの **PR_MAPPING_SIGNATURE** プロパティが同じ場合は、これらのオブジェクトが同じ名前から識別子へのマッピングを使用すると仮定します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

_lppPropNames_ パラメーターが指すプロパティ タグ配列に戻す識別子は、0x8000から0xFFFEである必要があります。 この配列のエントリは  _、lppPropNames_ が指すプロパティ名配列で渡される名前と同じ順序である必要があります。 
  
コンテナーで名前付きプロパティをサポートする場合は、コンテナー内のすべてのオブジェクトに対して同じ名前から識別子へのマッピングを使用します (つまり、メッセージ ストア内のフォルダーまたはフォルダー内の各メッセージに対して異なるマッピングを使用しない)。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_lppPropTags_ が指すプロパティ タグ配列内の返される識別子のプロパティ型は **PT_UNSPECIFIED** に設定されますので、正確な型を取得するには [、IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出す必要があります。 
  
名前付きプロパティを持つオブジェクトを移動またはコピーし、ソース オブジェクトと移動先オブジェクトのマッピングシグネチャが **異なる場合は、PR_MAPPING_SIGNATURE** プロパティの値で示されるマッピング署名が異なる場合は、これらの操作中に名前を保持する必要があります。 プロパティ名を保持するには、対応するプロパティ識別子を、コピー先オブジェクトの名前と識別子のマッピングと一致する値に調整します。 
  
一部のオブジェクトには、名前を付けできるプロパティ識別子の数に制限があります。 **GetIDsFromNames** の呼び出しによってこの制限を超えた場合、メソッドは値を返MAPI_E_TOO_BIG。 この場合、識別子によるクエリを実行します。 
  
詳細については、「MAPI 名前付き [プロパティ」を参照してください](mapi-named-properties.md)。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::FindAllNamedPropsUsed  <br/> |MFCMAPI は **IMAPIProp::GetIDsFromNames** メソッドを使用して、マップされた名前付きプロパティのプロパティ タグを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[MAPINAMEID](mapinameid.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI ���O�t���v���p�e�B](mapi-named-properties.md)
  
[エラー処理にマクロを使用する](using-macros-for-error-handling.md)

