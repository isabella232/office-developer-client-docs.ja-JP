---
title: HrCompareABEntryIDsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e537c25f-51b5-4f06-a20a-44ee540b9a1f
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 730c24a179cc6aaf8dc2068199ffc206d30156b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800275"
---
# <a name="hrcompareabentryidswithexchangecontext"></a>HrCompareABEntryIDsWithExchangeContext

  
  
**適用されます**: Outlook 
  
複数の Exchange プロファイルに安全に 2 つのアドレス帳**エントリ Id**を比較します。 [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md)の交換用の関数です。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |abhelp.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
HRESULT HrCompareABEntryIDsWithExchangeContext(
  LPMAPISESSION pmsess,
  const MAPIUID *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG * lpulResult
);
```

## <a name="parameters"></a>Parameters

 _pmsess_
  
> [in]**IMAPISession**にログオンします。 NULL にすることはできません。
    
 _pEmsmdbUID_
  
> [in]エントリ id の詳細を表示するのにはこの関数を使用する必要があります Exchange のアドレス帳プロバイダーが含まれている Exchange サービスを識別する**emsmdbUID**へのポインター。 受信のエントリ id が Exchange アドレス帳プロバイダー エントリ識別子でない場合は、このパラメーターは無視され、関数呼び出しは、 [IAddrBook::Details](iaddrbook-details.md)のように動作します。 このパラメーターが NULL またはゼロの MAPIUID の場合は、この関数は、 [IAddrBook::Details](iaddrbook-details.md)のように動作します。
    
 _pAddrBook_
  
> [in]アドレス帳のエントリ id を開くために使用します。 NULL にすることはできません。
    
 _cbEntryID1_
  
> [in]_LpEntryID1_パラメーターで指定された最初のエントリの識別子のバイト数です。 
    
 _lpEntryID1_
  
> [in]比較するアドレス帳のエントリを表す最初のエントリの識別子へのポインター。
    
 _cbEntryID2_
  
> [in]_LpEntryID2_パラメーターで指定された 2 番目のエントリの識別子のバイト数です。 
    
 _lpEntryID2_
  
> [in]比較で使用される 2 番目のエントリの識別子へのポインターを比較するアドレス帳のエントリを表します。
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpulResult_
  
> [out]比較の結果を格納する場所へのポインター。 
    

