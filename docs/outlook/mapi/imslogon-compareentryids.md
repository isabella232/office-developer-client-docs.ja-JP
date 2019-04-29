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
  
2つのエントリ識別子を比較して、同じオブジェクトを参照しているかどうかを判断します。 MAPI では、両方のエントリ識別子の一意識別子 (uid) がそのプロバイダによって処理される場合にのみ、サービスプロバイダへの呼び出しを参照します。
  
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
  
> 順番_lpEntryID1_パラメーターによって示されるエントリ識別子のバイト単位のサイズ _。_
    
 _lpEntryID1_
  
> 順番比較する最初のエントリ識別子へのポインター。
    
 _cbEntryID2_
  
> 順番_lpEntryID2_パラメーターによって示されるエントリ識別子のバイト単位のサイズ _。_
    
 _lpEntryID2_
  
> 順番比較する2番目のエントリ id へのポインター。
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lルー result_
  
> 読み上げ返された比較結果へのポインター。 2つのエントリ識別子が同じオブジェクトを参照している場合は TRUE。それ以外の場合は FALSE。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

メッセージストアプロバイダーは、 **IMSLogon:: compareentryids**メソッドを実装して、メッセージストア内の指定されたエントリの2つのエントリ識別子を比較し、それらが同じオブジェクトを参照しているかどうかを判断します。 2つのエントリ識別子が同じオブジェクトを参照している場合、 **compareentryids**は_lpulresult_パラメーターを TRUE に設定します。別のオブジェクトを参照している場合、 **compareentryids**は_lpulresult_を FALSE に設定します。 
  
 **compareentryids**は、1つのオブジェクトが複数の有効なエントリ識別子を持つことができるので便利です。 これは、たとえば、新しいバージョンのメッセージストアプロバイダーがインストールされた後に発生する可能性があります。 
  
## <a name="see-also"></a>関連項目



[IMSLogon : IUnknown](imslogoniunknown.md)

