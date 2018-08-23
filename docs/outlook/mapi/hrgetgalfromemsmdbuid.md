---
title: HrGetGALFromEmsmdbUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9b824e70-ed9a-490c-b777-8902a793fece
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4b05baf1f819a821da3496cc63c2b2980894efd7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575715"
---
# <a name="hrgetgalfromemsmdbuid"></a>HrGetGALFromEmsmdbUID

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
_PEmsmdbUID_によって識別される Exchange サービスのグローバル アドレス帳のエントリの識別子を返します。 返されるエントリの識別子は、 [MAPIFreeBuffer](mapifreebuffer.md)を使用して解放する必要があります。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |abhelp.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
HRESULT HrGetGALFromEmsmdbUID(
  LPMAPISESSION pSess,
  LPADRBOOK lpAdrBook,
  const MAPIUID * pEmsmdbUID,
  ULONG * lpcbeid,
  LPENTRYID * lppeid
);
```

## <a name="parameters"></a>パラメーター

 _pSess_
  
> [in]IMAPISession にログオンします。 NULL にすることはできません。
    
 _pAddrBook_
  
> [in]アドレス帳のエントリ id を開くために使用します。 NULL にすることはできません。
    
 _pEmsmdbUID_
  
> [in]取得する Exchange サービスのグローバル アドレス一覧を識別する**emsmdbUID**へのポインター。 _PEmsmdbUID_が NULL または UID が 0 の場合は、この関数は、レガシ Exchange サービスのグローバル アドレス一覧を取得します。 
    
 _lpcbeid_
  
> [out]グローバル アドレス一覧のエントリの識別子のバイト数へのポインター。
    
 _lppeid_
  
> [out]グローバル アドレス一覧のエントリの識別子へのポインター。 これは、 [MAPIFreeBuffer](mapifreebuffer.md)を使用して解放する必要があります。
    

