---
title: imapisupportcompareentryids
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CompareEntryIDs
api_type:
- COM
ms.assetid: be6991d9-6353-4838-bc6b-39de51a94d8d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6c79943792c8c17ee007c39b5c5c215a6fbc0699
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331571"
---
# <a name="imapisupportcompareentryids"></a>IMAPISupport::CompareEntryIDs

  
  
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
  
> パラメーターとして指定されたいずれかまたは両方のエントリ識別子が有効なオブジェクトを参照していません。現在、使用できない状態である可能性があります。
    
## <a name="remarks"></a>解説

**imapisupport:: compareentryids**メソッドは、アドレス帳およびメッセージストアプロバイダーのサポートオブジェクトに実装されています。 **compareentryids**は、1つのサービスプロバイダーに属する2つのエントリ識別子を比較して、同じオブジェクトを参照しているかどうかを判断します。 MAPI は、エントリ識別子から[MAPIUID](mapiuid.md)部分を抽出して、オブジェクトを処理するサービスプロバイダーを決定します。 MAPI は、そのログオンオブジェクトの**compareentryids**メソッドを呼び出して、比較を実行します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

 **compareentryids**は、1つのオブジェクトが複数の有効なエントリ識別子を持つことができるので便利です。 このような状況は、サービスプロバイダーの新しいバージョンがインストールされた後などに発生します。 
  
**compareentryids**がエラーを返す場合は、比較の結果に基づいてアクションを実行しないでください。 その代わりに、可能な限り最も厳しい方法を採用します。 たとえば、エントリ識別子の一方または両方に無効な**MAPIUID**構造が含まれている場合、 **compareentryids**は失敗する可能性があります。 
  
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

