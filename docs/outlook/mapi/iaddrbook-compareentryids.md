---
title: iaddrbookcompareentryids
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBookCompareEntryIDs
api_type:
- COM
ms.assetid: 7dabc1d3-5ea4-482f-91a9-9ef3009eddd2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b6abecc298df7a86afff9338752a15615c73b3a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424260"
---
# <a name="iaddrbookcompareentryids"></a>IAddrBook::CompareEntryIDs

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
特定のアドレス帳プロバイダーに属する2つのエントリ識別子を比較して、同じアドレス帳オブジェクトを参照しているかどうかを判断します。 
  
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
  
> 読み上げ比較結果へのポインター。 2つのエントリ識別子が同じオブジェクトを参照する場合、 _lアウト result_の内容は TRUE に設定されます。それ以外の場合は、内容が FALSE に設定されます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_UNKNOWN_ENTRYID 
  
> _lpEntryID1_パラメーターまたは_lpEntryID2_パラメーターと共に渡されたエントリ識別子の一方または両方が、アドレス帳プロバイダーによって認識されません。 
    
## <a name="remarks"></a>注釈

クライアントアプリケーションおよびサービスプロバイダーは、1つのアドレス帳プロバイダーに属する2つのエントリ識別子を比較して、同じオブジェクトを参照しているかどうかを判断するために、 **compareentryids**メソッドを呼び出します。 **compareentryids**は、1つのオブジェクトが複数の有効なエントリ識別子を持つことができるので便利です。 このような状況は、アドレス帳プロバイダーの新しいバージョンがインストールされた後などに発生します。 
  
この呼び出しは、エントリ識別子を処理するアドレス帳プロバイダーに渡され、エントリ識別子の[MAPIUID](mapiuid.md)構造と、 **MAPIUID**構造が一致することによって適切なプロバイダーが決定されます。供給. 
  
2つのエントリ識別子が同じオブジェクトを参照している場合、 **compareentryids**は_lpulresult_パラメーターの内容を TRUE に設定します。異なるオブジェクトを参照している場合、 **compareentryids**は内容を FALSE に設定します。 どちらの場合も、 **compareentryids**は S_OK を返します。 **compareentryids**がエラーを返した場合は、アドレス帳プロバイダーが登録されていない**MAPIUID**構造がエントリ識別子内にある場合、クライアントとプロバイダーは、その結果に基づいて操作を行うことはできません。結果. そのような場合は、実行するアクションに対して最も慎重な方法をとる必要があります。 
  
## <a name="see-also"></a>関連項目



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

