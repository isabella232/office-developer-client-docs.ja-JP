---
title: IABLogonCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.CompareEntryIDs
api_type:
- COM
ms.assetid: cb4a38ff-2fdd-40ac-a613-12c3f11a1df9
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 48ddb5a7c4e013c03138b08d9dadcdc0991faeec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438373"
---
# <a name="iablogoncompareentryids"></a>IABLogon::CompareEntryIDs

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
2つのエントリ識別子を比較して、同じオブジェクトを参照しているかどうかを判断します。
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulRet
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
    
 _lアウト ret_
  
> 読み上げ比較結果へのポインター。 2つのエントリ識別子が同じオブジェクトを参照していることを示す場合は TRUE。それ以外の場合は FALSE。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> エントリ識別子が正常に比較されました。
    
MAPI_E_INVALID_ENTRYID 
  
> 一方または両方のエントリ識別子は、アドレス帳プロバイダーに属していません。
    
## <a name="remarks"></a>注釈

アドレス帳プロバイダーは、2つのエントリ識別子を比較して同じオブジェクトを参照するかどうかを判断するために、 **compareentryids**メソッドを実装します。 
  
 **compareentryids**は、1つのオブジェクトが複数の有効なエントリ識別子を持つことができるので便利です。このような状況は、短い用語のエントリ id を長期のエントリ識別子と比較する場合などに発生する可能性があります。 
  
エントリ識別子を作成する方法の詳細については、「 [MAPI エントリ識別子](mapi-entry-identifiers.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[IABLogon : IUnknown](iablogoniunknown.md)

