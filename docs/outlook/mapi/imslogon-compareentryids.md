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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c2e6600af66f3dab8ff0fbb5442a1354687a3cbb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801038"
---
# <a name="imslogoncompareentryids"></a>IMSLogon::CompareEntryIDs

  
  
**適用されます**: Outlook 
  
同じオブジェクトを参照しているかどうかを決定する 2 つのエントリ id を比較します。 MAPI は、両方のエントリの識別子を比較するには、一意の識別子 (Uid) がそのプロバイダーによって処理される場合にのみ、サービス ・ プロバイダーへの呼び出しを意味します。
  
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

## <a name="parameters"></a>Parameters

 _cbEntryID1_
  
> [in]_._ _LpEntryID1_パラメーターで指定されたエントリの識別子のバイト単位のサイズ
    
 _lpEntryID1_
  
> [in]比較する最初のエントリの識別子へのポインター。
    
 _cbEntryID2_
  
> [in]_._ _LpEntryID2_パラメーターで指定されたエントリの識別子のバイト単位のサイズ
    
 _lpEntryID2_
  
> [in]比較する 2 番目のエントリの識別子へのポインター。
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpulResult_
  
> [out]比較の結果が返されましたへのポインター。 2 つのエントリの識別子が同じオブジェクトを参照する場合は TRUE。それ以外の場合、FALSE です。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

メッセージ ストア プロバイダーは、同じオブジェクトを参照しているかどうかを確認するメッセージ ・ ストア内の指定されたエントリの 2 つのエントリ id を比較する**IMSLogon::CompareEntryIDs**メソッドを実装します。 **CompareEntryIDs**が TRUE に_lpulResult_パラメーターを設定する場合は 2 つのエントリの識別子は、同じオブジェクトを参照してください、別のオブジェクトを参照している場合、 **CompareEntryIDs**は false を指定する_lpulResult_を設定します。 
  
 **CompareEntryIDs**は、オブジェクトが 1 つ以上の有効なエントリ id を持つことができますので便利です。 これは、たとえば、メッセージ ストア プロバイダーの新しいバージョンをインストールした後に発生します。 
  
## <a name="see-also"></a>関連項目



[IMSLogon: IUnknown](imslogoniunknown.md)

