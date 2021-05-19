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
  
特定のアドレス帳プロバイダーに属する 2 つのエントリ識別子を比較して、同じアドレス帳オブジェクトを参照するかどうかを判断します。 
  
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
  
> [in]  _lpEntryID1_ パラメーターが指すエントリ識別子のバイト 数。 
    
 _lpEntryID1_
  
> [in]比較する最初のエントリ識別子へのポインター。
    
 _cbEntryID2_
  
> [in]  _lpEntryID2_ パラメーターが指すエントリ識別子のバイト 数。 
    
 _lpEntryID2_
  
> [in]比較する 2 番目のエントリ識別子へのポインター。
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpulResult_
  
> [out]比較の結果へのポインター。 2 つのエントリ識別子が同じオブジェクトを参照する場合  _、lpulResult_ の内容は TRUE に設定されます。それ以外の場合、コンテンツは FALSE に設定されます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_UNKNOWN_ENTRYID 
  
> _lpEntryID1_ または _lpEntryID2_ パラメーターで渡されたエントリ識別子の一方または両方は、アドレス帳プロバイダーによって認識されません。 
    
## <a name="remarks"></a>注釈

クライアント アプリケーションとサービス プロバイダーは **CompareEntryIDs** メソッドを呼び出して、1 つのアドレス帳プロバイダーに属する 2 つのエントリ識別子を比較して、同じオブジェクトを参照するかどうかを判断します。 **CompareEntryIDs は** 、オブジェクトが複数の有効なエントリ識別子を持つ可能性がある場合に便利です。 この状況は、たとえば、アドレス帳プロバイダーの新しいバージョンがインストールされた後に発生する可能性があります。 
  
MAPI は、エントリ識別子を担当するアドレス帳プロバイダーにこの呼び出しを渡し、エントリ識別子の [MAPIUID](mapiuid.md) 構造をプロバイダーによって登録された **MAPIUID** 構造と照合して、適切なプロバイダーを決定します。 
  
2 つのエントリ識別子が同じオブジェクトを参照する場合 **、CompareEntryIDs は**  _lpulResult_ パラメーターの内容を TRUE に設定します。異なるオブジェクトを参照する場合 **、CompareEntryIDs はコンテンツ** を FALSE に設定します。 どちらの場合も **、CompareEntryIDs は** データをS_OK。 **CompareEntryIDs** がエラーを返す場合は、アドレス帳プロバイダーがエントリ識別子の **MAPIUID** 構造と一致する MAPIUID 構造を登録していない場合に発生する可能性があります。クライアントとプロバイダーは、比較の結果に基づいてアクションを実行する必要があります。 代わりに、実行するアクションに対して最も保守的なアプローチを取る必要があります。 
  
## <a name="see-also"></a>関連項目



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

