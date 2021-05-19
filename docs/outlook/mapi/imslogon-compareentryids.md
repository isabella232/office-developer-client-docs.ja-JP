---
title: IMSLogonCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.CompareEntryIDs
api_type:
- COM
ms.assetid: 481812d6-8e94-4510-b288-55501dd5757c
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4196ed8b949ecb9e23c4bd34380db9cc5a369e23
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410134"
---
# <a name="imslogoncompareentryids"></a>IMSLogon::CompareEntryIDs

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
2 つのエントリ識別子を比較して、同じオブジェクトを参照するかどうかを判断します。 MAPI は、比較する両方のエントリ識別子の一意識別子 (UID) が、そのプロバイダーによって処理される場合にのみ、サービス プロバイダーに対してこの呼び出しを参照します。
  
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
  
> [in]  _lpEntryID1_ パラメーターが指すエントリ識別子のサイズ (バイト  _単位)。_
    
 _lpEntryID1_
  
> [in]比較する最初のエントリ識別子へのポインター。
    
 _cbEntryID2_
  
> [in]  _lpEntryID2_ パラメーターが指すエントリ識別子のサイズ (バイト  _単位)。_
    
 _lpEntryID2_
  
> [in]比較する 2 番目のエントリ識別子へのポインター。
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpulResult_
  
> [out]比較の返される結果へのポインター。 2 つのエントリ識別子が同じオブジェクトを参照する場合は TRUE。それ以外の場合は FALSE。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

メッセージ ストア プロバイダーは **、IMSLogon::CompareEntryIDs** メソッドを実装して、メッセージ ストア内の特定のエントリの 2 つのエントリ識別子を比較して、同じオブジェクトを参照するかどうかを判断します。 2 つのエントリ識別子が同じオブジェクトを参照する場合 **、CompareEntryIDs は**  _lpulResult_ パラメーターを TRUE に設定します。異なるオブジェクトを参照する場合 **、CompareEntryIDs は**  _lpulResult を FALSE に_ 設定します。 
  
 **CompareEntryIDs は** 、オブジェクトが複数の有効なエントリ識別子を持つ可能性がある場合に便利です。 これは、たとえば、メッセージ ストア プロバイダーの新しいバージョンがインストールされた後に発生する可能性があります。 
  
## <a name="see-also"></a>関連項目



[IMSLogon : IUnknown](imslogoniunknown.md)

