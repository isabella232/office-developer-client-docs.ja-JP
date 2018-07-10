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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 03256f2dec62d0228c4d5456dcd1b60f66b13ad2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800351"
---
# <a name="iablogoncompareentryids"></a>IABLogon::CompareEntryIDs

  
  
**適用されます**: Outlook 
  
同じオブジェクトを参照しているかどうかを決定する 2 つのエントリ id を比較します。
  
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

## <a name="parameters"></a>Parameters

 _cbEntryID1_
  
> [in]_LpEntryID1_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID1_
  
> [in]比較する最初のエントリの識別子へのポインター。
    
 _cbEntryID2_
  
> [in]_LpEntryID2_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID2_
  
> [in]比較する 2 番目のエントリの識別子へのポインター。
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpulRet_
  
> [out]比較の結果へのポインター。 2 つのエントリの識別子が同じオブジェクトを参照している場合は TRUE。それ以外の場合、FALSE です。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> エントリ id が正常に比較されました。
    
MAPI_E_INVALID_ENTRYID 
  
> いずれかまたは両方のエントリの識別子は、アドレス帳プロバイダーに属していません。
    
## <a name="remarks"></a>備考

アドレス帳プロバイダーは、同じオブジェクトを参照しているかどうかを決定する 2 つのエントリ id を比較する**CompareEntryIDs**メソッドを実装します。 
  
 **CompareEntryIDs**は、オブジェクトが複数のエントリの有効な識別子を持つことができますので便利です。このような状況には、たとえば、長期的なエントリの識別子を使用して、短期的なエントリ id を比較するときが発生します。 
  
エントリの識別子を作成する方法の詳細については、 [MAPI エントリの識別子](mapi-entry-identifiers.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[IABLogon: IUnknown](iablogoniunknown.md)
