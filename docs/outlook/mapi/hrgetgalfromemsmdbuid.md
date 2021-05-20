---
title: HrGetGALFromEmsmdbUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9b824e70-ed9a-490c-b777-8902a793fece
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b9a31fec93ec7fafc4d1565d63e4bc427ba4050e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439108"
---
# <a name="hrgetgalfromemsmdbuid"></a>HrGetGALFromEmsmdbUID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
_pEmsmdbUID_ で識別される Exchangeアドレス帳のエントリ識別子を返します。 返されるエントリ識別子は [、MAPIFreeBuffer を使用して解放する必要があります](mapifreebuffer.md)。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |abhelp.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
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
  
> [in]ログオンしている IMAPISession。 NULL にすることはできません。
    
 _pAddrBook_
  
> [in]エントリ識別子を開くのに使用するアドレス帳。 NULL にすることはできません。
    
 _pEmsmdbUID_
  
> [in]取得するサービスの GAL を識別する **emsmdbUID** Exchangeポインター。 _pEmsmdbUID_ が NULL または 0 の UID の場合、この関数は、Exchange サービスの従来の GAL を取得します。 
    
 _lpcbeid_
  
> [out]グローバル アドレス一覧のエントリ識別子のバイト数へのポインター。
    
 _lppeid_
  
> [out]グローバル アドレス一覧のエントリ識別子へのポインター。 これは [MAPIFreeBuffer を使用して解放する必要があります](mapifreebuffer.md)。
    

