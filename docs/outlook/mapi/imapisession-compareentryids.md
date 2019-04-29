---
title: imapisessioncompareentryids
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.CompareEntryIDs
api_type:
- COM
ms.assetid: 319f10e9-db8d-4d16-aa1f-6cf5fef493eb
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4dfde82aa843072168288f4e0b0084dfccd5cd2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427816"
---
# <a name="imapisessioncompareentryids"></a>IMAPISession::CompareEntryIDs

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
2つのエントリ識別子を比較して、同じオブジェクトを参照しているかどうかを判断します。 
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
);
```

## <a name="parameters"></a>パラメーター

 _cbEntryID1_
  
> 順番_lpEntryID1_パラメーターによって指定されたエントリ識別子のバイト数。 
    
 _lpEntryID1_
  
> 順番比較する最初のエントリ識別子へのポインター。
    
 _cbEntryID2_
  
> 順番_lpEntryID2_パラメーターによって指定されたエントリ識別子のバイト数。 
    
 _lpEntryID2_
  
> 順番比較する2番目のエントリ id へのポインター。
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lルー result_
  
> 読み上げ比較結果へのポインター。 2つのエントリ識別子が同じオブジェクトを参照している場合は TRUE。それ以外の場合は FALSE。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 比較に成功しました。
    
MAPI_E_UNKNOWN_ENTRYID 
  
> パラメーターとして指定されたいずれかまたは両方のエントリ識別子がオブジェクトを参照していない可能性があります。これらのオブジェクトは現在開かれていないため、使用できない可能性があります。
    
## <a name="remarks"></a>注釈

**imapisession:: compareentryids**メソッドは、1つのサービスプロバイダーに属する2つのエントリ識別子を比較して、同じオブジェクトを参照するかどうかを判断します。 MAPI は、エントリ識別子から[MAPIUID](mapiuid.md)部分を抽出して、オブジェクトを処理するサービスプロバイダーを決定し、そのログオンオブジェクトの**compareentryids**メソッドを呼び出して比較を実行します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**compareentryids**メソッドは、1つのオブジェクトが複数の有効なエントリ識別子を持つことができるので便利です。 このような状況は、サービスプロバイダーの新しいバージョンがインストールされた後などに発生します。 
  
**compareentryids**がエラーを返す場合は、比較の結果に基づいてアクションを実行しないでください。 その代わりに、可能な限り最も厳しい方法を採用します。 たとえば、エントリ識別子の一方または両方に無効な**MAPIUID**が含まれている場合、 **compareentryids**は失敗する可能性があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|basedialog  <br/> |cbasedialog:: oncompareentryids  <br/> |mfcmapi は、 **imapisession:: compareentryids**メソッドを使用して、ユーザーが入力する2つのエントリ id を比較します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

