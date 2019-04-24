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
ms.openlocfilehash: b9a31fec93ec7fafc4d1565d63e4bc427ba4050e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347832"
---
# <a name="hrgetgalfromemsmdbuid"></a>HrGetGALFromEmsmdbUID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
_pEmsmdbUID_によって識別される Exchange サービスのグローバルアドレス帳のエントリ id を返します。 返されたエントリ id は、 [MAPIFreeBuffer](mapifreebuffer.md)を使用して解放する必要があります。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |abhelp .h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
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

 _psess_
  
> 順番ログオンしている imapisession。 NULL にすることはできません。
    
 _pAddrBook_
  
> 順番エントリ識別子を開くために使用されるアドレス帳。 NULL にすることはできません。
    
 _pEmsmdbUID_
  
> 順番取得する Exchange サービスの GAL を識別する**emsmdbUID**へのポインター。 _pEmsmdbUID_が NULL またはゼロ UID の場合、この関数は、Exchange サービスの従来の GAL を取得します。 
    
 _lpcbeid_
  
> 読み上げグローバルアドレス一覧のエントリ識別子のバイト数へのポインター。
    
 _lppeid_
  
> 読み上げグローバルアドレス一覧のエントリ識別子へのポインター。 これは、 [MAPIFreeBuffer](mapifreebuffer.md)を使用して解放する必要があります。
    

