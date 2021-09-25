---
title: IABLogonCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABLogon.CompareEntryIDs
api_type:
- COM
ms.assetid: cb4a38ff-2fdd-40ac-a613-12c3f11a1df9
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ca5474e56a1a72124e6d49bc67329994e6eec04f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571921"
---
# <a name="iablogoncompareentryids"></a>IABLogon::CompareEntryIDs

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
2 つのエントリ識別子を比較して、同じオブジェクトを参照するかどうかを判断します。
  
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
  
> [in]  _lpEntryID1_ パラメーターが指すエントリ識別子のバイト 数。 
    
 _lpEntryID1_
  
> [in]比較する最初のエントリ識別子へのポインター。
    
 _cbEntryID2_
  
> [in]  _lpEntryID2_ パラメーターが指すエントリ識別子のバイト 数。 
    
 _lpEntryID2_
  
> [in]比較する 2 番目のエントリ識別子へのポインター。
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpulRet_
  
> [out]比較の結果へのポインター。 TRUE を指定すると、2 つのエントリ識別子が同じオブジェクトを参照します。それ以外の場合は FALSE。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> エントリ識別子が正常に比較されました。
    
MAPI_E_INVALID_ENTRYID 
  
> エントリ識別子の一方または両方がアドレス帳プロバイダーに属していない。
    
## <a name="remarks"></a>注釈

アドレス帳プロバイダーは **CompareEntryIDs** メソッドを実装して、2 つのエントリ識別子を比較して、同じオブジェクトを参照するかどうかを判断します。 
  
 **CompareEntryIDs は** 、オブジェクトが複数の有効なエントリ識別子を持つ可能性がある場合に便利です。このような状況は、たとえば、短期エントリ識別子と長期エントリ識別子を比較するときに発生する可能性があります。 
  
エントリ識別子を作成する方法の詳細については、「MAPI エントリ識別子 [」を参照してください](mapi-entry-identifiers.md)。
  
## <a name="see-also"></a>関連項目



[IABLogon : IUnknown](iablogoniunknown.md)

