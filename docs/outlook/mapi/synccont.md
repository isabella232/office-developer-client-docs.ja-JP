---
title: SYNCCONT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b4307a3-5a8c-89bf-1113-2549556a7fe7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: afba7fa718a35d33966d45289461313e349ef2e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349575"
---
# <a name="synccont"></a>SYNCCONT

**適用対象**: Outlook 2013 | Outlook 2016 
  
[コンテンツ同期状態](synchronize-contents-state.md)の間に、ローカルストア内の指定したフォルダーの内容をサーバーと同期するための情報。 これにはアップロードのみが含まれます。または、アップロードとダウンロードを含む完全同期を行います。
  
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

## <a name="members"></a>メンバー

_ulFlags_
  
> 順番同期時に適切な動作を決定するフラグ。
    
  - UPC_OK
    
  - 順番アップロードまたは完全同期が正常に完了しました。 クライアントは、情報をサーバーと同期した後にこれを設定します。
    
_ient_
  
> 読み上げによって指定されたフォルダーの数について__ のコンテンツの同期を追跡するインデックス。
    
_fea-cent-logging-service_
  
> 読み上げレプリケートするフォルダーの数。
    
_pvreserved_
  
> このメンバーは、Outlook の内部使用のために予約されており、サポートされていません。 
    
_ptagaReserved_
  
> このメンバーは、Outlook の内部使用のために予約されており、サポートされていません。 
    
_psosreserved_
  
> このメンバーは、Outlook の内部使用のために予約されており、サポートされていません。 
    
## <a name="see-also"></a>関連項目

- [レプリケーション API について](about-the-replication-api.md)
- [レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
- [MAPI 定数](mapi-constants.md)

