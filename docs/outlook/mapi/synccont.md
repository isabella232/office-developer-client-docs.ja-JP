---
title: SYNCCONT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b4307a3-5a8c-89bf-1113-2549556a7fe7
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 82923895353cf600c4d0b78b9a6e16fc7d57e466
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804058"
---
# <a name="synccont"></a>SYNCCONT

**適用対象**: Outlook 
  
[内容の状態を同期](synchronize-contents-state.md)する際にサーバーとローカル ストア内の指定したフォルダーの内容を同期するための情報です。 これだけのアップロード、またはアップロードし、ダウンロードを含む完全な同期が含まれます。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
struct SYNCCONT 
{ 
   ULONG   ulFlags; 
   UINT   iEnt; 
   UINT   cEnt; 
   LPVOID    pvReserved; 
   LPSPropTagArray   ptagaReserved; 
   LPSSortOrderSet   psosReserved; 
};
```

## <a name="members"></a>Members

_ulFlags_
  
> [in]同期中に適切な動作を決定するフラグを設定します。
    
  - UPC_OK
    
  - [in]アップロードまたは完全な同期が成功しました。 クライアントでは、情報をサーバーと同期した後、これを設定します。
    
_iEnt_
  
> [out]_セント_で指定されたフォルダーの内容の同期を追跡するためにインデックスを作成します。
    
_セント_
  
> [out]レプリケートするフォルダーの数です。
    
_pvReserved_
  
> このメンバーは、Outlook の内部使用に予約されている、サポートされていません。 
    
_ptagaReserved_
  
> このメンバーは、Outlook の内部使用に予約されている、サポートされていません。 
    
_psosReserved_
  
> このメンバーは、Outlook の内部使用に予約されている、サポートされていません。 
    
## <a name="see-also"></a>関連項目

- [レプリケーション API について](about-the-replication-api.md)
- [レプリケーション ステート マシンについて](about-the-replication-state-machine.md)
- [MAPI �萔](mapi-constants.md)

