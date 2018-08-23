---
title: IAddrBookCompareEntryIDs
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d6f983e49132e7ab6ea402a8e32bb5ec56d1efba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564851"
---
# <a name="iaddrbookcompareentryids"></a>IAddrBook::CompareEntryIDs

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
同じアドレス帳オブジェクトを参照しているかどうかを判断するのには、特定のアドレス帳プロバイダーに属している 2 つのエントリ id を比較します。 
  
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
  
> [in]_LpEntryID1_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID1_
  
> [in]比較する最初のエントリの識別子へのポインター。
    
 _cbEntryID2_
  
> [in]_LpEntryID2_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID2_
  
> [in]比較する 2 番目のエントリの識別子へのポインター。
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpulResult_
  
> [out]比較の結果へのポインター。 _LpulResult_の内容が TRUE に設定される場合は 2 つのエントリの識別子が同じオブジェクトを参照してください。それ以外の場合、内容は、FALSE に設定されます。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_UNKNOWN_ENTRYID 
  
> _LpEntryID1_または_lpEntryID2_パラメーターで渡されたエントリ id の一方または両方が、アドレス帳プロバイダーで認識されません。 
    
## <a name="remarks"></a>注釈

クライアント アプリケーションとサービス プロバイダーの呼び出し、 **CompareEntryIDs**メソッド 2 つのエントリ id を比較するのには同じオブジェクトを参照しているかどうかを決定する 1 つのアドレス帳プロバイダーに属しています。 **CompareEntryIDs**は、オブジェクトが 1 つ以上の有効なエントリ id を持つことができますので便利です。 このような状況には、たとえば、アドレス帳プロバイダーの新しいバージョンをインストールした後が発生します。 
  
MAPI アドレス帳プロバイダーに、エントリの識別子で登録されている**MAPIUID**構造を持つエントリの識別子の[MAPIUID](mapiuid.md)構造を照合することによって適切なプロバイダーを決定するには、この呼び出しを渡します、プロバイダーです。 
  
**CompareEntryIDs**が TRUE に_lpulResult_パラメーターの内容を設定する場合は 2 つのエントリの識別子は、同じオブジェクトを参照してください、別のオブジェクトを参照している場合、 **CompareEntryIDs**は false を指定する内容を設定します。 どちらの場合では、 **CompareEntryIDs**は、S_OK を返します。 **CompareEntryIDs**エントリの識別子に一致する**MAPIUID**構造体を登録されているアドレス帳プロバイダーがない場合に発生する、エラーを取得する場合は、クライアントとプロバイダーはかかりません操作の結果に基づいて、比較します。 実行中のアクションを最も保守的なアプローチを受講する必要があります代わりにします。 
  
## <a name="see-also"></a>関連項目



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

